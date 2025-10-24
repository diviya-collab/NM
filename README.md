PRODUCT CATALOG WITH MONGODB
A simple and scalable Product Catalog API built with Node.js, Express, and MongoDB.
This project demonstrates how to design, build, and manage a product database — ideal for e-commerce or inventory systems.

 Features:
 MongoDB Integration – Stores product data efficiently with Mongoose schemas.
 CRUD Operations – Create, Read, Update, and Delete products.
 Product Filtering – Filter products by category, price, rating, or availability.
 RESTful API – Clean and well-structured endpoints.
 Validation – Schema validation using Mongoose and Express middleware.
 Modular Codebase – Easy to extend and maintain.

Tech Stack
Layer	Technology
Backend	Node.js, Express.js
Database	MongoDB, Mongoose
Tools	Postman, dotenv, nodemon
Installation
1. Clone the repository
git clone https://github.com/your-username/product-catalog-mongodb.git
cd product-catalog-mongodb

2. Install dependencies
npm install

3. Setup environment variables
Create a .env file in the root directory and add:
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/productdb

4. Run the server
npm start

Server will start on http://localhost:5000

API Endpoints:
Method	Endpoint	Description
GET	/api/products	Get all products
GET	/api/products/:id	Get product by ID
POST	/api/products	Create a new product
PUT	/api/products/:id	Update a product
DELETE	/api/products/:id	Delete a product

Example Product Schema:
{
  "name": "Wireless Headphones",
  "price": 79.99,
  "category": "Electronics",
  "brand": "SoundX",
  "inStock": true,
  "description": "High-quality wireless headphones with noise cancellation."
}

Folder Structure:
product-catalog-mongodb/
│
├── src/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   └── productController.js
│   ├── models/
│   │   └── productModel.js
│   ├── routes/
│   │   └── productRoutes.js
│   └── server.js
│
├── .env
├── package.json
└── README.md

Example Request (POST):
curl -X POST http://localhost:5000/api/products \
-H "Content-Type: application/json" \
-d '{
  "name": "Smart Watch",
  "price": 149.99,
  "category": "Accessories",
  "brand": "TechPro",
  "inStock": true,
  "description": "Waterproof smart watch with heart rate monitor."
}'
Future Improvements:
Add user authentication (JWT)
Add reviews and ratings
Upload product images with Cloudinary
Implement pagination and search
