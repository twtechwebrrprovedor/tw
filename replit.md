# TechWeb Internet Provider - Replit MD

## Overview

This is a full-stack web application for TechWeb, an internet service provider (ISP) offering fiber optic internet plans. The application serves as a marketing website and customer interface, built with modern web technologies including React, Node.js/Express, and PostgreSQL with Drizzle ORM.

## User Preferences

Preferred communication style: Simple, everyday language.
Preferred language: Portuguese (Brazilian)
Visual preferences: Authentic app colors and icons for social media integration

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for development and production builds
- **UI Framework**: Shadcn/ui components with Radix UI primitives
- **Styling**: Tailwind CSS with custom design system
- **Routing**: Wouter for client-side routing
- **State Management**: TanStack Query for server state management
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with TypeScript
- **Framework**: Express.js for REST API
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Session Management**: Connect-pg-simple for PostgreSQL session storage
- **Development**: ESBuild for production bundling, TSX for development

### Build and Development
- **Monorepo Structure**: Client, server, and shared code in separate directories
- **Development Server**: Custom Vite setup with Express middleware integration
- **Hot Module Replacement**: Enabled for React components during development
- **TypeScript**: Strict configuration with path aliases

## Key Components

### Client Structure
- **Pages**: Index (landing page), NotFound (404 page)
- **Components**: 
  - Header with navigation and logo
  - HeroSection with main value proposition
  - PlansSection displaying internet plans
  - BenefitsSection highlighting service advantages
  - ContactSection with contact information
  - Footer with company details
  - WhatsAppButton for direct customer contact
- **UI Components**: Complete Shadcn/ui component library
- **Styling**: Custom Tech Web brand colors (blue, purple, red) with dark theme

### Server Structure
- **Routes**: Centralized route registration in `routes.ts`
- **Storage**: Interface-based storage layer with in-memory implementation
- **Development**: Vite integration for serving React app
- **Logging**: Custom request logging middleware

### Shared Components
- **Schema**: Drizzle schema definitions with Zod validation
- **Types**: Shared TypeScript types between client and server

### Database Schema
- **Users Table**: Basic user structure with id, username, and password fields
- **Migrations**: Drizzle-kit for database migrations
- **Connection**: Neon Database serverless PostgreSQL

## Data Flow

1. **Client Requests**: React app makes API calls using TanStack Query
2. **API Routes**: Express server handles requests at `/api` endpoints
3. **Storage Layer**: Interface-based storage operations (currently in-memory)
4. **Database Operations**: Drizzle ORM handles PostgreSQL interactions
5. **Response Handling**: JSON responses with error handling middleware

## External Dependencies

### Core Technologies
- **React Ecosystem**: React 18, React DOM, React Hook Form
- **UI Libraries**: Radix UI components, Lucide React icons
- **Development Tools**: Vite, TypeScript, ESBuild
- **Database**: Neon Database, Drizzle ORM, PostgreSQL drivers
- **Styling**: Tailwind CSS, PostCSS, Autoprefixer

### Business Integrations
- **WhatsApp Business**: Direct integration for customer communication
- **Replit Platform**: Development environment optimizations

### Asset Management
- **Images**: Logo assets and background images stored in client/src/assets
- **Public Assets**: Robots.txt and other static files

## Deployment Strategy

### Development
- **Local Development**: `npm run dev` starts both Express server and Vite dev server
- **Hot Reloading**: Enabled for both client and server code
- **Environment**: NODE_ENV=development with TSX for TypeScript execution

### Production
- **Build Process**: Two-step build with Vite for client and ESBuild for server
- **Client Build**: Static files generated to `dist/public`
- **Server Build**: Bundled Node.js application in `dist/index.js`
- **Start Command**: `npm start` runs production build

### Database
- **Migrations**: `npm run db:push` applies schema changes
- **Environment Variables**: DATABASE_URL required for database connection
- **Serverless**: Neon Database provides serverless PostgreSQL

### Platform Considerations
- **Replit Integration**: Special handling for Replit environment
- **Error Handling**: Runtime error overlay for development
- **Static Assets**: Served through Express in production

The application follows modern web development practices with a clear separation of concerns, type safety throughout the stack, and a responsive design optimized for the Brazilian internet service provider market.

## Recent Changes (January 31, 2025)

### Social Media Integration Improvements
- **Authentic App Icons**: Integrated react-icons library for official social media icons
  - WhatsApp: FaWhatsapp with official green color (#25D366)
  - Instagram: FaInstagram with authentic gradient (purple/pink/red)
  - Gmail: SiGmail with official red color
  - Google Maps: SiGooglemaps with official blue color

### UI/UX Enhancements
- **Floating Buttons Position**: Adjusted floating social media buttons to bottom-24 to prevent footer overlap
- **Footer Layout**: Added lateral padding (px-20) to copyright and menu items for mobile compatibility
- **Contact Section**: Enhanced with proper Google Maps and agenda icons for address and business hours
- **Button Variants**: Updated button styles with authentic app colors and gradients

### Technical Updates
- **Dependencies**: Added react-icons package for comprehensive icon library
- **Component Updates**: Updated WhatsAppButton, InstagramButton, ContactSection, and Footer components
- **Styling**: Improved gradient implementation for Instagram branding