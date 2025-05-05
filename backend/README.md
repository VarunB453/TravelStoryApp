# 🌍 Travel Story App - Backend

*Your adventures, our APIs. Share stories, upload memories, and explore the world—one endpoint at a time.*

---

## ✨ What Is This?

Welcome to the backend of the **Travel Story App**—a Node.js-powered engine that fuels the storytelling experience. It’s built to handle everything from user authentication to image uploads and story management.

Whether you're posting about a Parisian getaway or a hike through the Himalayas, this backend has your back.

---

## 🚀 Features

* 🧭 RESTful API architecture
* 🔐 Secure JWT-based authentication
* 🖼️ Image upload and static serving
* ✏️ Full CRUD support for travel stories
* 🔍 Smart search and date filtering
* 💥 Centralized error handling for smooth debugging

---

## 🛠️ Tech Stack

| Tech         | What it does                          |
| ------------ | ------------------------------------- |
| **Node.js**  | JavaScript runtime environment        |
| **Express**  | Web framework for handling routes/API |
| **MongoDB**  | Flexible NoSQL database               |
| **Mongoose** | MongoDB ORM for schema & queries      |
| **JWT**      | Token-based authentication            |
| **Multer**   | Handles file uploads                  |
| **bcryptjs** | Password hashing and salting          |
| **dotenv**   | Manages environment variables         |
| **cors**     | Enables cross-origin requests         |

---

## ⚙️ Getting Started

### 📦 Prerequisites

* Node.js (v14+)
* MongoDB (local or Atlas cluster)

### 📥 Installation

```bash
# Clone the repo
git clone https://github.com/VarunB453/TravelStoryApp
cd TravelStoryApp/backend

# Install dependencies
npm install
```

### 🔐 Environment Setup

Create a `.env` file in the `backend/` directory:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=3000
```

Need help generating a strong JWT secret? Run:

```bash
node generate-secret.js
```

---

## 🏁 Running the Server

### 🛠 Development

```bash
npm run dev
```

### 🚢 Production

```bash
npm start
```

---

## 📚 API Overview

### 🔐 Authentication

* **Register:** `POST /api/auth/signup`
* **Login:** `POST /api/auth/signin`
* **Logout:** `POST /api/user/signout`

### 📖 Travel Stories

* **Create:** `POST /api/TravelStoryApp/add`
* **Read all:** `GET /api/TravelStoryAppy/get-all`
* **Update:** `POST /api/TravelStoryApp/edit-story/:id`
* **Delete:** `DELETE /api/TravelStoryApp/delete-story/:id`
* **Favorite toggle:** `PUT /api/TravelStoryApp/update-is-favourite/:id`
* **Search stories:** `GET /api/TravelStoryApp/search?query=Paris`
* **Filter by date:** `GET /api/TravelStoryApp/filter?startDate=...&endDate=...`

### 🖼️ Image Management

* **Upload:** `POST /api/TravelStoryApp/image-upload` (form-data)
* **Delete:** `DELETE /api/TravelStoryApp/delete-image?imageUrl=...`

---

## 🗂️ Project Structure

```
backend/
├── controllers/
│   ├── auth.controller.js
│   ├── travelStory.controller.js
│   └── user.controller.js
├── models/
│   ├── travelStory.model.js
│   └── user.model.js
├── routes/
│   ├── auth.route.js
│   ├── travelStory.route.js
│   └── user.route.js
├── uploads/           # Directory for uploaded images
├── utils/
│   ├── error.js
│   └── verifyUser.js
├── .env               # Environment variables (not in repo)
├── .gitignore
├── generate-secret.js # Helper script for JWT secret
├── index.js           # Entry point
├── multer.js          # File upload configuration
├── package.json
└── README.md
```

---

## 🧰 Developer Guide

### 🔄 Adding New Features

1. Model your data in `models/`
2. Add controller logic in `controllers/`
3. Wire routes in `routes/`
4. Hook up middleware or services as needed

### 🧪 Testing the API

Use **Postman**, **Insomnia**, or **Thunder Client** (VS Code) to test endpoints with real data and files.

---

## ❗ Error Handling Example

All errors follow a consistent format:

```json
{
  "success": false,
  "statusCode": 404,
  "message": "Travel Story not found!"
}
```

---

## 🔒 Authentication & Security

* Routes are protected with JWT and validated via middleware
* Passwords are hashed with `bcryptjs`
* Tokens are stored in HTTP-only cookies for added security

---

## 📁 File Uploads

* Images are stored in `/uploads`
* URLs are returned for easy access and preview
* Static file serving is enabled for public access

---

## 💡 Pro Tip

Want to contribute? Fork, clone, and create magic! PRs are welcome.

---

Ready to bring your travel stories to life? ✈️

---



