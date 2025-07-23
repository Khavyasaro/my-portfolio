# Portfolio Web Application

## Overview

This is a full-stack portfolio web application built with React, Express, and PostgreSQL. The application showcases an AI engineer's portfolio with a modern, responsive design featuring smooth animations and interactive components. It includes a contact form for visitors to send messages and demonstrates proficiency in AI technologies like machine learning, computer vision, and voice AI.

## System Architecture

The application follows a modern full-stack architecture with clear separation between frontend and backend:

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Framework**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **Animations**: Framer Motion for smooth transitions and interactions
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack React Query for server state management
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database ORM**: Drizzle ORM for type-safe database operations
- **Database**: PostgreSQL (configured for Neon serverless)
- **Session Management**: Built-in storage abstraction with memory fallback
- **API Design**: RESTful API with JSON responses

## Key Components

### Frontend Components
- **Navigation**: Fixed header with smooth scroll navigation
- **Hero Section**: Landing area with animated introduction
- **About Section**: Skills showcase with animated cards
- **Contact Section**: Interactive form with real-time validation
- **Footer**: Social links and professional information

### Backend Components
- **Routes**: Contact form submission and message retrieval endpoints
- **Storage Layer**: Abstracted storage interface supporting both memory and database implementations
- **Middleware**: Request logging, error handling, and static file serving
- **Development Tools**: Vite integration for hot module replacement

### Database Schema
- **Users Table**: Basic user authentication structure (prepared for future use)
- **Contact Messages Table**: Stores form submissions with timestamps
- **Type Safety**: Full TypeScript integration with Drizzle ORM schemas

## Data Flow

1. **Contact Form Submission**:
   - User fills out contact form on frontend
   - Form data validated using Zod schemas
   - POST request sent to `/api/contact` endpoint
   - Backend validates and stores message in database
   - Success/error response returned to frontend
   - Toast notification displayed to user

2. **Message Retrieval**:
   - Admin can access messages via GET `/api/contact`
   - Backend queries database and returns all messages
   - Future enhancement: Add authentication for admin access

3. **Static Content**:
   - Portfolio content served statically
   - Smooth scroll navigation between sections
   - Responsive design adapts to mobile/desktop

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Neon PostgreSQL connection
- **drizzle-orm**: Type-safe ORM with PostgreSQL dialect
- **@tanstack/react-query**: Server state management
- **framer-motion**: Animation library
- **@radix-ui/***: Accessible UI primitives
- **zod**: Schema validation
- **react-hook-form**: Form management

### Development Dependencies
- **tsx**: TypeScript execution for development
- **esbuild**: Production bundling
- **tailwindcss**: Utility-first CSS framework
- **@replit/vite-plugin-***: Replit-specific development tools

### UI Component System
- Complete shadcn/ui component library
- Consistent design tokens via CSS variables
- Dark/light mode support (infrastructure ready)
- Accessible by default with Radix UI primitives

## Deployment Strategy

### Development Environment
- **Runtime**: Node.js 20 with Replit modules
- **Database**: PostgreSQL 16 module
- **Development Server**: Vite dev server with HMR
- **Port Configuration**: Application runs on port 5000

### Production Build
- **Frontend**: Vite builds optimized static assets to `dist/public`
- **Backend**: esbuild bundles server code to `dist/index.js`
- **Deployment Target**: Autoscale deployment on Replit
- **Environment**: Production environment variables for database connection

### Database Management
- **Schema**: Managed via Drizzle migrations in `./migrations`
- **Configuration**: Database URL required via environment variable
- **Push Command**: `npm run db:push` for schema updates

## Changelog

Changelog:
- June 24, 2025. Initial setup
- June 24, 2025. Enhanced with creative design flourishes, micro-interactions, and animations
- June 24, 2025. Added project modals, certificates section, email notifications, and layout refinements
- July 11, 2025. Enabled resume download functionality with Khavya's AI Engineer resume PDF

## User Preferences

Preferred communication style: Simple, everyday language.