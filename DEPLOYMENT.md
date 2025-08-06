# Static Deployment Guide

This spin-the-wheel application is now configured for static deployment to platforms like Netlify, Vercel, or GitHub Pages.

## Features for Static Deployment

✅ **Client-side storage** - Uses localStorage instead of database
✅ **EmailJS integration** - Sends emails directly from browser
✅ **No backend required** - Completely self-contained frontend
✅ **Responsive design** - Works on all devices

## Building for Static Deployment

```bash
# Build the static version
npm run build

# The built files will be in dist/public/
# Upload this folder to your static hosting provider
```

## Configuration

### EmailJS Setup
The app uses EmailJS for sending emails. Make sure your EmailJS account is configured with:

- **Service ID**: `service_72b961n`
- **User Template ID**: `template_3k7ehvr` 
- **Admin Template ID**: `template_hflosex`
- **Public Key**: `jp6NMnw0T-NYE40fy`

### Template Variables
Make sure your EmailJS templates include these variables:
- `{{to_email}}` - recipient email
- `{{user_name}}` - full name
- `{{first_name}}` - first name
- `{{prize_title}}` - the prize won
- `{{prize_code}}` - coupon code
- `{{contact_email}}` - your contact email
- `{{company_name}}` - JS Digital DreamWorks

## Deployment Platforms

### Netlify
1. Upload `dist/public/` folder
2. Set build command: `npm run build`
3. Set publish directory: `dist/public`

### Vercel
1. Upload `dist/public/` folder
2. Set build command: `npm run build`
3. Set output directory: `dist/public`

### GitHub Pages
1. Push `dist/public/` contents to `gh-pages` branch
2. Enable GitHub Pages in repository settings

## Data Storage

User registrations are stored in browser localStorage. Each user can only spin once per browser/device. Data persists until browser cache is cleared.

## Testing Locally

```bash
# Start development server
npm run dev

# Build and preview static version
npm run build
npx vite preview --outDir dist/public
```