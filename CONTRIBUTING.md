# Contributing to IFRS Gap Analysis System

Thank you for your interest in contributing to the IFRS Gap Analysis System! This document provides guidelines for contributing to the project.

## 🚀 Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/yourusername/ifrs-gap-analysis.git
   cd ifrs-gap-analysis
   ```
3. **Install dependencies**:
   ```bash
   npm install
   ```
4. **Set up environment variables**:
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

## 🔧 Development Setup

### Prerequisites
- Node.js 18+
- PostgreSQL database
- OpenAI API key for testing

### Running the Application
```bash
npm run dev
```

This starts both the frontend (Vite) and backend (Express) servers.

## 📝 Making Changes

### Branch Naming
- `feature/description` - for new features
- `fix/description` - for bug fixes
- `docs/description` - for documentation updates
- `refactor/description` - for code refactoring

### Code Style
- TypeScript for all new code
- Use existing ESLint configuration
- Follow React/Express best practices
- Add type definitions for new features

### Testing
- Test your changes thoroughly
- Ensure the application builds without errors
- Verify both frontend and backend functionality

## 🐛 Bug Reports

When reporting bugs, please include:
- Clear description of the issue
- Steps to reproduce
- Expected vs actual behavior
- Environment details (OS, browser, Node.js version)
- Screenshots if applicable

## ✨ Feature Requests

For new features:
- Describe the feature and its use case
- Explain how it improves the application
- Consider backwards compatibility
- Provide mockups or examples if helpful

## 🔀 Pull Request Process

1. **Create a feature branch** from `main`
2. **Make your changes** with clear commit messages
3. **Test thoroughly** - ensure nothing breaks
4. **Update documentation** if needed
5. **Submit a pull request** with:
   - Clear title and description
   - Link to any related issues
   - Screenshots for UI changes
   - Test instructions

### Pull Request Template
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Refactoring

## Testing
- [ ] Tested locally
- [ ] No console errors
- [ ] All features working

## Screenshots (if applicable)
Add screenshots for UI changes
```

## 📊 Areas for Contribution

### High Priority
- Enhanced error handling and user feedback
- Additional export formats (Word, PowerPoint)
- Improved AI analysis accuracy
- Performance optimizations

### Medium Priority
- Multi-language support
- Advanced filtering and search
- Batch processing multiple reports
- Integration with other sustainability frameworks

### Documentation
- API documentation
- User guides
- Video tutorials
- Translation of documentation

## 🤝 Community Guidelines

- Be respectful and constructive
- Follow the code of conduct
- Help newcomers get started
- Share knowledge and best practices
- Focus on the project's sustainability reporting mission

## 📚 Resources

- [React Documentation](https://react.dev/)
- [Express.js Guide](https://expressjs.com/)
- [IFRS Sustainability Standards](https://www.ifrs.org/sustainability/)
- [OpenAI API Documentation](https://platform.openai.com/docs)

## 📞 Getting Help

- Create an issue for bugs or questions
- Join discussions in GitHub Discussions
- Check existing issues before creating new ones

Thank you for contributing to making sustainability reporting more accessible and accurate! 🌱