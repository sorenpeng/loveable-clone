# Loveable Clone

A clone of the Loveable platform built with the Claude Code SDK for AI-powered development assistance.

## Overview

This project aims to recreate the core functionality of Loveable, a platform that enables rapid web application development through AI assistance. By leveraging the Claude Code SDK, this clone provides intelligent code generation, debugging, and development workflow automation.

## Features

- 🤖 AI-powered code generation using Claude Code SDK
- 🚀 Rapid prototyping and development
- 🔧 Intelligent debugging and error resolution
- 📝 Automated documentation generation
- 🎨 UI/UX design assistance
- 🔄 Real-time code suggestions and improvements

## Prerequisites

Before getting started, ensure you have:

- Node.js (v18 or higher)
- npm or yarn package manager
- Claude API key (for SDK integration)
- Git for version control

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd loveable-clone
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

3. Set up environment variables:
```bash
cp .env.example .env
```

Add your Claude API key to the `.env` file:
```
CLAUDE_API_KEY=your_api_key_here
```

## Claude Code SDK Integration

This project utilizes the Claude Code SDK for AI-powered development features:

### Setup

```javascript
import { Claude } from '@anthropic-ai/sdk';

const claude = new Claude({
  apiKey: process.env.CLAUDE_API_KEY,
});
```

### Key Features

- **Code Generation**: Generate components, functions, and entire modules
- **Code Review**: Automated code analysis and suggestions
- **Documentation**: Auto-generate documentation from code
- **Debugging**: AI-assisted error detection and resolution

## Project Structure

```
loveable-clone/
├── src/
│   ├── components/     # React components
│   ├── services/       # API and Claude SDK services
│   ├── utils/          # Utility functions
│   └── pages/          # Application pages
├── public/             # Static assets
├── docs/               # Documentation
└── tests/              # Test files
```

## Development

### Running the Development Server

```bash
npm run dev
# or
yarn dev
```

The application will be available at `http://localhost:3000`.

### Building for Production

```bash
npm run build
# or
yarn build
```

### Running Tests

```bash
npm test
# or
yarn test
```

## Usage

### Basic Code Generation

```javascript
import { generateCode } from './services/claude';

const prompt = "Create a React component for a user profile card";
const generatedCode = await generateCode(prompt);
```

### AI-Assisted Development

1. **Component Generation**: Describe your component requirements
2. **Code Review**: Submit code for AI analysis
3. **Bug Fixing**: Get AI suggestions for error resolution
4. **Optimization**: Receive performance improvement recommendations

## Configuration

### Claude SDK Settings

Customize the Claude integration in `src/config/claude.js`:

```javascript
export const claudeConfig = {
  model: 'claude-3-sonnet-20240229',
  maxTokens: 4000,
  temperature: 0.7,
  // Additional configuration options
};
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## API Documentation

### Claude Integration Endpoints

- `POST /api/generate` - Generate code from natural language
- `POST /api/review` - Review and analyze existing code
- `POST /api/debug` - Get debugging assistance
- `POST /api/optimize` - Receive optimization suggestions

## Troubleshooting

### Common Issues

1. **API Key Issues**: Ensure your Claude API key is valid and properly set
2. **Rate Limiting**: Implement proper rate limiting for API calls
3. **Token Limits**: Monitor token usage to avoid exceeding limits

### Getting Help

- Check the [Claude SDK documentation](https://docs.anthropic.com/)
- Review the project issues on GitHub
- Join our community discussions

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Anthropic for the Claude AI platform
- The Loveable team for inspiration
- Open source community contributors

## Roadmap

- [ ] Enhanced UI/UX design tools
- [ ] Multi-language code generation
- [ ] Advanced debugging features
- [ ] Integration with popular IDEs
- [ ] Collaborative development features
- [ ] Performance monitoring and analytics

---

**Note**: This is a clone project for educational and development purposes. Please respect the original Loveable platform and its intellectual property.