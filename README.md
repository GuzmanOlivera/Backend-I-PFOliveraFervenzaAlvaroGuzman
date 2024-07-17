# SurtidoCompleto

This project is a web application for managing products and shopping carts, utilizing Node.js, Express, MongoDB with mongoose and mongoose-paginate-v2 for efficient database operations, Socket.IO for real-time communication, Handlebars for templating, and dotenv for environment variable management.

The name "SurtidoCompleto" reflects the idea of providing a complete assortment or full range of products, emphasizing comprehensive and extensive offerings within the project.

## Features

Product management: add, update, delete, and list products.
Cart management: create carts, add products to carts, and view cart details.
Real-time product management with Socket.IO for live updates.
User-friendly interface with Handlebars templates and Bootstrap styling.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/GuzmanOlivera/PFOliveraFervenzaAlvaroGuzman.git
   ```

2. Navigate to the project directory:

   ```bash
   cd PFOliveraFervenzaAlvaroGuzman
   ```

3. Install the dependencies:

   ```bash
   npm install
   ```

4. Start the server:

   ```bash
   npm run dev
   ```

# Endpoints

## Products

- `GET /api/products`: Get the list of products.
- `GET /api/products/:pid`: Get a product by its ID.
- `POST /api/products`: Add a new product.
- `PUT /api/products/:pid`: Update an existing product.
- `DELETE /api/products/:pid`: Delete a product.

## Carts

- `POST /api/carts`: Create a new cart.
- `GET /api/carts/:cid`: Get a cart by its ID.
- `POST /api/carts/:cid/products/:pid`: Add a product to the cart.
- `PUT /api/carts/:cid/products/:pid`: Update a product in the cart.
- `DELETE /api/carts/:cid/products/:pid`: Remove a product from the cart.


# Project Structure

- `.env`: Environment variables for connecting MongoDB database.
- `src/app.js`: Main application and server configuration.
- `src/config/database.js`: MongoDB database connection and configuration.
- `src/dao/db/cart-manager.js`: Cart management logic.
- `src/dao/db/product-manager.js`: Product management logic.
- `src/dao/models/cart.model.js`: Cart model.
- `src/dao/models/product.model.js`: Product model.
- `src/routes/products.router.js`: Routes for product management.
- `src/routes/carts.router.js`: Routes for cart management.
- `src/routes/views.router.js`: Routes for application views.
- `src/public/js/main.js`: Client-side logic for real-time interaction.
- `src/public/css/style.css`: Custom application styles.
- `src/views/layouts/main.handlebars`: Main layout for views.
- `src/views/cartDetail.handlebars`: View for Cart Details.
- `src/views/home.handlebars`: Main view for the product list.
- `src/views/realTimeProducts.handlebars`: View for real-time product management.

### Notes

This project uses MongoDB for data storage and retrieval. Ensure that you have MongoDB configured. Additionally, it is needed to create a .env file in the root directory of the project, following the structure outlined in .env.example, to set up environment variables for connecting to MongoDB.