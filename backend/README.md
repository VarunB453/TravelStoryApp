# Travel Story App - Backend

The backend server for the Travel Story application, built with Node.js, Express, and MongoDB.

## Features

- RESTful API architecture
- User authentication with JWT
- Image upload and management
- CRUD operations for travel stories
- Search and filter functionality
- Error handling middleware

## Tech Stack

- **Node.js** - JavaScript runtime
- **Express** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Tokens for authentication
- **Multer** - Middleware for handling file uploads
- **bcryptjs** - Password hashing
- **dotenv** - Environment variable management
- **cors** - Cross-Origin Resource Sharing

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)

### Installation

1. Clone the repository (if you haven't already)
```bash
git clone https://github.com/yourusername/travel-story-app.git
cd travel-story-app/backend
```

2. Install dependencies
```bash
npm install
```

3. Create a `.env` file in the root directory with the following variables:
```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=3000
```

4. Generate a JWT secret (optional)
```bash
node generate-secret.js
```

### Running the Server

#### Development mode
```bash
npm run dev
```

#### Production mode
```bash
npm start
```

## API Documentation

### Authentication Endpoints

#### Register a new user
```
POST /api/auth/signup
```
Request body:
```json
{
  "username": "johndoe",
  "email": "john@example.com",
  "password": "password123"
}
```

#### Login a user
```
POST /api/auth/signin
```
Request body:
```json
{
  "email": "john@example.com",
  "password": "password123"
}
```

#### Logout a user
```
POST /api/user/signout
```

### Travel Story Endpoints

#### Create a new travel story
```
POST /api/travel-story/add
```
Request body:
```json
{
  "title": "My Trip to Paris",
  "story": "It was an amazing experience...",
  "visitedLocation": ["Paris", "France"],
  "imageUrl": "http://localhost:3000/uploads/1234567890.jpg",
  "visitedDate": 1625097600000
}
```

#### Get all travel stories
```
GET /api/travel-story/get-all
```

#### Update a travel story
```
POST /api/travel-story/edit-story/:id
```
Request body:
```json
{
  "title": "Updated Trip to Paris",
  "story": "It was an incredible experience...",
  "visitedLocation": ["Paris", "France"],
  "imageUrl": "http://localhost:3000/uploads/1234567890.jpg",
  "visitedDate": 1625097600000
}
```

#### Delete a travel story
```
DELETE /api/travel-story/delete-story/:id
```

#### Toggle favorite status
```
PUT /api/travel-story/update-is-favourite/:id
```
Request body:
```json
{
  "isFavorite": true
}
```

#### Search travel stories
```
GET /api/travel-story/search?query=Paris
```

#### Filter travel stories by date
```
GET /api/travel-story/filter?startDate=1620000000000&endDate=1630000000000
```

### Image Management Endpoints

#### Upload an image
```
POST /api/travel-story/image-upload
```
Request body (form-data):
```
image: [file]
```

#### Delete an image
```
DELETE /api/travel-story/delete-image?imageUrl=http://localhost:3000/uploads/1234567890.jpg
```

## Project Structure

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

## Error Handling

The API uses a centralized error handling middleware that returns consistent error responses:

```json
{
  "success": false,
  "statusCode": 404,
  "message": "Travel Story not found!"
}
```

## Authentication

The API uses JWT (JSON Web Tokens) for authentication. Protected routes require a valid token in the request cookies.

## File Upload

Images are uploaded to the `/uploads` directory and served as static files. The API returns the URL to access the uploaded image.

## Development

### Adding New Features

1. Create or update models in the `models/` directory
2. Implement controller functions in the `controllers/` directory
3. Define routes in the `routes/` directory
4. Update the main `index.js` file if necessary

### Testing

You can use tools like Postman or Insomnia to test the API endpoints.