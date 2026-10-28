# foodpass
# 🍔 FoodPass – Pay, Scan, Eat

Order at the counter, pay with GPay/UPI or card, and get a **one-time encrypted QR ticket**. When the food is served, the vendor scans the QR (or taps "Mark served") and the ticket becomes invalid.

## Features
- Customer: menu by category, cart, payment (Razorpay test-style flow), QR tickets
- Vendor: scan/paste/manual serve, order details, monthly & yearly accounts (GST, gateway fees, net payout), transaction ledger
- AES-256-GCM encrypted QR payloads, SHA-256 transaction hashes
- Helper chatbot, feedback (review / suggestion / complaint), Snack Smash mini-game
- 3D cartoon UI in white, black, green, gold and blue

## Run
Open `index.html` in a browser, or enable GitHub Pages (Settings → Pages → `main` / root).

Demo vendor PIN: `1234`

## Status: prototype
- Payments are **simulated**. Real Razorpay needs a backend to create orders and verify signatures.
- Data is stored in the browser (`localStorage`), so customer and vendor views only share data on one device.
- The encryption key is stored in the browser. In production keep it on the server.

## Roadmap
- [ ] Node/Express backend with Razorpay order creation + signature verification
- [ ] Database (orders, menu, vendors)
- [ ] Server-side QR signing/validation
- [ ] Claude-powered helper via backend API
- [ ] Real vendor authentication

## Security
Never commit Razorpay key secrets or encryption keys. Use environment variables (`.env`, already git-ignored).