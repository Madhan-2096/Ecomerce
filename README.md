# MERN E-Commerce Project 

![MERN Stack](https://img.shields.io/badge/MERN-Stack-green)
![License](https://img.shields.io/badge/License-MIT-blue)

This is a full-stack e-commerce web application built with the MERN (MongoDB, Express, React, Node.js) stack. It features a complete customer-facing storefront and a full-featured admin panel for managing products, orders, and users.


## Features

### Customer-Facing Storefront
* **User Authentication:** Secure sign-up and sign-in with JSON Web Tokens (JWT).
* **Product Browsing:** View all products with search and filtering capabilities.
* **Product Details:** View detailed information for a single product.
* **Shopping Cart:** Add, remove, and update item quantities in the cart.
* **Checkout Process:** A multi-step checkout process.
* **Payment Integration:** (e.g., Stripe/Razorpay) for processing payments.
* **User Profile:** View and update user information and order history.

### Admin Dashboard
* **Admin-Only Access:** Secure routes for administrators.
* **Product Management (CRUD):** Create, read, update, and delete products.
* **Order Management:** View and update the status of customer orders.
* **User Management:** View and manage all registered users.
* **Dashboard Analytics:** (Optional) View sales charts, user registrations, etc.

## Tech Stack

This project is built with the following technologies:

* **Frontend:**
    * [**React.js**](https://reactjs.org/): A JavaScript library for building user interfaces.
    * [**Redux Toolkit**](https://redux-toolkit.js.org/): For state management.
    * [**Tailwind CSS**](https://tailwindcss.com/): A utility-first CSS framework.
    * [**Vite**](https://vitejs.dev/): A fast frontend build tool.

* **Backend:**
    * [**Node.js**](https://nodejs.org/): A JavaScript runtime environment.
    * [**Express.js**](https://expressjs.com/): A web framework for Node.js.
    * [**MongoDB**](https://www.mongodb.com/): A NoSQL database.
    * [**Mongoose**](https://mongoosejs.com/): An ODM (Object Data Modeling) library for MongoDB.

* **Authentication:**
    * [**JWT (JSON Web Tokens)**](https://jwt.io/): For secure user authentication.

## Prerequisites

Before you begin, ensure you have the following installed:

* [Node.js](https://nodejs.org/en/download/) (LTS version recommended)
* [MongoDB](https://www.mongodb.com/try/download/community) (or a MongoDB Atlas cloud account)
* `npm` (Node Package Manager) or `yarn`

## Installation & Setup

Follow these steps to get your project running locally.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[YOUR_USERNAME]/[YOUR_REPO_NAME].git
    cd [YOUR_REPO_NAME]
    ```

2.  **Set up the Backend (Server):**

    * Navigate to the `server` directory:
        ```bash
        cd server
        ```
    * Install backend dependencies:
        ```bash
        npm install
        # or
        yarn install
        ```
    * Create a `.env` file in the `server` directory. Copy the contents of `.env.example` (if it exists) or add the following variables:
        ```env
        MONGO_URI=your_mongodb_connection_string
        JWT_SECRET=your_super_secret_key_for_jwt
        
        # Add any other required keys (e.g., Stripe Secret Key)
        STRIPE_SECRET_KEY=...
        ```

3.  **Set up the Frontend (Client):**

    * Navigate to the `client` directory from the root:
        ```bash
        cd ../client
        ```
    * Install frontend dependencies:
        ```bash
        npm install
        # or
        yarn install
        ```
    * Create a `.env` file in the `client` directory and add the following variable. This tells your React app where to find your backend API.
        ```env
        # The port should match the one your server is running on
        VITE_API_URL=http://localhost:5000 
        
        # Add any other required keys (e.g., Stripe Publishable Key)
        VITE_STRIPE_PUBLISHABLE_KEY=...
        ```

## Running the Application

1.  **Start the Backend Server:**
    * From the `server` directory:
        ```bash
        npm run dev
        ```
    * The server will typically start on `http://localhost:5000`.

2.  **Start the Frontend Client:**
    * From the `client` directory (in a separate terminal):
        ```bash
        npm run dev
        ```
    * The React app will start, usually on `http://localhost:5173`.

You can now open `http://localhost:5173` in your browser to see the application running.
