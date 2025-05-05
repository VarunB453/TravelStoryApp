# Travel Story App

A full-stack application for creating and managing travel stories with image uploads, search functionality, and favorites.

## Features

- User authentication (signup, login, logout)
- Create, read, update, and delete travel stories
- Upload and manage images for travel stories
- Mark stories as favorites
- Search and filter stories by date and keywords
- Responsive design

## Tech Stack

### Frontend
- React (with Vite)
- Redux Toolkit for state management
- React Router for navigation
- Tailwind CSS for styling
- Axios for API requests
- React Day Picker for date selection
- React Toastify for notifications

### Backend
- Node.js with Express
- MongoDB with Mongoose
- JWT for authentication
- Multer for file uploads
- CORS for cross-origin requests

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/travel-story-app.git
cd travel-story-app
```

2. Install dependencies for backend
```bash
cd backend
npm install
```

3. Install dependencies for frontend
```bash
cd ../frontend
npm install
```

4. Create a `.env` file in the backend directory with the following variables:
```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=3000
```

5. Generate a JWT secret (optional)
```bash
cd backend
node generate-secret.js
```

### Running the Application

1. Start the backend server
```bash
cd backend
npm start
```

2. Start the frontend development server
```bash
cd frontend
npm run dev
```

3. Open your browser and navigate to `http://localhost:5173`

## API Endpoints

### Authentication
- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/signin` - Login a user
- `GET /api/auth/signout` - Logout a user

### Travel Stories
- `POST /api/travel-story/add` - Create a new travel story
- `GET /api/travel-story/get-all` - Get all travel stories for the logged-in user
- `POST /api/travel-story/edit-story/:id` - Update a travel story
- `DELETE /api/travel-story/delete-story/:id` - Delete a travel story
- `PUT /api/travel-story/update-is-favourite/:id` - Toggle favorite status
- `GET /api/travel-story/search` - Search travel stories
- `GET /api/travel-story/filter` - Filter travel stories by date

### Image Management
- `POST /api/travel-story/image-upload` - Upload an image
- `DELETE /api/travel-story/delete-image` - Delete an image

## Project Structure

```
travel-story-app/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── uploads/
│   ├── utils/
│   ├── index.js
│   └── multer.js
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── redux/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── index.html
│   └── vite.config.js
└── README.md
```

## License

This project is licensed under the MIT License.

---
