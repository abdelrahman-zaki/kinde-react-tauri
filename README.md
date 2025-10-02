# Kinde React Starter Kit + Tauri v1

This is an example project showing how to integrate the [Kinde React Starter Kit](https://github.com/kinde-starter-kits/react-starter-kit) with [Tauri v1](https://v1.tauri.app/).

It allows running the React app as a cross-platform desktop application using Tauri. Authentication is handled via the SDK.

- **Development mode**: runs on `http://localhost:3000`  
- **Build mode**: runs as a packaged desktop app, using `https://tauri.localhost` as the callback URL

## Setup

1. Clone this repo and install dependencies:

   ```bash
   npm install
   ```

2. Copy the example environment file and update values:

   ```bash
   cp .env.example .env
   ```

   Example:

   ```
   # Development
   VITE_KINDE_DOMAIN=https://your_subdomain.kinde.com
   VITE_KINDE_CLIENT_ID=your_kinde_client_id
   VITE_KINDE_REDIRECT_URL=http://localhost:3000
   VITE_KINDE_LOGOUT_URL=http://localhost:3000

   # Build
   # When building with Tauri, update redirect/logout URLs to:
   VITE_KINDE_REDIRECT_URL=https://tauri.localhost
   VITE_KINDE_LOGOUT_URL=https://tauri.localhost
   ```

3. Run in development:

   ```bash
   npx tauri dev
   ```

4. Build desktop app:

   ```bash
   npm run build          # generates ./dist
   npx tauri build        # packages the desktop app
   ```