# IFRS Gap Analysis System

AI-powered tool that analyzes annual reports against IFRS S1 and S2 sustainability standards.

## Features

- Upload annual report (PDF) for automated compliance analysis
- Pre-loaded official IFRS S1 and S2 standards
- AI-powered gap analysis using your OpenAI API key
- Export results to Excel and PDF

## Quick Start

1. **Get OpenAI API Key**: Visit [platform.openai.com](https://platform.openai.com/account/api-keys)
2. **Access Settings**: Enter your API key and save
3. **Upload Report**: Go to Analysis page and upload your annual report
4. **Start Analysis**: Click "Start Analysis" and download results

## Setup

```bash
git clone https://github.com/yourusername/ifrs-gap-analysis.git
cd ifrs-gap-analysis
npm install

# Set environment variables
cp .env.example .env
# Add your DATABASE_URL

# Start development
npm run dev
```

## Environment Variables

```env
DATABASE_URL=your_postgresql_url
NODE_ENV=production
```

Note: Users provide their own OpenAI API keys through the app settings.

## License

MIT License - see [LICENSE](LICENSE) file.