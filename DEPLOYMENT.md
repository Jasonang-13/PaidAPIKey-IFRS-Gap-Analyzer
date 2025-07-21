# Deployment Guide

## Quick Deploy Options

### 1. Vercel (Recommended)
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Follow prompts to connect your GitHub repo
```

### 2. Netlify
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Build and deploy
npm run build
netlify deploy --prod --dir=dist
```

### 3. Railway
```bash
# Install Railway CLI
npm install -g @railway/cli

# Login and deploy
railway login
railway link
railway up
```

### 4. Render
1. Connect your GitHub repository
2. Set build command: `npm install && npm run build`
3. Set start command: `npm start`
4. Add environment variables in dashboard

## Environment Variables for Production

```env
DATABASE_URL=your_production_database_url
NODE_ENV=production
PORT=5000
```

Note: Users provide their own OPENAI_API_KEY through the Settings page.

## Database Setup

### PostgreSQL (Production)
```sql
-- Create database
CREATE DATABASE ifrs_analysis;

-- Run migrations (handled automatically by Drizzle)
```

### Neon (Serverless)
1. Create account at neon.tech
2. Create database
3. Copy connection string to DATABASE_URL

## Build Commands

```bash
# Install dependencies
npm install

# Build frontend
npm run build

# Start production server
npm start
```

## Health Check

Your app should respond at:
- `/` - Main application
- `/api/analyses` - API endpoint
- `/settings` - Settings page