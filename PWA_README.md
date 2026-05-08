# POS & Inventory Management System - PWA Updates

This app has been updated to work as a Progressive Web App (PWA) with offline functionality and install capability.

## What's Been Added

### 1. Web App Manifest (`manifest.json`)
- Defines app metadata for installation
- Includes app icons, theme colors, and display mode

### 2. Service Worker (`sw.js`)
- Caches static assets for offline use
- Handles fetch requests with cache-first strategy
- Enables background sync capabilities

### 3. Firebase Offline Persistence
- Added `database.enablePersistence()` to enable offline data storage
- Data will sync when connection is restored

### 4. Install Prompt
- Added install button that appears when app can be installed
- Handles the `beforeinstallprompt` event
- Shows install prompt when user clicks install

### 5. Offline Notification
- Shows notification when app goes offline
- Hides when back online

## What You Need to Do

### Create App Icons
You need to create and add the following icon files:

1. `icon-192.png` - 192x192 pixel PNG icon
2. `icon-512.png` - 512x512 pixel PNG icon

You can generate these icons using:
- [PWA Builder](https://www.pwabuilder.com/)
- [Real Favicon Generator](https://realfavicongenerator.net/)
- Or any icon generation tool

### Testing
1. Serve the app over HTTPS (required for PWA features)
2. Test offline functionality by going offline in dev tools
3. Test install prompt on supported browsers (Chrome, Edge, etc.)
4. Verify data persists when offline and syncs when online

### Browser Support
- Service Workers: Chrome 40+, Firefox 44+, Safari 11.1+, Edge 17+
- Web App Manifest: Chrome 38+, Firefox 41+, Safari 11.3+, Edge 17+
- Install Prompt: Chrome 68+, Edge 79+

## How Offline Works

1. **Caching**: Static assets (HTML, CSS, JS, images) are cached
2. **Firebase Persistence**: Data is stored locally when offline
3. **Sync**: Data automatically syncs when connection is restored
4. **Fallback**: App shows cached version when offline

## Install Process

1. App detects if it can be installed
2. Install button appears in navigation
3. User clicks install, browser shows install prompt
4. User can add to home screen or desktop

The app is now a fully functional PWA that works offline and can be installed!