<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&size=30&duration=4000&pause=1000&color=F76C6C&center=true&vCenter=true&width=600&lines=%E2%98%95+Welcome+to+Caf%C3%A9+Aroma;Fresh+Brews+Delivered+to+Your+Door;Brewed+with+Love+%26+Pinch+of+Tech" alt="Café Aroma Animated Banner" />
</p>

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
| **Frontend** | HTML5, CSS3, JavaScript,SweetAlert |
| **Backend**  | Python , Django (Template Language) |
| **Database** | SQLite |
| **Payments** | Razorpay |
| **Other**    | Django ORM, SMTP |

---

## 🏗️ Project Structure
cafe_aroma/
│
├── authentication/ # Handles user login & registration
├── main/ # Products, cart, orders, payment
├── templates/ # HTML templates
├── static/ # CSS, JS, images
├── db.sqlite3
├── manage.py
└── README.md


---

## 🚀 Quick Start

###
1️⃣ Clone the Repository

<pre> git clone https://github.com/MrSamarjitBanerjee/CafeAroma.git
  cd cafe_aroma </pre>

2️⃣ Create Virtual Environment & Install Dependencies
<pre>
  python -m venv venv
  venv\Scripts\activate    # Windows
  source venv/bin/activate # Mac/Linux
</pre>


pip install -r requirements.txt

3️⃣ Apply Migrations
<pre>python manage.py migrate</pre>

4️⃣ Create Superuser
<pre> python manage.py createsuperuser </pre>

5️⃣ Run the Server
<pre>python manage.py runserver</pre>

Visit http://127.0.0.1:8000/

🖼️ Screenshots

<img width="955" height="445" alt="image" src="https://github.com/user-attachments/assets/4a34ce78-c50e-4707-97e2-9914dde733fd" />
<img width="959" height="448" alt="image" src="https://github.com/user-attachments/assets/a0bfbb21-6582-4b39-883f-2fbf26e7606d" />
<img width="955" height="431" alt="image" src="https://github.com/user-attachments/assets/c8306740-42e9-4f8d-b5e3-12083a174870" />
<img width="959" height="410" alt="image" src="https://github.com/user-attachments/assets/5c4f3adf-d261-4726-ace6-80bf4f3accaa" />



📚 Learning Outcomes
Session management in Django

Secure password handling

Payment gateway integration

Admin-based order tracking

SweetAlert for better UX

💡 Future Improvements
Add coupons & discounts

Implement order tracking for customers

Add product categories & search

👨‍💻 Author
Samarjit Banerjee
💌 Email Me
banerjeesamarjit9@gmail.com



⭐ If you like this project, give it a star on GitHub!




