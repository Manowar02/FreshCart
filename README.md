# 🛒 FreshCart - Full-Stack E-Commerce Platform

FreshCart is a modern, responsive, full-stack online grocery & fresh produce e-commerce application built with the **MERN** stack (MongoDB, Express, React, Node.js), Vite, Tailwind CSS v4, Cloudinary, and Stripe integration.

🌐 **Live Demo**: [https://freshcart-ashy-nine.vercel.app/](https://freshcart-ashy-nine.vercel.app/)
---

## 🚀 Features

### 👤 Customer Features
- **User Authentication**: Secure Signup, Login, and Logout using JWT tokens stored in HTTP-only cookies.
- **Product Browsing**: Filter products by category, search by product name, and view detailed product information.
- **Shopping Cart**: Add, update quantity, or remove items with real-time total price calculation.
- **Address Management**: Save and manage delivery addresses for fast checkout.
- **Flexible Payments**: Support for online payments powered by **Stripe** and **Cash on Delivery (COD)**.
- **Order Management**: Track past orders and view detailed order status updates.

### 🏬 Seller / Admin Dashboard
- **Seller Authentication**: Dedicated secure access for platform sellers.
- **Product Management**: Upload new products with multiple images powered by **Cloudinary**, set prices, categories, and descriptions.
- **Product Catalog**: Manage active inventory and remove products.
- **Order Processing**: View incoming customer orders and update shipping/delivery statuses in real-time.

---

## 🛠️ Tech Stack

### **Frontend (`/client`)**
- **Framework**: React 19 + Vite
- **Routing**: React Router DOM (v7)
- **Styling**: Tailwind CSS v4
- **HTTP Client**: Axios
- **Notifications**: React Hot Toast

### **Backend (`/server`)**
- **Runtime**: Node.js
- **Framework**: Express.js (v5)
- **Database**: MongoDB Atlas with Mongoose ORM
- **Authentication**: JSON Web Token (JWT) & Cookie Parser
- **File Storage**: Cloudinary & Multer
- **Payments**: Stripe Node SDK & Webhooks

---
### Deployment
- Frontend: Vercel
- Backend: Vercel
- Database: MongoDB Atlas
- Image Storage: Cloudinary

---

## 📸 Screenshots
<img width="959" height="472" alt="image" src="https://github.com/user-attachments/assets/2a32c948-f44e-4e79-a8a1-d9672074524b" />
<img width="959" height="475" alt="image" src="https://github.com/user-attachments/assets/5cb8d2b2-722c-4143-9e32-3fc4a7ddb76e" />
<img width="959" height="473" alt="image" src="https://github.com/user-attachments/assets/0de29dcf-5406-45cc-90cb-7fcb6a6b7bfb" />
<img width="959" height="473" alt="image" src="https://github.com/user-attachments/assets/37ca5ae2-82ee-4ab4-a0f2-9c13ef5aad4f" />
<img width="959" height="434" alt="image" src="https://github.com/user-attachments/assets/d0974a75-9e28-4018-8c5c-94beac0e11bb" />
<img width="959" height="470" alt="image" src="https://github.com/user-attachments/assets/d4897816-a701-49d1-9450-4722d704d0be" />
<img width="959" height="473" alt="image" src="https://github.com/user-attachments/assets/c86ce37f-1d63-4b1f-8d9e-71429349ffce" />






---

## 📂 Project Structure

```
FreshCart/
├── client/                 # React Frontend
│   ├── public/             # Static assets
│   ├── src/
│   │   ├── assets/         # Icons, logos, static images
│   │   ├── components/     # UI components (Navbar, Footer, ProductCard, etc.)
│   │   ├── context/        # React Context API (AppContext)
│   │   ├── pages/          # Application pages & Seller dashboard pages
│   │   ├── App.jsx         # Main App Routing
│   │   └── main.jsx        # App entry point
│   ├── vercel.json         # Vercel deployment configuration
│   ├── vite.config.js      # Vite build configuration
│   └── package.json
│
├── server/                 # Express Backend API
│   ├── configs/            # DB & Cloudinary connection setup
│   ├── controllers/        # Request handlers (User, Product, Cart, Order, Seller)
│   ├── middleware/         # Auth & Multer middlewares
│   ├── models/             # Mongoose schemas (User, Product, Order, Address)
│   ├── routes/             # API Endpoint routes
│   ├── server.js           # Express app entry point & Stripe webhooks
│   ├── vercel.json         # Serverless API deployment configuration
│   └── package.json
└── README.md
```
## 📡 API Endpoints Summary

| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/api/user/register` | POST | Register a new user |
| `/api/user/login` | POST | Login user & issue JWT cookie |
| `/api/user/logout` | POST | Logout user |
| `/api/user/is-auth` | GET | Verify user authentication state |
| `/api/seller/login` | POST | Seller authentication login |
| `/api/product/list` | GET | Fetch all active products |
| `/api/product/add` | POST | Add product with image upload (Seller) |
| `/api/cart/get` | GET | Get user cart items |
| `/api/cart/update` | POST | Update cart quantity |
| `/api/address/add` | POST | Save user shipping address |
| `/api/order/cod` | POST | Place Cash on Delivery order |
| `/api/order/stripe` | POST | Create Stripe Checkout payment session |
| `/api/order/user` | GET | Fetch user order history |
| `/api/order/seller` | GET | Fetch all customer orders (Seller) |
| `/stripe` | POST | Stripe Webhook handler |
---
