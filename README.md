<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&size=30&duration=4000&pause=1000&color=F76C6C&center=true&vCenter=true&width=600&lines=%E2%98%95+Welcome+to+Caf%C3%A9+Aroma;Fresh+Brews+Delivered+to+Your+Door;Brewed+with+Love+%26+Pinch+of+Tech" alt="Café Aroma Animated Banner" />
</p>


Developed “Café Aroma”, a Django-based e-commerce site for a dine-in coffee shop. Features include custom user auth, product management, session-based cart, Razorpay payments, OTP verification, order tracking with admin updates, and SMTP-based contact form.


# ☕ Café Aroma – Your Ultimate Dine-In Coffee Experience

![Café Aroma Banner](https://i.ibb.co/fHkT0jQ/coffee-banner.gif)

> **Café Aroma** is a **full-stack Django web application** built to bring the cozy coffeehouse experience online.  
> Designed with a **beautiful UI**, **seamless UX**, and **robust backend** — this project blends technology and taste in perfect harmony.

---

## ✨ Features

### 👥 User Management
- **Registration** with validation for:
  - Name, Email, Phone, Address, City, Country
  - Secure password hashing
- **Login & Session Management** – Users stay logged in until they log out.
- **Profile Picture in Navbar** (rounded style).
- Automatic redirection:
  - If logged in → Profile Page
  - If not logged in → Login Page

---

### 🛒 Cart & Orders
- **Add to Cart** instantly when clicking “Order Now.”
- **View Cart**: All products in one place.
- **Session-based Cart** (No DB cart model — lightweight and fast).
- **Delete Items** from cart with SweetAlert confirmation.
- **Subtotal & Total Price Calculation**.
- **Razorpay Integration** for smooth, secure payments.

---

### 📦 Order Management
- Orders stored in DB linked to customers.
- Admin can **mark orders as Delivered** from the Django Admin Panel.
- Delivery status **auto-updates** in transaction history.

---

### 📸 Product Management
- Coffee items managed by **Admin Panel**:
  - Image
  - Title
  - Description
  - Price
- Fully dynamic — changes instantly reflect on the website.

---

### 📬 Contact & Support
- **SMTP Integration** – Customers can send messages via contact form.

---

## 🖥️ Tech Stack

| Layer        | Technologies Used |
|--------------|-------------------|
| **Frontend** | HTML5, CSS3, JavaScript, TailwindCSS, SweetAlert |
| **Backend**  | Python 3, Django (Template Language) |
| **Database** | SQLite |
| **Payments** | Razorpay |
| **Other**    | Django ORM, SMTP |

---

## 🏗️ Project Structure
