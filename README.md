🌴 Resort Management System

A full-stack hotel & resort management web application built using Next.js, Node.js/Express, MongoDB, and Cloudinary.
This system allows customers to browse rooms, view details, check availability, and make bookings.
It also includes a complete Admin Panel for managing rooms, reservations, users, and uploads.

🚀 Features
🏡 Frontend (Next.js)

Fully responsive UI

Home page with featured rooms

Room listing with price, type, and occupancy

Dynamic room pages /rooms/[slug]

Image carousel and gallery

Booking form with date selection

User authentication (login/register)

User dashboard for booking history

Global state management

Integrated API calls to backend

Error-free ESLint configuration

SEO optimized Next.js pages

⚙️ Backend (Node.js / Express)

REST API for rooms, bookings, and users

JWT-based authentication

Secure password hashing (bcrypt)

Room availability check

Admin-only protected routes

Booking creation & management

Room CRUD operations

Image upload using multer → cloudinary

MongoDB schema for users, rooms, bookings

Seed script to populate initial data (npm run seed)

🗄️ Database (MongoDB)

Document schemas for:

Users

Rooms

Bookings

Automatic relation mapping

Indexing for efficient room lookup

🛠️ Tech Stack
Frontend

Next.js 14

React 18

Axios

Tailwind CSS

Swiper.js (image carousel)

Backend

Node.js

Express.js

MongoDB + Mongoose

JWT Authentication

Multer

Cloudinary SDK

dotenv

📦 Project Structure
ResortManagementSystem/
│
├── frontend/
│   ├── pages/
│   ├── components/
│   ├── styles/
│   ├── utils/
│   ├── public/
│   └── package.json
│
├── backend/
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── middleware/
│   ├── utils/
│   ├── config/
│   └── package.json
│
└── README.md

🧑‍💻 Installation & Setup
1️⃣ Clone the Repository
git clone https://github.com/YOUR-USERNAME/ResortManagementSystem.git
cd ResortManagementSystem

🔧 Backend Setup
2️⃣ Install dependencies
cd backend
npm install


If multer version error comes, correct version is:

npm install multer@1.4.5-lts.1

3️⃣ Setup environment variables

Create a .env file:

PORT=5000
MONGO_URI=your_mongodb_url
JWT_SECRET=your_secret
CLOUDINARY_CLOUD_NAME=xxxx
CLOUDINARY_API_KEY=xxxx
CLOUDINARY_API_SECRET=xxxx

4️⃣ Run seed script (optional)
npm run seed

5️⃣ Start backend server
npm start

🎨 Frontend Setup
6️⃣ Install dependencies
cd ../frontend
npm install

7️⃣ Start frontend
npm run dev


Frontend will start at:
👉 http://localhost:3000

Backend runs at:
👉 http://localhost:5000

🧰 Admin Panel

Admin can:

Add/edit/delete rooms

Upload images

View all bookings

Manage users

Approve or reject bookings

Admin login made through seeded data:

email: admin@example.com
password: 123456

📸 Screenshots (Optional Section)

You can add your screenshots here.

Example:

/screenshots/home.png
/screenshots/room_details.png

📡 API Endpoints (Summary)
Rooms
GET /api/rooms
GET /api/rooms/:slug
POST /api/rooms (Admin)
PUT /api/rooms/:id (Admin)
DELETE /api/rooms/:id (Admin)

Bookings
POST /api/bookings
GET /api/bookings/user
GET /api/bookings (Admin)

Users
POST /api/auth/register
POST /api/auth/login
GET /api/auth/profile
