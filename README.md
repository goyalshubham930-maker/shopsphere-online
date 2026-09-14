# ShopSphere Online Marketplace

A full-stack marketplace based on the original ShopSphere frontend. Buyers and sellers use the same online application. Sellers can publish products and receive buyer orders; each seller gets their own shipment status for multi-seller carts.

## Stack
- Node.js + Express
- PostgreSQL
- JWT authentication + bcrypt password hashing
- Multer image uploads
- Responsive HTML/CSS/JavaScript frontend

## Local setup
1. Install Node.js LTS and PostgreSQL.
2. Create a PostgreSQL database named `shopsphere`.
3. Copy `.env.example` to `.env` and set `DATABASE_URL` and a strong `JWT_SECRET`.
4. Run `npm install`.
5. Run `npm start`.
6. Open http://localhost:3000
7. Seller portal: http://localhost:3000/seller.html

The database tables are created automatically on first start.

## Online deployment
Push this folder to GitHub. Create a managed PostgreSQL database (for example Supabase or another PostgreSQL provider), then create a Node web service (for example Render). Set these environment variables in the host:
- DATABASE_URL
- JWT_SECRET
- NODE_ENV=production
- PORT (the host normally provides this automatically)

Build command: `npm install`
Start command: `npm start`

For production, move product images from local `public/uploads` to persistent/object storage and add a real payment gateway, email/SMS notifications, HTTPS, rate limiting, admin moderation and backups before accepting real payments.
