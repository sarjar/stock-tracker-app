# Stocks App

A modern web application for stock market analysis and trading signals.

## Tech Stack

- **Framework**: Next.js 15.6 with Turbopack
- **Language**: TypeScript
- **Authentication**: Better Auth
- **Database**: MongoDB with Mongoose
- **Background Jobs**: Inngest
- **AI Integration**: Google Gemini
- **Form Management**: React Hook Form
- **Styling**: 
  - Tailwind CSS
  - shadcn/ui
  - Class Variance Authority

## Project Structure

```
stocks-app/
├── app/                    # Next.js 15 app directory
│   ├── (auth)/            # Authentication routes
│   │   ├── sign-in/       # Sign in page
│   │   └── sign-up/       # Sign up page
│   ├── (root)/            # Root routes
│   │   └── stocks/        # Stock-related pages
│   ├── api/               # API routes
│   │   └── inngest/       # Inngest webhooks
│   ├── globals.css        # Global styles
│   └── layout.tsx         # Root layout
├── components/            
│   ├── forms/             # Form components
│   └── ui/                # Shadcn UI components
├── database/              # MongoDB configuration
│   ├── mongoose.ts        # Mongoose connection
│   └── models/            # MongoDB models
├── hooks/                 # Custom React hooks
├── lib/                   
│   ├── actions/           # Server actions
│   ├── better-auth/       # Auth configuration
│   ├── inngest/          # Inngest setup
│   └── utils/            # Utility functions
├── middleware/           # Next.js middleware
├── public/               # Static assets
└── types/               # TypeScript type definitions

```

## Environment Setup

Create a `.env` file with:

```env
# Database
MONGODB_URI="your-mongodb-uri"

# Better Auth
AUTH_SECRET="your-auth-secret"

# Inngest
INNGEST_EVENT_KEY="your-event-key"
INNGEST_BASE_URL="https://api.inngest.com"

# AI
GEMINI_API_KEY="your-gemini-key"

# Email
SMTP_USER="your-smtp-username"
SMTP_PASSWORD="your-smtp-password"
SMTP_HOST="your-smtp-host"
SMTP_PORT="587"
```

## Development

```bash
# Install dependencies
npm install

# Start development server with Turbopack
npm run dev
```

## Scripts

```json
{
  "dev": "next dev --turbopack",
  "build": "next build --turbopack",
  "start": "next start",
  "lint": "eslint"
}
```

## Features

- 🔐 Authentication with Better Auth
- 📊 Real-time stock data visualization with TradingView
- 🤖 AI-powered market analysis with Gemini
- 📈 Trading signals and watchlists
- 🔄 Background jobs with Inngest
- � Email notifications with Nodemailer
- �📱 Responsive design with shadcn/ui
- 🎨 Modern UI with Tailwind CSS and shadcn/ui
- 🌍 Country selection support

## Architecture

- **App Router**: Leverages Next.js 15 server components
- **Server Actions**: For form handling and data mutations
- **API Routes**: RESTful endpoints and Inngest webhooks
- **Middleware**: Auth protection and request handling
- **Database**: MongoDB with Mongoose models
- **Components**: shadcn/ui (built on Radix UI primitives)

## Dependencies

### Core
- next: ^15.5.4
- react: ^19.1.0
- mongodb: ^6.20.0
- mongoose: ^8.19.1
- better-auth: ^1.3.27
- inngest: ^3.44.3
- nodemailer: ^7.0.9

### UI & Forms
- shadcn/ui components with Radix UI primitives
- react-hook-form: ^7.64.0
- class-variance-authority: ^0.7.1
- lucide-react: ^0.545.0
- sonner: ^2.0.7
- tailwind-merge: ^3.3.1
- cmdk: ^1.1.1

### Development
- typescript: ^5
- tailwindcss: ^4
- eslint: ^9
- @types/* packages
