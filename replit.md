# IFRS Gap Analysis System

## Overview

This is a React-based application that performs automated gap analysis for IFRS sustainability reporting standards (S1 & S2). The system accepts document uploads, processes them using AI-powered analysis, and generates comprehensive compliance reports with export capabilities.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

The application follows a full-stack architecture with clear separation between frontend and backend concerns:

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **UI Library**: Radix UI components with shadcn/ui styling system
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Build Tool**: Vite for development and bundling

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Pattern**: RESTful API with file upload capabilities
- **File Processing**: Multer for multipart form handling
- **Document Processing**: PDF parsing with AI-powered text analysis

### Database & ORM
- **ORM**: Drizzle ORM with PostgreSQL dialect
- **Database**: PostgreSQL (configured for Neon serverless)
- **Migrations**: Drizzle Kit for schema management
- **Schema Location**: Shared between client and server (`shared/schema.ts`)

## Key Components

### Document Processing Pipeline
1. **File Upload**: Accepts 4 PDF documents (IFRS S1, IFRS S2, Industry Metrics, Annual Report)
2. **Text Extraction**: Uses pdf-parse library to extract text content
3. **AI Analysis**: OpenAI GPT-4o processes documents for compliance analysis
4. **Gap Analysis**: Compares requirements against actual disclosures
5. **Report Generation**: Creates structured results with recommendations

### AI Integration
- **Provider**: OpenAI API with GPT-4o model
- **Processing**: Structured JSON responses for requirement extraction and compliance analysis
- **Error Handling**: Comprehensive error handling for API failures and invalid responses

### Export System
- **Excel Export**: Uses ExcelJS for structured spreadsheet generation
- **PDF Export**: jsPDF with autotable plugin for formatted reports
- **Format Support**: Multiple export formats for different stakeholder needs

### UI Components
- **File Upload**: Drag-and-drop interface with validation
- **Processing Status**: Real-time progress tracking with visual indicators
- **Results Table**: Filterable and searchable compliance results
- **Export Controls**: Download buttons for different report formats

## Data Flow

1. **Upload Phase**: User uploads 4 required PDF documents through the web interface
2. **Processing Phase**: Backend extracts text, sends to OpenAI for analysis, stores results in database
3. **Display Phase**: Frontend polls for completion and displays results in interactive table
4. **Export Phase**: Users can download results in Excel or PDF format

### Storage Strategy
- **Development**: In-memory storage for rapid development and testing
- **Production**: PostgreSQL database with Drizzle ORM for persistence
- **File Handling**: Files are processed in memory without persistent storage

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: PostgreSQL connection for serverless environments
- **@tanstack/react-query**: Advanced server state management
- **@radix-ui/***: Accessible UI component primitives
- **drizzle-orm**: Type-safe database ORM
- **openai**: Official OpenAI API client

### Processing Libraries
- **pdf-parse**: PDF text extraction
- **multer**: File upload handling
- **exceljs**: Excel file generation
- **jspdf**: PDF report generation

### Development Tools
- **vite**: Fast development server and build tool
- **typescript**: Type safety across the stack
- **tailwindcss**: Utility-first CSS framework
- **zod**: Runtime type validation

## Deployment Strategy

### Development Environment
- **Server**: Node.js with tsx for TypeScript execution
- **Client**: Vite development server with HMR
- **Database**: Environment variable configuration for flexibility

### Production Build
- **Client**: Static assets built with Vite to `dist/public`
- **Server**: Bundled with esbuild to `dist/index.js`
- **Environment**: NODE_ENV-based configuration switching

### Environment Configuration
- **Database**: `DATABASE_URL` environment variable
- **AI Service**: `OPENAI_API_KEY` environment variable  
- **Session**: PostgreSQL session store for production scaling

### Replit Integration
- **Development**: Cartographer plugin for enhanced Replit experience
- **Error Handling**: Runtime error overlay for development debugging
- **Banner**: Replit development banner for external access

## Recent Changes

### July 21, 2025 - GitHub Production Release v1.0.0
- **Complete Security Implementation**: User-provided OpenAI API keys with validation preventing unauthorized server costs
- **API Integration Fixed**: Resolved API key transmission from frontend to backend for successful analysis
- **Production Testing**: Verified OpenAI integration with proper error handling for quota exceeded scenarios
- **GitHub Deployment Ready**: Comprehensive documentation, MIT license, and deployment guides for multiple platforms
- **Error Handling Enhanced**: User-friendly messages for API quota issues and billing problems
- **Next Phase Planned**: Simplified free version to be developed after GitHub deployment