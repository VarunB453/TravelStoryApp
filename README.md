# 🌍 Travel Story App — *Your Adventures, Told Beautifully*

> ✨ *Because every trip deserves a tale.*
> Whether you're scaling mountains, wandering through bustling cities, or strolling along hidden beaches, the **Travel Story App** helps you **capture, organize, and relive your journeys**, one story at a time.

---
| Screenshot 🛸|
|:-----------:|
| ![Screenshot 2025-05-05 151259](https://github.com/user-attachments/assets/157756a2-34c6-4945-b5fb-2a1f58ae0d70) |
| ![Screenshot 2025-05-05 151852](https://github.com/user-attachments/assets/83459a64-d17b-42ae-a3c3-f9133238c228) |
---

## 📸 What Can You Do?



* ✅ **Sign up & dive in** Create your travel journal in minutes.

* 📝 **Write your stories** Add titles, descriptions, dates & memories.

* 🖼️ **Upload stunning images** Because one picture = a thousand words.

* ❤️ **Favorite your best moments**  Highlight the highlights.

* 🔍 **Search & filter** Instantly find that sunset in Santorini.

* 📱 **Fully responsive** Looks beautiful on every screen, big or small.

---

## 🛠️ Tech Behind the Magic

### 🎨 Frontend – The Explorer's Interface

* ⚛️ **React** + Vite – Lightning-fast pages
* 📦 **Redux Toolkit** – State management made simple
* 🧭 **React Router** – Seamless storytelling navigation
* 💅 **Tailwind CSS** – Clean, modern design
* 🛰️ **Axios** – Talk to the backend effortlessly
* 📆 **React Day Picker** – Select travel dates with ease
* 🛎️ **React Toastify** – Friendly feedback for every action

### 🧠 Backend – The Story Engine

* 🔧 **Node.js + Express** – Reliable and fast
* 📚 **MongoDB + Mongoose** – Store all your travel dreams
* 🔐 **JWT Auth** – Your memories are safe with us
* 🗂️ **Multer** – Smooth image uploads
* 🌐 **CORS** – Cross-origin? Cross it off your list.

---

## 🚀 Getting Started on Your Journey

### 📋 What You Need

* Node.js `v14+`
* MongoDB (local or cloud)

### 🧭 Guidebook (Installation)

```bash
# 1. Clone this beautiful journey
git clone https://github.com/VarunB453/TravelStoryApp
cd TravelStoryApp

# 2. Prepare your backend
cd backend
npm install

# 3. Prepare your frontend
cd frontend
npm install
```

🔑 Create a `.env` file in the `backend/` folder:

```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_key
PORT=3000
```

🧪 *(Optional but cool)* Generate a JWT secret:

```bash
node generate-secret.js
```

---

### 🎬 Time to Roll

Start the backend server:

```bash
cd backend
npm start
```

Start the frontend dev server:

```bash
cd frontend
npm run dev
```

🎉 Head over to: [http://localhost:5173](http://localhost:5173) and start writing your story.

---

## 📚 API Map — *Under the Hood*

### 🔐 Auth Routes

* `POST /api/auth/signup` – Create account
* `POST /api/auth/signin` – Log in
* `GET /api/auth/signout` – Log out

### ✍️ Story Routes

* `POST /api/TravelStoryApp/add` – Add a new story
* `GET /api/TravelStoryApp/get-all` – See all your tales
* `POST /api/TravelStoryApp/edit-story/:id` – Update a story
* `DELETE /api/TravelStoryApp/delete-story/:id` – Remove a story
* `PUT /api/TravelStoryApp/update-is-favourite/:id` – Toggle favorite
* `GET /api/TravelStoryApp/search` – Search stories
* `GET /api/TravelStoryApp/filter` – Filter by travel date

### 🖼️ Image Upload

* `POST /api/TravelStoryApp/image-upload` – Add an image
* `DELETE /api/TravelStoryApp/delete-image` – Delete an image

---

## 🗂️ Project Structure

```bash
TravelStoryApp/
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

---

## 📜 License

This project is licensed under the **MIT License** — use it, fork it, build on it. Just don’t forget to write your own stories!

---

## 🤝 Want to Contribute?

Got a feature idea or found a bug?
Open an issue, fork the repo, and submit a pull request — we’d love your help!

---

> *“Traveling – it leaves you speechless, then turns you into a storyteller.” – Ibn Battuta*
> Start your story today. 🌍🖋️

---
