# FishYourStyle

FishYourStyle is a streetwear shopping experience built with a focus on product discovery, visual identity, and the tools needed to manage a real store.

This was my first e-commerce project where I worked beyond the frontend. My earlier React store, Lucas, focused on the customer-facing interface; FishYourStyle gave me the opportunity to work with live data, orders, admin tools, analytics, and reporting.

**Live website:** [Explore FishYourStyle](https://fishyourstyle.vercel.app)

---

## The shopping experience

- Browse products, categories, and designs through a responsive storefront.
- View product images, options, prices, and stock availability.
- Save favorites, manage a cart, and place an order.
- Use the site in multiple languages and switch between light and dark modes.
- See loyalty progress in an account: after five delivered orders, an eligible customer can receive 8% off the product subtotal of their next order.

---

## Behind the store

- **Next.js, React, TypeScript, and Tailwind CSS** — the application, interactive interface, and responsive styling.
- **Firebase Authentication and Firestore** — accounts and live store data, including products and orders.
- **Cloudinary** — product image uploads and delivery, with image transformations for appropriate formats and sizes.
- **Google Analytics 4** — shopping events such as product views, cart additions, checkout starts, and purchases, after analytics consent.
- **Google Apps Script and Google Sheets** — scheduled order reporting for review and analysis.
- **Vercel** — deployment of the website.

The site also uses an animated 3D logo as part of its visual identity.

---

## Admin dashboard and order reporting

The admin dashboard supports product and order management, including product details, images, stock, and order status.

For reporting, a protected server endpoint exports order data. A Google Apps Script can fetch new data on a schedule and add it to two Sheets tabs: **Orders** and **OrderItems**. Stable row keys help avoid adding the same rows twice. The Sheets copy is useful for reviewing sales and analyzing order items; the application continues to manage its orders in Firestore.

The admin dashboard also provides CSV downloads when a manual export is needed.

---

## Performance, SEO, and security

- Used limits and more focused data requests as I learned how Firestore reads affect performance and cost.
- Used Cloudinary image delivery options and lazy loading where appropriate.
- Added page metadata and other SEO features to help public pages appear and look better when shared.
- Protected administrative actions on the server instead of relying only on what the browser displays.
- Kept the Sheets export endpoint separate from normal admin access and protected it with an export token.

---

## Project screenshots

### 01 — Homepage: Brand & 3D Logo

<!-- Add homepage screenshot here -->

### 02 — Shop: Products & Filters

<!-- Add shop screenshot here -->

### 03 — Product Details: Images, Options & Stock

<!-- Add product page screenshot here -->

### 04 — Light & Dark Modes

<!-- Add two screenshots of the same page in each mode here -->

### 05 — Cart & Checkout

<!-- Add cart and checkout screenshots here -->

### 06 — Account: Orders & Loyalty Progress

<!-- Add account screenshot here -->

### 07 — Favorites: Saved Products

<!-- Add favorites screenshot here -->

### 08 — Admin: Product & Stock Management

<!-- Add admin products screenshot here -->

### 09 — Admin: Orders & Status

<!-- Add admin orders screenshot here -->

### 10 — Reporting: CSV & Google Sheets

<!-- Add a screenshot of the CSV control and a Sheet with sample data here -->

### 11 — Mobile Experience

<!-- Add mobile screenshot here -->

---

## My contribution

I approached FishYourStyle as a step beyond my earlier frontend-only store. I worked on the customer experience and the systems around it: connecting the storefront to Firebase, developing admin workflows, working with product imagery, and adding analytics and reporting.

One part I'm especially proud of is the Google Sheets order workflow. It connects a protected export endpoint to Apps Script so order and item data can be organized for analysis without manually copying every order.

I also worked on the visual identity, including the animated 3D logo and light and dark modes, while continuing to improve the site's responsiveness, SEO, and performance.

---

## What I learned

- **Firebase and Firestore:** My first experience working with live product and order data, authentication, and the need to limit reads as a project grows.
- **Performance:** How query limits, image delivery, caching, and responsive design affect the experience and operating cost.
- **Admin workflows:** How product, stock, and order management support the customer-facing store.
- **Order reporting:** How Apps Script can connect a protected API to Google Sheets for scheduled analysis.
- **Analytics and SEO:** How to measure shopping activity with GA4 and prepare public pages for search and sharing.
- **Product development:** How to build a larger project in stages and keep improving it as new requirements appear.
