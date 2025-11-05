# Koloni

**Koloni** is an AI-powered platform where governance, creativity, and automation converge. Every artifact is sealed, auditable, and inheritable, ensuring scalable experimentation, zero-cost rituals, and communal lineage.

## Features

### 🐝 Core Platform
- **Decentralized Governance**: Community-driven decision making
- **Creative Tools**: AI-powered content creation
- **Automation**: Streamlined workflows and processes
- **Auditable Artifacts**: Transparent and traceable content

### ✨ Koloni Creator Studio

The Creator Studio is an AI-powered content generation platform that enables users to create, format, and export content for various social media platforms.

#### Key Features:

**AI Content Generation**
- 🎨 **LongCat Format**: Generate vertical, scrollable content optimized for mobile viewing
- ⚡ **Emu Format**: Create quick, impactful content for rapid consumption
- 🎯 Multiple style and tone options (Creative, Professional, Casual, Humorous, Educational)
- 🧠 Powered by OpenAI GPT-4 for high-quality content

**Smart Export System**
- 📷 **Instagram Export**: Automatically format content with captions, hashtags, and optimal spacing
- 🎥 **YouTube Export**: Generate titles, descriptions, tags, and structured chapters
- 📋 One-click copy to clipboard
- 💡 Platform-specific tips and best practices

**Token Management**
- 🪙 Credit-based system for AI generations
- 💳 Stripe integration for token purchases
- 📊 Transaction history and balance tracking
- 🔄 Automatic token deduction and management

**User Experience**
- 📜 Generation history with search and retrieval
- 🎨 Clean, modern interface with dark mode
- 📱 Fully responsive design
- ⚡ Real-time feedback and notifications

#### Technology Stack:

**Frontend**
- Vanilla JavaScript (ES6+)
- Modern CSS with CSS Variables
- Responsive design principles
- Accessibility-first approach

**Backend (Netlify Functions)**
- \`generate-longcat.js\` - LongCat AI content generation
- \`generate-emu.js\` - Emu AI content generation
- \`export-instagram.js\` - Instagram content formatting
- \`export-youtube.js\` - YouTube content formatting
- \`token-manager.js\` - Token/credit management system
- \`stripe-webhook.js\` - Payment processing webhooks

**Integrations**
- OpenAI GPT-4 API
- Stripe Payments
- Netlify Serverless Functions

## Getting Started

### Prerequisites
- Node.js 18 or higher
- Netlify CLI (optional, for local development)
- OpenAI API key
- Stripe account (for payments)

### Installation

1. Clone the repository:
\`\`\`bash
git clone https://github.com/brandonlacoste9-tech/Koloni.git
cd Koloni
\`\`\`

2. Install dependencies:
\`\`\`bash
npm install
\`\`\`

3. Set up environment variables:
\`\`\`bash
cp .env.example .env
# Edit .env with your API keys
\`\`\`

4. Build the project:
\`\`\`bash
node build.js
\`\`\`

5. Run locally (optional):
\`\`\`bash
netlify dev
\`\`\`

Visit \`http://localhost:8888/create.html\` to access the Creator Studio.

### Deployment

See [DEPLOYMENT_CHECKLIST.md](./DEPLOYMENT_CHECKLIST.md) for detailed deployment instructions.

Quick deploy to Netlify:
\`\`\`bash
netlify deploy --prod
\`\`\`

## Project Structure

\`\`\`
Koloni/
├── netlify/
│   └── functions/          # Serverless functions
│       ├── generate-longcat.js
│       ├── generate-emu.js
│       ├── export-instagram.js
│       ├── export-youtube.js
│       ├── token-manager.js
│       └── stripe-webhook.js
├── src/
│   ├── components/         # Reusable UI components
│   ├── css/               # Stylesheets
│   │   └── creator.css
│   ├── js/                # JavaScript modules
│   │   ├── ai-router.js
│   │   └── creator.js
│   └── create.html        # Creator Studio UI
├── build.js               # Build script
├── .env.example           # Environment variables template
├── .gitignore            # Git ignore rules
├── DEPLOYMENT_CHECKLIST.md
└── README.md
\`\`\`

## Environment Variables

Required environment variables (see \`.env.example\`):

- \`OPENAI_API_KEY\` - Your OpenAI API key
- \`STRIPE_SECRET_KEY\` - Stripe secret key
- \`STRIPE_PUBLISHABLE_KEY\` - Stripe publishable key
- \`STRIPE_WEBHOOK_SECRET\` - Stripe webhook signing secret
- \`URL\` - Your site URL (auto-set by Netlify in production)

## Usage

### Creating Content

1. Navigate to \`/create.html\`
2. Select your desired format (LongCat or Emu)
3. Enter your content prompt
4. Choose style and tone options
5. Click "Generate Content"
6. Review and export to your preferred platform

### Exporting Content

1. Go to the Export tab
2. Select your platform (Instagram or YouTube)
3. Paste or use generated content
4. Click "Format for Export"
5. Copy the formatted content and tips

## Security

🔒 **Security Best Practices:**
- All API keys are stored as environment variables
- Webhook signatures are verified for Stripe events
- \`.env\` file is never committed to version control
- Sensitive data is never exposed to the frontend
- CORS headers limit API access

## Contributing

We welcome contributions! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

[Add your license here]

## Support

For issues, questions, or feature requests:
- Open an issue on GitHub
- Check the [DEPLOYMENT_CHECKLIST.md](./DEPLOYMENT_CHECKLIST.md) for troubleshooting

## Roadmap

- [ ] User authentication and accounts
- [ ] Database integration for persistent storage
- [ ] Additional AI content formats
- [ ] More social media platform integrations
- [ ] Analytics dashboard
- [ ] Team collaboration features
- [ ] Advanced AI customization options
- [ ] Content scheduling and automation

---

Built with 🐝 by the Koloni community
