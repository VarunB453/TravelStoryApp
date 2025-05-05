# Travel Story App - Frontend

The frontend client for the Travel Story application, built with React, Vite, and Tailwind CSS.

## Features

- User authentication (signup, login, logout)
- Create, read, update, and delete travel stories
- Upload and manage images for travel stories
- Mark stories as favorites
- Search and filter stories by date and keywords
- Responsive design with Tailwind CSS
- State management with Redux Toolkit
- Form validation and error handling

## Tech Stack

- **React** - UI library
- **Vite** - Build tool and development server
- **Redux Toolkit** - State management
- **React Router** - Navigation and routing
- **Axios** - API requests
- **Tailwind CSS** - Utility-first CSS framework
- **React Day Picker** - Date selection component
- **React Toastify** - Toast notifications
- **React Modal** - Modal dialogs
- **React Icons** - Icon library
- **Redux Persist** - Persist and rehydrate Redux store

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- Backend server running (see backend README)

### Installation

1. Clone the repository (if you haven't already)
```bash
git clone https://github.com/yourusername/travel-story-app.git
cd travel-story-app/frontend
```

2. Install dependencies
```bash
npm install
```

3. Create a `.env` file in the root directory with the following variables:
```
VITE_API_BASE_URL=http://localhost:3000/api
```

### Running the Application

#### Development mode
```bash
npm run dev
```

This will start the development server at `http://localhost:5173`.

#### Build for production
```bash
npm run build
```

#### Preview production build
```bash
npm run preview
```

## Project Structure

```
frontend/
├── public/
│   └── assets/
├── src/
│   ├── components/
│   │   ├── AddEditTravelStory.jsx
│   │   ├── EmptyCard.jsx
│   │   ├── FilterInfoTitle.jsx
│   │   ├── Navbar.jsx
│   │   ├── PrivateRoute.jsx
│   │   └── TravelStoryCard.jsx
│   ├── pages/
│   │   ├── Auth/
│   │   │   ├── Login.jsx
│   │   │   └── SignUp.jsx
│   │   └── Home/
│   │       ├── Home.jsx
│   │       └── ViewTravelStory.jsx
│   ├── redux/
│   │   ├── slices/
│   │   │   ├── authSlice.js
│   │   │   └── travelStorySlice.js
│   │   └── store.js
│   ├── utils/
│   │   ├── axiosInstance.js
│   │   └── helper.js
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── .eslintrc.js
├── .gitignore
├── index.html
├── package.json
├── tailwind.config.js
└── vite.config.js
```

## Key Components

### Authentication

- `Login.jsx` - User login form
- `SignUp.jsx` - User registration form
- `PrivateRoute.jsx` - Route protection for authenticated users

### Travel Stories

- `Home.jsx` - Main page displaying all travel stories
- `AddEditTravelStory.jsx` - Form for creating and editing travel stories
- `ViewTravelStory.jsx` - Detailed view of a single travel story
- `TravelStoryCard.jsx` - Card component for displaying travel story previews

### UI Components

- `Navbar.jsx` - Navigation bar with user menu
- `EmptyCard.jsx` - Displayed when no stories are available
- `FilterInfoTitle.jsx` - Shows active filters

## State Management

The application uses Redux Toolkit for state management with the following slices:

- `authSlice.js` - Manages user authentication state
- `travelStorySlice.js` - Manages travel story data

Redux Persist is used to persist the authentication state across page reloads.

## API Integration

The `axiosInstance.js` utility creates a configured Axios instance for making API requests to the backend server. It handles:

- Base URL configuration
- Request/response interceptors
- Authentication headers
- Error handling

## Styling

The application uses Tailwind CSS for styling with custom theme configuration in `tailwind.config.js`. Custom styles are defined in `index.css`.

## Deployment

To deploy the frontend application:

1. Build the application:
```bash
npm run build
```

2. The build output will be in the `dist` directory, which can be deployed to any static hosting service like:
   - Netlify
   - Vercel
   - GitHub Pages
   - Firebase Hosting
   - AWS S3 + CloudFront

## Development

### Adding New Features

1. Create new components in the `components/` directory
2. Add new pages in the `pages/` directory
3. Update Redux state in the `redux/slices/` directory
4. Add new utility functions in the `utils/` directory

### Code Style

The project uses ESLint for code linting. Run the linter with:
```bash
npm run lint
If you are developing a production application, we recommend using TypeScript and enable type-aware lint rules. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
