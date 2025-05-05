# 🌍 Travel Story App — Frontend

> ✨ “Every journey deserves a story — this is where yours begins.” ✨

Welcome to the **Travel Story App** frontend — a beautiful, interactive interface for documenting and sharing your wanderlust. Built with cutting-edge tech and designed for seamless storytelling, this is more than just code. It’s a digital passport for memories.

---

## 🧭 What’s Inside the Journey?

> From boarding to arrival — your features itinerary:

* 🛂 **User Access Control** — Sign up, check in, and logout like a seasoned traveler
* 📖 **StoryCrafting** — Create, edit, and delete your travel logs with ease
* 📸 **Photo Gallery** — Upload images to give your memories color
* 💖 **Favorites** — Star the moments that stole your heart
* 🔎 **Discovery Tools** — Search by dates, places, or magical keywords
* 🧼 **Form Guardrails** — Smart validation keeps you on the right path
* 🌀 **Redux-Powered Flow** — Organized state for a smooth user experience
* 📱 **Tailwind-Fueled UI** — Looks amazing from mobile to desktop
* ⚡ **Blazing Speed with Vite** — Because no one likes slow loading

---

## ⚙️ Tech Luggage

A powerful stack for smooth travels:

| Category            | Toolset                       |
| ------------------- | ----------------------------- |
| ✨ UI Framework      | React + Vite                  |
| 🎒 State Management | Redux Toolkit + Redux Persist |
| 🚦 Routing          | React Router                  |
| 🌊 API Requests     | Axios                         |
| 🎨 Styling          | Tailwind CSS                  |
| 🗓️ Date Picker     | React Day Picker              |
| 🔔 Notifications    | React Toastify                |
| 💬 Icons & Modals   | React Icons + React Modal     |

---

## 🧳 Getting Packed

### Requirements

* 📦 Node.js v14+
* 🔌 Backend server (see backend README)

### 🗺️ Setup

1. Clone your boarding pass:

```bash
git clone https://github.com/VarunB453/TravelStoryApp
cd TravelStoryApp/frontend
```

2. Install essentials:

```bash
npm install
```

3. Add your travel key:

```bash
# .env
VITE_API_BASE_URL=http://localhost:3000/api
```

---

### 🧪 Ready for Takeoff?

#### 🛫 Development Mode

```bash
npm run dev
```

Launches at `http://localhost:5173` — your departure gate.

#### 🏁 Build for Production

```bash
npm run build
```

#### 👀 Preview the Journey

```bash
npm run preview
```

---

## 🌐 Site Map (aka Terminal Layout)

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

---

## 🧩 Key Travel Features

### ✍️ Auth Checkpoints

* `Login.jsx` – Gateway to your journey
* `SignUp.jsx` – Passport registration
* `PrivateRoute.jsx` – Guards secret destinations

### 📚 Storybook Components

* `Home.jsx` – Gallery of travel logs
* `AddEditTravelStory.jsx` – Craft your narrative
* `ViewTravelStory.jsx` – Relive your adventures
* `TravelStoryCard.jsx` – A postcard preview of each story

### 🌟 UI Helpers

* `Navbar.jsx` – Navigation for every continent
* `EmptyCard.jsx` – Friendly message for empty pages
* `FilterInfoTitle.jsx` – Search filters in action

---

## 🧠 Powered by Redux

Redux Toolkit gives the app memory and purpose:

* `authSlice.js` – Handles logins and tokens
* `travelStorySlice.js` – Manages the stories themselves
* 🧊 Redux Persist keeps your auth state frozen between reloads

---

## 🌐 Axios Passport

The `axiosInstance.js` file ensures you travel securely:

* Automatic headers
* Error handlers
* Token inclusion
* Base URL configuration

---

## 🖌️ Styled for Adventure

* Tailwind CSS makes the app elegant, fast, and fully responsive
* Custom themes available in `tailwind.config.js`
* Global tweaks in `index.css`

---

## 🌍 Deployment: Send It Live

### ✈️ Build your trip:

```bash
npm run build
```

### 🚀 Choose your destination:

* Netlify
* Vercel
* GitHub Pages
* Firebase Hosting
* AWS S3 + CloudFront

Upload the contents of `dist/` and let the stories begin.

---

## 🧠 Tips for Dev Explorers

### ✨ Adding New Features

* New UI elements → `components/`
* New screens → `pages/`
* Redux changes → `redux/slices/`
* API or helpers → `utils/`

### 🧼 Keep it clean:

```bash
npm run lint
```

Want more safety on your travels? 🚨 Use **TypeScript**! Check out [Vite's React + TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts).

---

## 🧳 Final Thoughts

This isn’t just code — it’s a gateway for creators, explorers, and digital nomads to document what matters. Build it, style it, ship it. Then, go make memories worth storing.

> 📍 *Where will your next story take you?*

---
