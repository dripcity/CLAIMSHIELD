# ClaimShield DCV

> AI-Powered Diminished Value Appraisal Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Next.js](https://img.shields.io/badge/Next.js-14.x-black)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-18.x-61DAFB)](https://reactjs.org/)

## 📋 Overview

**ClaimShield DCV** is an advanced SaaS platform that revolutionizes diminished value (DV) appraisals for vehicles involved in accidents. Using AI-powered automation and comprehensive market data analysis, ClaimShield generates professional, insurance-accepted appraisal reports that help vehicle owners recover fair compensation for the inherent loss in their vehicle's market value.

### The Problem

When a vehicle is involved in an accident and subsequently repaired, its market value drops—even with flawless repairs. This is called **Diminished Value**. Insurance companies often:
- Use outdated formulas (like the controversial 17c method)
- Undervalue or deny DV claims
- Create barriers through complex claim processes
- Offer settlements far below actual market loss

### Our Solution

ClaimShield DCV provides:
- **Automated DV Calculations**: AI-driven algorithms using real market data
- **Professional Reports**: Insurance-accepted appraisal documentation
- **Claim Support**: Step-by-step guidance through the entire claim process
- **Fair Valuations**: Market-based assessments, not arbitrary formulas
- **Fast Turnaround**: Generate reports in minutes, not days

## ✨ Key Features

### 🤖 AI-Powered Valuation Engine
- Real-time market comparisons using live vehicle data
- Advanced damage severity analysis
- State-specific valuation methodologies
- Predictive analytics for resale impact

### 📊 Comprehensive Reporting
- Professional PDF appraisal reports
- CARFAX/AutoCheck integration
- Detailed damage documentation
- Market data visualization with charts
- Pre-accident vs. post-accident value analysis

### 💼 Insurance Claim Management
- Guided claim filing workflows
- Auto-generated demand letters
- Negotiation support and templates
- Progress tracking dashboard
- Document management system

### 🔐 Secure & Compliant
- Firebase Authentication
- End-to-end encryption for sensitive data
- GDPR/CCPA compliant data handling
- Secure document storage
- Role-based access control

## 🏗️ Technology Stack

### Frontend
- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **UI Library**: React 18
- **Styling**: Tailwind CSS + shadcn/ui components
- **State Management**: React Hooks & Context
- **Forms**: React Hook Form + Zod validation
- **Charts**: Recharts for data visualization
- **Icons**: Lucide React

### Backend & Services
- **Authentication**: Firebase Auth
- **Database**: Firebase Firestore
- **Storage**: Firebase Storage
- **AI/ML**: OpenAI GPT-4 API
- **API Client**: Axios
- **Hosting**: Vercel (recommended)

### Development Tools
- **Package Manager**: npm/yarn/pnpm
- **Linting**: ESLint + Next.js config
- **Type Checking**: TypeScript strict mode
- **Version Control**: Git/GitHub

## 🚀 Getting Started

### Prerequisites

```bash
# Node.js 18+ and npm
node --version  # Should be 18.0.0 or higher
npm --version
```

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/dripcity/CLAIMSHIELD.git
cd CLAIMSHIELD
```

2. **Install dependencies**

```bash
npm install
# or
yarn install
# or
pnpm install
```

3. **Set up environment variables**

Create a `.env.local` file in the root directory:

```env
# Firebase Configuration
NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_auth_domain
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_storage_bucket
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id

# OpenAI Configuration
OPENAI_API_KEY=your_openai_api_key

# App Configuration
NEXT_PUBLIC_APP_URL=http://localhost:3000
NEXT_PUBLIC_API_URL=http://localhost:3000/api
```

4. **Run the development server**

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 📁 Project Structure

```
CLAIMSHIELD/
├── app/                      # Next.js 14 App Router
│   ├── (auth)/              # Authentication routes
│   ├── (dashboard)/         # Protected dashboard routes
│   ├── api/                 # API routes
│   ├── layout.tsx           # Root layout
│   └── page.tsx             # Landing page
├── components/              # React components
│   ├── ui/                  # shadcn/ui components
│   ├── forms/               # Form components
│   ├── dashboard/           # Dashboard components
│   └── appraisal/          # Appraisal-specific components
├── lib/                     # Utility functions
│   ├── firebase/            # Firebase configuration
│   ├── openai/              # OpenAI integration
│   ├── utils/               # Helper functions
│   └── validations/         # Zod schemas
├── types/                   # TypeScript type definitions
├── public/                  # Static assets
├── styles/                  # Global styles
└── config/                  # App configuration
```

## 🎯 Core Functionality

### 1. Vehicle Information Input
- VIN decoder integration
- Make/Model/Year selection
- Mileage and condition assessment
- Accident date and details

### 2. Damage Assessment
- Structural damage evaluation
- Repair cost documentation
- Photo upload and analysis
- Severity classification

### 3. Market Analysis
- Comparable vehicle research
- Regional market trends
- Historical data analysis
- Depreciation modeling

### 4. Report Generation
- AI-powered narrative creation
- Professional formatting
- Supporting documentation compilation
- PDF export with branding

### 5. Claim Filing Support
- Insurance company database
- Claim form auto-population
- Email templates and demand letters
- Follow-up reminders

## 🔧 Configuration Files

### TypeScript Configuration (`tsconfig.json`)

Strict type checking with path aliases for clean imports.

### Next.js Configuration (`next.config.js`)

Optimized for production with image optimization and API routes.

### Tailwind Configuration (`tailwind.config.ts`)

Custom design system with extended colors, animations, and utilities.

### ESLint Configuration (`.eslintrc.json`)

Next.js recommended rules with TypeScript support.

## 📚 API Documentation

### Appraisal Endpoints

```typescript
// POST /api/appraisal/calculate
// Calculate diminished value for a vehicle

// POST /api/appraisal/generate-report
// Generate PDF appraisal report

// GET /api/appraisal/:id
// Retrieve existing appraisal
```

### Vehicle Data Endpoints

```typescript
// POST /api/vehicle/decode-vin
// Decode VIN and return vehicle details

// GET /api/vehicle/market-data
// Fetch comparable vehicle listings
```

### User Management

```typescript
// GET /api/user/profile
// Get user profile

// PUT /api/user/profile
// Update user profile

// GET /api/user/appraisals
// List user's appraisals
```

## 🧪 Testing

```bash
# Type checking
npm run type-check

# Linting
npm run lint

# Build test
npm run build
```

## 🚢 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Import project in Vercel
3. Configure environment variables
4. Deploy

```bash
npm run build
npm run start
```

### Other Platforms

Compatible with any Node.js hosting platform:
- Netlify
- AWS Amplify
- Railway
- Render
- DigitalOcean App Platform

## 🔒 Security Considerations

- Never commit `.env.local` or API keys
- Use environment variables for all secrets
- Implement rate limiting on API routes
- Validate all user inputs with Zod
- Sanitize data before database operations
- Use Firebase Security Rules
- Enable CORS only for trusted domains

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Nicky V** (dripcity)
- GitHub: [@dripcity](https://github.com/dripcity)

## 🙏 Acknowledgments

- Vehicle market data providers
- Insurance industry experts
- Open source community
- AI/ML research community

## 📞 Support

For questions, issues, or feature requests:
- Open an issue on GitHub
- Check existing documentation
- Review closed issues for solutions

## 🗺️ Roadmap

- [ ] Multi-language support
- [ ] Mobile app (React Native)
- [ ] Advanced analytics dashboard
- [ ] API for third-party integrations
- [ ] Bulk appraisal processing
- [ ] Live chat support
- [ ] Video damage assessment
- [ ] Blockchain-based report verification

---

**Made with ❤️ for vehicle owners seeking fair compensation**
