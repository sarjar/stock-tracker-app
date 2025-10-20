# Stocks App

A modern web application for stock market analysis and trading signals.

## Tech Stack

- **Framework**: Next.js 15.6 with App Router
- **Language**: TypeScript
- **Authentication**: NextAuth.js
- **Database**: PostgreSQL with Prisma ORM
- **State Management**: React Context
- **Background Jobs**: Inngest
- **AI Integration**: Google Gemini
- **Styling**: 
  - Tailwind CSS
  - Shadcn/ui
  - CSS Modules

## Project Structure

```
stocks-app/
├── app/                    # Next.js 15 app directory
│   ├── (auth)/            # Authentication routes
│   ├── (dashboard)/       # Protected dashboard routes
│   ├── api/               # API routes
│   └── layout.tsx         # Root layout
├── components/            
│   ├── forms/             # Form components
│   ├── layouts/           # Layout components
│   └── ui/                # UI components
├── lib/                   
│   ├── actions/           # Server actions
│   ├── auth/              # Auth configuration
│   ├── inngest/           # Inngest setup
│   ├── prisma/            # Database client
│   └── utils/             # Utility functions
├── prisma/
│   └── schema.prisma      # Database schema
├── public/                # Static assets
├── styles/                # Global styles
├── types/                 # TypeScript types
└── middleware.ts          # Next.js middleware

```

## Environment Setup

Create a `.env` file with:

```env
# Database
DATABASE_URL="postgresql://..."

# Authentication
NEXTAUTH_SECRET="your-secret"
NEXTAUTH_URL="http://localhost:3000"

# Inngest
INNGEST_EVENT_KEY="your-event-key"
INNGEST_BASE_URL="https://api.inngest.com"

# AI
GEMINI_API_KEY="your-gemini-key"
```

## Development

```bash
# Install dependencies
npm install

# Generate Prisma client
npx prisma generate

# Run database migrations
npx prisma migrate dev

# Start development server
npm run dev
```

## Scripts

```json
{
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint",
  "test": "jest",
  "prisma:studio": "prisma studio"
}
```

## Features

- 🔐 Authentication with NextAuth.js
- 📊 Real-time stock data visualization
- 🤖 AI-powered market analysis
- 📈 Trading signals generation
- 🔄 Background jobs with Inngest
- 📱 Responsive design
- 🎨 Theme customization

## Architecture

- **App Router**: Leverages Next.js 15 server components
- **Server Actions**: For form handling and data mutations
- **API Routes**: RESTful endpoints for external integrations
- **Middleware**: Auth protection and request handling
- **Database**: Prisma schema with PostgreSQL
