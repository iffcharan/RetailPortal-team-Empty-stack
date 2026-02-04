# RetailPortal-team-Empty-stack
A modular Retail / E-Commerce Portal built using the MERN stack architecture, with a decoupled frontend and backend.
The project is structured to support user shopping, admin management, orders, payments, analytics, and scalable integrations.
``` text
mern-ecommerce/
│
├── backend/                # Node.js + Express backend
│   ├── server.js
│   ├── routes/
│   ├── lib/
│   ├── config/
│   └── ...
│
├── frontend/               # React + Vite frontend
│   ├── src/
│   │   ├── api/
│   │   │   └── api.js
│   │   ├── products/
│   │   │   └── ProductHome.jsx
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── ...
│
├── db.json                 # Mock backend (json-server)
├── .env                    # Environment variables (not committed)
└── README.md
```
## ✨ Current Features (Implemented)
### ✅ Frontend

Product Home Page

Product listing using mock REST API

Responsive UI with Bootstrap

Clean component-based architecture

Centralized API configuration

### ✅ Mock Backend

Products endpoint using json-server

Realistic REST API behavior (GET /products)

🛠️ Features in Progress / Planned

User authentication (JWT)

Admin dashboard

Product CRUD (Admin)

Cart & checkout

Orders & order history

Payments (Stripe)

Analytics

Redis caching

Deployment (Vercel / Render)

### ⚙️ Setup Instructions
### 1️⃣ Clone the Repository
git clone https://github.com/iffcharan/RetailPortal-team-Empty-stack.git
cd mern-ecommerce

### 2️⃣ Backend Setup
cd backend
npm install


Create a .env file in the project root:

PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/retaildb
NODE_ENV=development
CLIENT_URL=http://localhost:5173


Run backend:

npm run dev


Backend runs on:

http://localhost:5000

### 3️⃣ Frontend Setup
cd frontend
npm install
npm run dev


Frontend runs on:

http://localhost:5173

### 4️⃣ Mock Backend Setup (Required for Frontend)

Create db.json in the project root:
```
{
  "products": [
    { "id": 1, "name": "Laptop", "price": 60000, "image": "https://via.placeholder.com/300" },
    { "id": 2, "name": "Headphones", "price": 2000, "image": "https://via.placeholder.com/300" },
    { "id": 3, "name": "Shoes", "price": 3500, "image": "https://via.placeholder.com/300" }
  ]
}
```

### Start mock API:

npx json-server --watch db.json --port 4000


### Mock API endpoint:

http://localhost:4000/products

### 🔌 API Configuration
frontend/src/api/api.js
import axios from "axios";
```
const api = axios.create({
  baseURL: "http://localhost:4000",
  headers: {
    "Content-Type": "application/json",
  },
});
```
export default api;


Switching to real backend later only requires changing baseURL.

### 🧠 Development Approach

Frontend and backend are decoupled

UI developed first using mock APIs

Backend integration planned after UI stabilization

Follows real-world team workflow

### 🔐 Security Notes

.env is not committed

Secrets (MongoDB URI, tokens, Stripe keys) must remain private

Use environment variables for all sensitive data

### 📦 Scripts Summary
Frontend
npm run dev
npm run build

Backend
npm run dev
npm start

### 🤝 Contribution Guidelines

Fork the repository

Create a feature branch

Commit with clear messages

Open a pull request

### 📄 License

This project is for educational and hackathon purposes.

### 👨‍💻 Authors

Retail Portal Team
--- 
Built as part of a MERN stack learning & hackathon project
