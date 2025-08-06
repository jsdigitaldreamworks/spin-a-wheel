# Replit.md

## Overview

This is a React-based web application for a promotional spin-the-wheel contest. Users can register with their information and spin a virtual wheel to win various prizes and discount codes. The application features a registration form, an interactive spinning wheel component, and email notifications for both users and administrators when prizes are won.

The system is now configured for **static deployment** with client-side storage and EmailJS integration. It includes a complete user flow from registration to prize redemption, with special handling for "Try Again" results that show failure messages instead of prize notifications.

## Recent Changes (January 2025)

✅ **Fixed "Try Again" Logic** - Now shows "Better Luck Next Time!" message with no prize
✅ **Static Deployment Ready** - Converted to client-side localStorage instead of database
✅ **Updated EmailJS** - Using latest SDK version (v4) to fix deprecated version errors
✅ **Perfect Wheel Alignment** - Rebuilt with SVG for mathematically precise 11 equal segments
✅ **Accessibility Fixed** - Added DialogTitle and DialogDescription for screen readers
✅ **Clockwise Text Positioning** - Text properly rotated and aligned in each segment

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript for type safety and better development experience
- **UI Framework**: Shadcn/ui components built on Radix UI primitives for consistent, accessible interface components
- **Styling**: Tailwind CSS for utility-first styling with custom CSS variables for theming
- **State Management**: React Query (TanStack Query) for server state management and caching
- **Form Handling**: React Hook Form with Zod validation for type-safe form validation
- **Routing**: Wouter for lightweight client-side routing
- **Build Tool**: Vite for fast development and optimized production builds

### Storage Architecture
- **Client-Side Storage**: localStorage-based storage for static deployment
- **Data Persistence**: User registrations stored in browser localStorage
- **Validation**: Client-side input validation using Zod schemas
- **Spin Tracking**: Prevents multiple spins per user through localStorage state
- **Fallback Support**: Express.js backend available for development with in-memory storage

### Database Design
- **Primary Table**: `registrations` table storing user information, prize details, and spin status
- **Schema**: Uses Drizzle schema definitions with Zod validation for data integrity
- **Database Provider**: Configured for PostgreSQL with Neon Database serverless connection

### Authentication & Security
- **Validation**: Server-side input validation using Zod schemas
- **Email Verification**: Prevents duplicate registrations by checking existing email addresses
- **Data Sanitization**: Form inputs are validated and sanitized before database storage

### Email Integration
- **Service**: EmailJS for client-side email sending without backend email server requirements
- **Templates**: Separate email templates for user notifications and admin notifications
- **Content**: Dynamic email content including user details, prize information, and promotional codes

### Prize System
- **Prize Pool**: Predefined list of prizes with corresponding discount codes
- **Distribution**: Random prize selection with weighted probability
- **Tracking**: Database tracking of won prizes and spin status to prevent multiple spins per user

### Development Features
- **Hot Reload**: Vite development server with fast refresh for rapid development
- **Type Safety**: Full TypeScript implementation across frontend and backend
- **Code Organization**: Modular component structure with shared utilities and types
- **Error Boundaries**: Client-side error handling with user-friendly error displays

## External Dependencies

### Database Services
- **Neon Database**: Serverless PostgreSQL database hosting
- **Connection**: Uses `@neondatabase/serverless` driver for database connectivity

### Email Services
- **EmailJS**: Client-side email service for sending notifications
- **Service ID**: `service_72b961n`
- **Templates**: 
  - User template: `template_3k7ehvr`
  - Admin template: `template_hflosex`
- **Public Key**: `jp6NMnw0T-NYE40fy`

### UI Component Libraries
- **Radix UI**: Comprehensive set of low-level UI primitives for accessibility
- **Shadcn/ui**: Pre-built component library built on top of Radix UI
- **Lucide React**: Icon library for consistent iconography

### Development Tools
- **Drizzle Kit**: Database migration and schema management tool
- **ESBuild**: Fast JavaScript bundler for production builds
- **PostCSS**: CSS processing with Tailwind CSS integration

### External Links
- **Privacy Policy**: https://www.jsdigitaldreamworks.ca/privacy-policy
- **Terms & Conditions**: https://www.jsdigitaldreamworks.ca/terms-and-conditions
- **Contact**: https://www.jsdigitaldreamworks.ca/contact-us

### Company Information
- **Brand**: JS Digital DreamWorks
- **Contact Email**: Referenced in email templates for customer support