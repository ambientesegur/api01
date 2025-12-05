# Kit Natal Cacau Show 2025 - Checkout Page

## Overview
This is a checkout page for a Brazilian Christmas chocolate kit promotion ("Kit Natal Cacau Show 2025"). The page includes a Node.js backend server that integrates with the BlackCat Pagamentos PIX API for payment processing.

## Project Structure
- `index.html` - Main checkout page with embedded styles and scripts
- `server.js` - Node.js/Express backend server for PIX API integration
- `package.json` - Node.js dependencies

## Features
- Responsive checkout form with Brazilian address fields (CEP, CPF)
- BlackCat Pagamentos PIX payment integration
- Two shipping options with different pricing:
  - Normal delivery (free): R$ 83.20 total
  - Fast delivery (+R$ 19.90): R$ 103.10 total
- Address auto-fill via CEP lookup (ViaCEP API)
- Countdown timers for offer and PIX code expiration
- Automatic payment status checking
- QR Code generation for PIX payments
- Animated snowflake background
- UTM parameter tracking
- Location detection

## Technologies
- Node.js with Express
- HTML5, Tailwind CSS (via CDN), Vanilla JavaScript
- QRCode.js library
- BlackCat Pagamentos API for PIX payments
- ViaCEP API for address lookup

## Environment Variables (Secrets)
- `BLACKCAT_PUBLIC_KEY` - BlackCat Pagamentos public API key
- `BLACKCAT_SECRET_KEY` - BlackCat Pagamentos secret API key

## API Endpoints
- `POST /api/create-pix` - Create a new PIX payment transaction
- `POST /api/check-status` - Check payment status by transaction ID

## Configuration
- Backend served on port 5000
- Deployment configured as autoscale

## Recent Changes
- December 05, 2025: Initial import and setup for Replit environment
- December 05, 2025: Integrated BlackCat Pagamentos PIX API
- Added Node.js backend server for secure API key handling
- Implemented different amounts for normal/fast shipping
- Added automatic payment status polling
