🛒 E-Commerce API
Welcome to the E-Commerce API, a powerful and scalable backend built with Node.js and Express.js, designed to handle user authentication, product management, and cart functionalities efficiently. This project leverages MongoDB as the database and JWT for secure authentication.

🚀 Features
✅ User Authentication (Register & Login)
✅ Product Management (CRUD Operations)
✅ Cart Functionality (Add, Get, Update, Remove Items)
✅ Secure Authentication with JWT Middleware
✅ Modern Tech Stack: Node.js, Express.js, MongoDB, Mongoose

🛠 Tech Stack
Backend: Node.js, Express.js

Database: MongoDB, Mongoose
Authentication: JWT, bcrypt.js

📌 Installation Guide
1️⃣ Clone the Repository
git clone https://github.com/dhimansaurabh43/shoppyBackend.git

2️⃣ Install Dependencies
npm install

3️⃣ Create a .env File
touch .env
Inside .env, add the following:
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<dbname>?retryWrites=true&w=majority
JWT_SECRET=your_jwt_secret_key
PORT=3000

4️⃣ Start the Server
npm run dev   # Using nodemon for live reload
# or
node server.js
🔗 API Endpoints
🔐 User Authentication
➤ Register User
Endpoint: POST /api/register
{
  "username": "dhimanSaurabh",
  "email": "Saurabhdhiman66@example.com",
  "password": "monsterclub"
}
➤ Login User
Endpoint: POST /api/login
{
  "email": "Saurabhdhiman66@example.com",
  "password": "monsterclub"
}

🛍️ Product Management
➤ Get All Products
Endpoint: GET /api/products
➤ Get Product by ID
Endpoint: GET /api/product/:id
➤ Create a Product
Endpoint: POST /api/product
{
  "name": "Product Name",
  "price": 99.99,
  "description": "Product description"
}
➤ Update a Product
Endpoint: PUT /api/product/:id
{
  "price": 89.99
}
➤ Delete a Product
Endpoint: DELETE /api/product/:id
🛒 Cart Management
➤ Add Item to Cart
Endpoint: POST /api/cart
{
  "productId": "12345",
  "quantity": 2
}
➤ Get User Cart
Endpoint: GET /api/cart
➤ Update Cart Item
Endpoint: PUT /api/cart/:id
{
  "quantity": 3
}
➤ Remove Item from Cart
Endpoint: DELETE /api/cart/:id
🔒 Middleware
authMiddleware.js - Protects routes using JWT authentication.
