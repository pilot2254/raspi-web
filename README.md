# Raspberry Pi Web Hosting Template

A simple template for hosting websites locally on Raspberry Pi, accessible from other devices on your network.

## Features

- Plain HTML/CSS website
- Vite development server
- Network-accessible configuration
- Lightweight and fast

## Quick Setup

### 1. Clone and Install
```bash
git clone https://github.com/pilot2254/raspi-web.git
cd raspi-web
npm install
```

### 2. Start Development Server
```bash
npm run dev
```

### 3. Access from Network
- Find your Pi's IP: `hostname -I`
- Access from any device: `http://[PI_IP_ADDRESS]:5173`

## Configuration

The template is pre-configured to accept connections from all network interfaces:

- **Development**: `npm run dev` (port 5173)
- **Production preview**: `npm run preview` (port 4173)
- **Build**: `npm run build`

## Network Access

The `vite.config.js` and `package.json` are configured with:
- `host: '0.0.0.0'` - Binds to all network interfaces
- Default ports: 5173 (dev), 4173 (preview)

## Customization

1. Edit `index.html` for your content
2. Modify `style.css` for styling
3. Add assets to the project root
4. Update `package.json` name and details

## Production Deployment

For production use:
```bash
npm run build
npm run preview
```

Or serve the `dist` folder with any static file server.

## Requirements

- Node.js 16+
- Raspberry Pi with network connection
- Devices on same network for access

## License

MIT License - see LICENSE file for details.

Enjoy!
