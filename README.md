# EPICBOX

> A secure, modern cloud-storage platform for uploading, organising, and managing files from one place.

![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-5%2B-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5%2B-646CFF?style=flat-square&logo=vite&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-Database%20%26%20Auth-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![License](https://img.shields.io/badge/license-not%20declared-lightgrey?style=flat-square)

## Overview

EPICBOX is a full-featured cloud-storage web application built for reliable file management. It provides an authenticated workspace where users can upload files, browse stored content, filter by type, and manage digital assets through a responsive interface.

The project combines a React frontend with Supabase services and optional object-storage integrations. The repository also includes implementation guides for storage, encryption, authentication, presentations, and deployment.

**Live application:** [epicbox.vercel.app](https://epicbox.vercel.app/)

## Core capabilities

### File management

- Upload and manage files from a central dashboard
- Browse files with type-aware filtering and organised views
- Support common document, image, video, and archive workflows
- Display file metadata and storage information
- Provide loading, empty, error, and success states for user actions

### Identity and access

- User authentication and account management
- Protected application routes and authenticated data access
- Session-aware frontend state
- Supabase-backed authentication and database services
- Password reset and account recovery flows where configured

### Storage and data

- Supabase database integration for application data
- Cloud object-storage support for scalable file handling
- Encryption-related implementation guidance
- Storage configuration and migration documentation
- Clear separation between public client configuration and private secrets

### Product experience

- Responsive dashboard for desktop and mobile
- Reusable React components and shared UI primitives
- Consistent notifications and user feedback
- File-type filtering and focused browsing workflows
- Documentation for demonstrations, presentations, and user onboarding

## Architecture

EPICBOX is a Vite-powered React and TypeScript application with the following layers:

- Application layer — route composition, page rendering, and global app state
- UI layer — reusable components, layouts, forms, dialogs, and feedback states
- Data layer — Supabase queries, authentication, storage services, and API helpers
- Validation layer — typed models and form validation where applicable
- Styling layer — Tailwind CSS utilities, global styles, and responsive design tokens

## Project structure

- src/App.tsx — application shell and top-level routing
- src/main.tsx — frontend bootstrap
- src/pages — route-level screens and user workflows
- src/components — reusable interface components
- src/layout — shared page and dashboard layouts
- src/context — shared application state and providers
- src/services — database, authentication, and storage integrations
- src/db — database-related configuration and helpers
- src/hooks — reusable React hooks
- src/lib — shared utilities and client helpers
- src/types — shared TypeScript types
- public — static assets and public resources
- supabase — database configuration and migrations where present
- docs — product, storage, security, and workflow documentation

## Technology stack

### Frontend

- React 18 and TypeScript
- Vite and React Router
- Tailwind CSS and Radix UI primitives
- React Hook Form and Zod
- React Dropzone for upload interactions
- Axios and Ky for HTTP requests
- Lucide React for icons
- Recharts for data visualisation where used

### Platform services

- Supabase for authentication, database, and configured storage services
- AWS S3 SDK for supported object-storage workflows
- Vercel-compatible frontend deployment

## Requirements

- Node.js 20 or newer
- npm 10 or newer
- A Supabase project for connected authentication and data features
- Supabase URL and public anonymous key
- Object-storage credentials only when an external storage integration is enabled

## Getting started

### 1. Install dependencies

    git clone https://github.com/Deepparmar07/EPICBOX.git
    cd EPICBOX
    npm install

### 2. Configure the environment

Create a local .env file using .env.example as a reference. Add the public client configuration required by the application and provider configuration for enabled services.

Never commit private keys, service-role keys, database passwords, or cloud-storage secrets.

### 3. Start development

    npm run dev

Vite will print the local development URL in the terminal.

### 4. Build and preview

    npm run build
    npm run preview

## Available scripts

| Command | Description |
| --- | --- |
| npm run dev | Start the Vite development server |
| npm run build | Build the application for production |
| npm run preview | Preview the production build locally |
| npm run lint | Run repository lint and validation checks |

## Environment and security

- Use separate Supabase projects or credentials for development, staging, and production.
- Expose only browser-safe public configuration to the frontend.
- Keep service-role keys and cloud credentials on trusted server-side infrastructure.
- Apply least-privilege policies to database tables and storage buckets.
- Validate file types, file sizes, and user permissions before accepting uploads.
- Do not expose signed URLs longer than required.
- Review the encryption and storage guides before enabling production uploads.
- Rotate compromised credentials immediately and remove secrets from Git history.

## Deployment checklist

Before releasing to production:

- Configure environment variables in the hosting platform.
- Confirm Supabase authentication redirect URLs and site URL.
- Apply database schema and storage policies.
- Configure storage buckets, file-size limits, and allowed MIME types.
- Verify protected routes and row-level security policies.
- Test registration, login, password reset, upload, filtering, download, and logout flows.
- Run the production build and inspect the generated output.
- Configure monitoring, backups, error reporting, and a rollback procedure.
- Confirm no secrets, local environment files, or test credentials are committed.

## Documentation

The repository includes guides covering cloud storage, encryption, Supabase setup, file-type filtering, loading and presentation workflows, user guidance, and deployment planning. See the Markdown files in the repository root and docs directory.

## Contributing

1. Create a focused feature branch.
2. Keep changes scoped and follow existing project patterns.
3. Update related documentation when behavior or configuration changes.
4. Run the relevant lint, build, and manual workflow checks.
5. Do not commit secrets or real user data.
6. Open a pull request with a clear summary, testing notes, and screenshots for UI changes.

## License

This project does not currently declare a license. Add an explicit license file before distributing or reusing the software outside the project.
