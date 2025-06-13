[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19777139&assignment_repo_type=AssignmentRepo)
# Express.js RESTful API Assignment

This assignment focuses on building a RESTful API using Express.js, implementing proper routing, middleware, and error handling.

## Assignment Overview

You will:
1. Set up an Express.js server
2. Create RESTful API routes for a product resource
3. Implement custom middleware for logging, authentication, and validation
4. Add comprehensive error handling
5. Develop advanced features like filtering, pagination, and search

## Getting Started

1. Accept the GitHub Classroom assignment invitation
2. Clone your personal repository that was created by GitHub Classroom
3. Install dependencies:
   ```
   npm install
   ```
4. Run the server:
   ```
   npm start
   ```

## Files Included

- `Week2-Assignment.md`: Detailed assignment instructions
- `server.js`: Starter Express.js server file
- `.env.example`: Example environment variables file

## Requirements

- Node.js (v18 or higher)
- npm or yarn
- Postman, Insomnia, or curl for API testing

## API Endpoints

The API will have the following endpoints:

- `GET /api/products`: Get all products
- `GET /api/products/:id`: Get a specific product
- `POST /api/products`: Create a new product
- `PUT /api/products/:id`: Update a product
- `DELETE /api/products/:id`: Delete a product

## Submission

Your work will be automatically submitted when you push to your GitHub Classroom repository. Make sure to:

1. Complete all the required API endpoints
2. Implement the middleware and error handling
3. Document your API in the README.md
4. Include examples of requests and responses

## Resources

- [Express.js Documentation](https://expressjs.com/)
- [RESTful API Design Best Practices](https://restfulapi.net/)
- [HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) 


# 🚀 Product API – Week 2 Assignment

A simple RESTful API built using Express.js that allows CRUD operations on a list of products, with middleware, error handling, and advanced features like filtering, search, and pagination.

---

## 📦 Setup & Installation

1. Clone the repository :

   ```bash
   git clone https://github.com/PLP-MERN-Stack-Development/week-2-express-js-assignment-nfvic.git
   cd week-2-express-js-assignment-nfvic.git
   
2. Install the dependencies using pnpm:

   ```bash
   pnpm install
   ```

3. Start the server:

   ```bash
   node server.js
   ```

---

## 🔐 Authentication

All API requests require an API key in the headers:

```
x-api-key: 123456
```

---

## 📁 Environment Variables

Create a `.env` file (optional for now), but the structure should match:

```
PORT=3000
API_KEY=123456
```

> You don't need dotenv yet, but include this if you decide to use environment variables later.

---

## 📚 API Endpoints

### GET `/`

* Welcome message

---

### GET `/api/products`

* Returns a list of products

#### Optional Query Parameters:

* `category=electronics` – filter by category
* `search=phone` – search name or description
* `page=1&limit=5` – pagination

#### Example:

```bash
curl -H "x-api-key: 123456" http://localhost:3000/api/products?category=electronics&page=1&limit=2
```

---

### GET `/api/products/:id`

* Returns a single product by ID

---

### POST `/api/products`

* Creates a new product

#### Request body:

```json
{
  "name": "Blender",
  "description": "500W high-speed blender",
  "price": 99.99,
  "category": "kitchen",
  "inStock": true
}
```

---

### PUT `/api/products/:id`

* Updates an existing product by ID

---

### DELETE `/api/products/:id`

* Deletes a product by ID

---

### GET `/api/products/stats`

* Returns statistics:

  * Total products
  * In-stock / Out-of-stock count
  * Product count by category
  * Average price

---

## 🧪 Testing

Use tools like [Postman](https://www.postman.com/), [Insomnia](https://insomnia.rest/), or `curl`:

Example:

```bash
curl -H "x-api-key: 123456" http://localhost:3000/api/products
```

---

## 📁 File Structure

```
├── server.js
├── .env.example
├── README.md
├── package.json
```

---

## ✅ Features Implemented

* [x] Express.js setup
* [x] Full RESTful CRUD routes
* [x] Custom middleware:
  * Logger
  * Auth
  * JSON parser
  * Input validation
* [x] Error handling with global handler
* [x] Filtering, pagination, search
* [x] Statistics endpoint
