# Juniors Automotive & Tire - Backend

Backend API and server for Juniors Automotive & Tire. Built with Node.js with zero external dependencies.

## Requirements

- Node.js 18 or newer

## Getting Started

Start the server:

```bash
ADMIN_PASSWORD=your-secure-password node server.js
```

Or run via npm:

```bash
npm start
```

Default endpoints:
- Server: `http://localhost:3000`
- Admin Login / Panel: `http://localhost:3000/admin`
- API routes: `http://localhost:3000/api/*`

If `ADMIN_PASSWORD` is omitted on first run, a random temporary password will be generated and printed to the console.

## Environment Variables

- `PORT`: Port to listen on (default `3000`)
- `ADMIN_PASSWORD`: Admin password for staff authentication
- `COOKIE_SECURE`: Set to `1` when running behind HTTPS
- `TRUST_PROXY`: Set to `1` if behind a reverse proxy (e.g. Caddy, NGINX, Cloudflare)

## API Endpoints

- `GET /api/site`: Fetch published tires and business details
- `GET /api/me`: Check admin session status
- `POST /api/login`: Staff login
- `POST /api/logout`: Staff logout
- `POST /api/orders`: Submit customer order
- `PUT /api/products`: Update tire catalog (Admin only)
- `PUT /api/business`: Update business information (Admin only)
- `POST /api/upload`: Upload tire images (Admin only)
- `GET /api/orders`: Retrieve orders (Admin only)
- `DELETE /api/orders/:id`: Delete order (Admin only)

## Data Storage

Persistent data is stored in the `data/` folder:
- `products.json`
- `business.json`
- `orders.json`
- `uploads/`
