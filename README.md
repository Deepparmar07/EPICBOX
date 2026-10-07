# EPICBOX — JSS NGO Website

EPICBOX is the web presence and service backend for the JSS NGO project. It provides information about the organisation, its projects and events, and gives visitors ways to donate, volunteer, and get in touch.

**Live website:** [jssngo.netlify.app](https://jssngo.netlify.app/)

## Features

- Organisation, projects, events, photos, and videos pages
- Online donation flow with Razorpay integration
- Volunteer registration and contact forms
- Email notifications through the backend service
- Responsive pages for desktop and mobile visitors

## Technology

- HTML, CSS, and JavaScript
- Node.js and Express
- MongoDB with Mongoose
- Razorpay for payments
- Nodemailer for email delivery

## Project structure

- HTML files — public website pages
- CSS files — page and component styling
- custom.js and email.js — client-side interactions and form helpers
- server.js — Express backend entry point
- testConnection.js and test-email.js — local service checks

## Getting started

### Prerequisites

- Node.js 14 or newer
- npm
- A MongoDB connection for database-backed features
- Payment and email provider credentials for production functionality

### Install and run

    npm install
    npm start

For development with automatic restarts:

    npm run dev

Open the local address shown by the server in your browser.

## Environment configuration

Create a local .env file for the credentials required by the backend. Keep secrets out of Git, and configure the MongoDB, Razorpay, email, and server settings using the variable names expected by server.js.

## Contributing

1. Create a feature branch.
2. Make and test your changes locally.
3. Submit a pull request with a clear description of the change.

## Authors

Deep Solanki, Jenil Sarvani, and Deep Parmar
