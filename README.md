# eCommerce Backend Project

## Description
A robust eCommerce backend developed using Spring Boot, designed to manage essential eCommerce features like user authentication, product management, shopping cart, wishlist, and order processing. This project ensures security, scalability, and seamless database interactions, making it a reliable foundation for online shopping platforms.

## Features

### User Management
- Secure user registration and login with JWT authentication.
- Role-based access control for admin and customers.

### Product Management
- Add, update, delete, and view products.
- Stock management and product search functionalities.

### Shopping Cart
- Add products to the cart, update quantities, and remove items.
- Automatic calculation of the total price.

### Wishlist
- Save favorite products for future purchases.
- Move items from wishlist to cart with ease.

### Order Processing
- Checkout functionality with detailed order history.
- Manage order statuses like Pending, Shipped, and Delivered.

## Tech Stack
- **Language**: Java
- **Framework**: Spring Boot
- **Database**: MySQL, H2
- **ORM**: Hibernate (JPA)
- **Build Tool**: Maven

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ecommerce-backend.git
   cd ecommerce-backend
   ```

2. Configure the database in `application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
   spring.datasource.username=sa
   spring.datasource.password=password
   ```

3. Build and run the application:
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```
   
4. Access the application at `http://localhost:8080`.

## API Endpoints

### User Authentication
- **POST /auth/register** - Register a new user.
- **POST /auth/login** - User login and token generation.

### Product Management
- **GET /products** - Fetch all products.
- **POST /products** - Add a new product (Admin only).
- **PUT /products/{id}** - Update product details (Admin only).
- **DELETE /products/{id}** - Delete a product (Admin only).

### Shopping Cart
- **POST /cart/add** - Add a product to the cart.
- **GET /cart/{userId}** - Fetch cart items for a user.
- **DELETE /cart/{cartItemId}** - Remove an item from the cart.

### Wishlist
- **POST /wishlist/add** - Add a product to the wishlist.
- **GET /wishlist/{userId}** - Fetch wishlist items for a user.

### Order Processing
- **POST /order/place** - Place a new order.
- **GET /order/{userId}** - Fetch order history for a user.

## Using Postman to Test APIs
You can use [Postman](https://www.postman.com/) to test all the available API endpoints. Import the provided API collection or manually test by sending requests to the specified endpoints.

## Additional Features
- **Auto DDL (Data Definition Language)**: The application uses Hibernate's auto DDL feature to automatically create and manage database tables based on entity definitions. Ensure the appropriate configurations are set in `application.properties`.

## Future Enhancements
- Add payment gateway integration.
- Implement product recommendations using AI/ML.
- Support multi-currency and multi-language features.
