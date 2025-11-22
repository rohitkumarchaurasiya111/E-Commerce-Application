# E-Commerce Application

A full-stack e-commerce web application with a Java-based backend and a JavaScript-based frontend.  
This project is organized into two main modules:

- `E-Commerce_Backend` – RESTful API for authentication, products, cart, orders, etc.
- `E-Commerce_Frontend` – Web client for customers to browse products and place orders.

## Features

### Customer Features

- Browse list of products with details (price, description, image, etc.)
- Search and filter products (e.g., by category or name)
- Add/remove items from the cart
- Update item quantity in the cart
- Place an order from the cart

### Admin / Store Management (optional / if implemented)

- Add new products
- Update existing products
- Delete products
- View list of all orders

---

## Project Structure

```text
E-Commerce-Application/
├── E-Commerce_Backend/    # Java backend source code
└── E-Commerce_Frontend/   # JavaScript frontend source code
```

Each folder is an independent project with its own dependencies and configuration.

---

## Tech Stack

**Backend**

- Java
- RESTful APIs (Spring Boot)
- JPA / ORM and relational database (MySQL) for persistence
- JSON for data exchange with the frontend

**Frontend**

- JavaScript (with HTML & CSS)
- A modern JS library (React) for building UI components
- Axios for calling backend APIs

---

## Getting Started

### Prerequisites

- **Java** (JDK 21 or later)
- **npm** (for the frontend)
- **Database** (MySQL) running locally or in the cloud

Make sure you have the above installed and properly configured on your system.

---

## Backend Setup (`E-Commerce_Backend`)

1. Open the `E-Commerce_Backend` folder in your IDE (IntelliJ, Eclipse, VS Code, etc.)  
2. Configure the database connection inside your backend configuration file (`application.properties`):
   - Database URL
   - Username
   - Password
3. Create the database schema in your DB server.
4. Build and run the backend:
   - You can run it directly from your IDE, **or**
   - Use your project build tool (Maven) from the terminal.

Once the backend starts successfully, it should expose REST APIs on a port like `http://localhost:8080`.

---

## Frontend Setup (`E-Commerce_Frontend`)

1. Open a terminal and navigate to the frontend folder:

   ```bash
   cd E-Commerce_Frontend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server (command may differ depending on your setup):

   ```bash
   npm run dev
   ```

4. Open the browser and go to the URL shown in your terminal  
   (usually `http://localhost:3000` or `http://localhost:5173`).

Make sure the backend is running so that the frontend can successfully call the APIs.

---

## Environment Configuration

Typical values you may need to configure:

### Backend

- Server port (e.g., `server.port=8080`)
- Database properties (URL, username, password)
- CORS configuration to allow calls from the frontend origin (e.g., `http://localhost:3000` or `http://localhost:5173`)

### Frontend

- API base URL pointing to the backend, for example:

  ```js
  const API_BASE_URL = "http://localhost:8080/api";
  ```
---

## API Endpoints (Example)

- `GET /api/products` – Get all products
- `GET /api/products/{id}` – Get product details by ID
- `POST /api/cart` – Add item to cart
- `GET /api/cart` – Get items in current user’s cart
- `PUT /api/cart/{itemId}` – Update quantity of a cart item
- `DELETE /api/cart/{itemId}` – Remove item from cart
- `POST /api/orders` – Place order
- `GET /api/orders` – Get current user’s orders
---

## Possible Improvements

- Add proper form validation and error handling in the UI
- Add role-based access control (customer vs admin)
- Integrate a real payment gateway (e.g., Razorpay, Stripe)
- Improve UI with better design and responsiveness
- Add unit tests and integration tests for critical flows
- Dockerize the application for easy deployment

---

## Contributing

1. Fork the repository
2. Create a new branch for your feature or bugfix:

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. Commit your changes and push the branch
4. Open a pull request with a clear description of the changes

---

## License

This project is currently for learning and demonstration purposes.  

---

## Author

**Rohit Kumar Chaurasia**

- GitHub: [@rohitkumarchaurasiya111](https://github.com/rohitkumarchaurasiya111)
