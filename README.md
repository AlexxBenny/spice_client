# 🌶️ Spice Client: E-Commerce Platform for Spices

**Spice Client** is a robust, full-featured e-commerce web application designed specifically for selling spices and culinary products. Built with **Flask**, it offers a seamless shopping experience for customers and a powerful management interface for administrators.

![Python](https://img.shields.io/badge/Python-3.11%2B-blue)
![Flask](https://img.shields.io/badge/Framework-Flask-green)
![Status](https://img.shields.io/badge/Status-Active-success)

---

## 🔥 Features

### For Customers
*   **Product Browsing**: Browse spices by category with filtering and search capabilities.
*   **User Accounts**: Secure registration, login, and profile management.
*   **Shopping Cart & Checkout**: Add items, manage cart, and process orders (simulated payment flow).
*   **Wishlist**: Save favorite items for later.
*   **Order History**: View past orders and status.
*   **Address Management**: Save multiple shipping and billing addresses.

### For Administrators
*   **Product Management**: Create, edit, and delete products (manage stock, prices, images).
*   **Category Management**: Organize products into categories (e.g., Whole Spices, Ground Spices, Blends).
*   **Order Management**: View and update order statuses (Pending, Shipped, Delivered).
*   **User Management**: a view of registered users.

---

## 🛠️ Tech Stack

*   **Backend**: Python, Flask
*   **Database**: PostgreSQL (Production) / SQLite (Dev), SQLAlchemy ORM
*   **Authentication**: Flask-Login
*   **Forms**: Flask-WTF
*   **Frontend**: Jinja2 Templates, Bootstrap 5 (or similar CSS framework from `static/`)
*   **Utilities**: `python-dotenv` for config, `werkzeug` for security.

---

## 📂 Project Structure

```
spice_client/
├── app.py              # Application entry point and configuration
├── models.py           # Database models (User, Product, Order, etc.)
├── forms.py            # WTForms definitions for validation
├── extensions.py       # Flask extensions setup (DB, LoginManager)
├── routes/             # Blueprints for application logic
│   ├── auth.py         # Authentication routes
│   ├── main.py         # Public facing pages (Home, Cart)
│   ├── products.py     # Product listing and details
│   └── admin.py        # Admin dashboard routes
├── templates/          # HTML Templates
├── static/             # CSS, JS, Images
└── requirements.txt    # Project dependencies
```

---

## 🚀 Getting Started

Follow these steps to set up the spice shop locally.

### Prerequisites
*   Python 3.11+
*   Git

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/cyriac-pullan/spice_client.git
    cd spice_client
    ```

2.  **Create a Virtual Environment**
    ```bash
    # Windows
    python -m venv venv
    venv\Scripts\activate

    # macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Environment Setup**
    Create a `.env` file in the root directory:
    ```env
    SESSION_SECRET="your-secret-key"
    DATABASE_URL="sqlite:///spice.db"  # or your PostgreSQL URL
    ```

5.  **Initialize Database**
    The app is set up to create tables and sample data automatically on first run (check `app.py` logic).

6.  **Run the Server**
    ```bash
    python app.py
    ```
    Access the store at `http://127.0.0.1:5000`

---

## 📦 Database Schema

*   **Users**: Customer data, passwords, contact info.
*   **Products**: Name, description, price, stock, SKU.
*   **Categories**: Logical grouping for products.
*   **Orders**: Transaction records linking Users and Products.
*   **OrderItems**: Line items for each order.
*   **Addresses**: Shipping/Billing details.

---

## 🤝 Contributing

Contributions are welcome! Please fork the repo and submit a Pull Request.

---

## 👤 Author

**Cyriac Paul Pullan**
*   GitHub: [@cyriac-pullan](https://github.com/cyriac-pullan)
