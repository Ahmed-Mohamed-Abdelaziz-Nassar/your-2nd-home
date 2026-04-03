# 📱 Your 2nd Home — Social Feed Web App

A production-ready **front-end social media application** that simulates a real-world feed-based platform, built using **HTML, CSS, Bootstrap, and Vanilla JavaScript**, and powered by the **Tarmeez Academy REST API**.

This project demonstrates a complete client-side application flow including authentication, API-driven rendering, ownership-based actions, and persistent session management — without relying on modern frameworks.

---

## 🔗 Live Demo

[🚀 View Live Application](https://ur-2nd-home.netlify.app/) : https://ur-2nd-home.netlify.app/

---

## 🚀 Key Features

### 🔐 Authentication

* User registration via API
* Secure login with token-based authentication
* Session persistence using `localStorage`
* Automatic redirect for authenticated users
* Logout with full session cleanup

---

### 📰 Feed System

* Fetch and render posts from a real API
* Infinite scrolling for progressive content loading
* Rich post cards including:

  * author info
  * avatar
  * content
  * images
  * timestamps

---

### ✍️ Post Management

* Create posts using `FormData` (with optional image upload)
* Edit posts via `_method=put`
* Delete posts directly from the feed
* Ownership-based UI controls (edit/delete only for author)

---

### 💬 Comments System

* Lazy-load comments per post
* Inline rendering of comments
* Add comments without leaving the page
* Instant DOM updates after submission

---

### 👤 User-Centric Pages

* **Profile Page**

  * user info (name, email, avatar)
  * post & comment counts

* **My Posts Page**

  * filtered posts by authenticated user
  * full CRUD support on owned content

---

### 🎨 User Experience

* Bootstrap modal workflows:

  * login / signup
  * create / edit post
* Offcanvas navigation for mobile-friendly UX
* Fallback avatars for missing profile images
* “Coming Soon” states for incomplete sections

---

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3, Vanilla JavaScript
* **UI Framework:** Bootstrap 5.3
* **HTTP Client:** Axios
* **State Management:** Browser `localStorage`
* **API:** Tarmeez Academy API
  https://tarmeezacademy.com/api/v1

---

## 📂 Project Structure

```bash
your2ndHome/
├── css/
│   └── master.css
├── html/
│   ├── posts.html
│   ├── myPosts.html
│   └── profile.html
├── imgs/
├── js/
│   ├── main-index.js
│   ├── main-posts.js
│   ├── main-myposts.js
│   ├── main-profile.js
│   └── main.js
├── index.html
├── package.json
└── package-lock.json
```

---

## 🏗️ Architecture

The application follows a **multi-page client-side architecture**, where each page owns its logic:

* `index.html` → authentication & redirect logic
* `posts.html` → main feed + interactions
* `myPosts.html` → user-specific content
* `profile.html` → profile rendering

### Architecture Highlights

* Clear separation between UI and logic
* Page-based modular JavaScript structure
* API-driven dynamic rendering
* `localStorage` as a shared state layer

---

## ⚙️ Installation & Setup

```bash
git clone <your-repository-url>
cd your2ndHome
npm install
```

Run locally:

```bash
npx serve .
```

Or open:

```bash
index.html
```

---

## 🔄 How It Works

* User lands on the public page
* Registers or logs in via modal
* Token and user data stored in `localStorage`
* Redirect to main feed
* Posts are fetched and rendered dynamically
* User can:

  * create posts
  * comment
  * edit/delete owned content
* Navigation allows access to Profile and My Posts
* Logout clears session and returns to landing page

---

## 🔌 API Integration

### Authentication

* `POST /register`
* `POST /login`

### Posts

* `GET /posts`
* `POST /posts`
* `PUT /posts/{id}`
* `DELETE /posts/{id}`

### Comments

* `GET /posts/{id}`
* `POST /posts/{id}/comments`

### User Data

* `GET /users/{id}/posts`

### Auth Method

* Token stored in `localStorage`
* Sent via request headers:

```js
authorization: localStorage.token
```

---

## 🎨 UI/UX Highlights

* Clean card-based layout for readability
* Modal-driven interactions keep context intact
* Responsive navigation using Bootstrap offcanvas
* Optimized layout for both desktop and mobile

---

## ⚡ Performance

* Infinite scrolling for progressive loading
* Lazy loading of comments
* Lightweight client-side rendering
* No heavy frameworks

---

## 🔐 Security

* Token-based authentication
* Protected routes via client-side checks
* Ownership-based UI control
* Session cleared on logout

⚠️ Note: Security ultimately depends on the backend API.

---

## 🧩 Challenges & Solutions

### 🔑 Authentication Without Frameworks

**Challenge:** Managing auth across multiple pages
**Solution:** Centralized session using `localStorage`

### 🖼️ File Upload Handling

**Challenge:** Supporting image uploads
**Solution:** Used `FormData` for multipart requests

### 👤 Ownership Logic

**Challenge:** Restrict actions to post owners
**Solution:** Compare user ID with post author ID

### ⚡ Performance Optimization

**Challenge:** Avoid heavy initial load
**Solution:** Infinite scroll + lazy comment loading

### 🔗 Multi-Page Coordination

**Challenge:** No router or global state
**Solution:** Page-based architecture + shared storage

---

## 📈 Future Improvements

* Refactor shared logic into reusable modules
* Replace reloads with dynamic UI updates
* Add validation and better error handling
* Implement route guards
* Improve accessibility
* Add toast notifications
* Introduce SPA architecture (React/Vue)
* Add testing layer

---

## 🌟 Why This Project Stands Out

* Real API-driven application (not mock data)
* Full authentication + CRUD workflow
* Ownership-aware UI behavior
* Infinite scrolling implementation
* Clean separation of logic and UI
* Demonstrates real product-level thinking

This is not a simple front-end — it is a **functional social platform simulation**.

---

## 👨‍💻 Author

**Ahmed Mohamed Abdelaziz Nassar**
Frontend Developer | Software Engineering Portfolio

🔗 https://github.com/Ahmed-Mohamed-Abdelaziz-Nassar

🔗 https://www.linkedin.com/in/ahmed-mohamed-abdelaziz-nassar/
