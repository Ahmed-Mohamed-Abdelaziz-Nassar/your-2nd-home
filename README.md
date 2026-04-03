# 📱 Your 2nd Home

A fully functional **social media web application** built with HTML, CSS, Bootstrap, and vanilla JavaScript, integrated with the Tarmeez Academy REST API.

The application simulates a real-world social platform, enabling authenticated users to create, manage, and interact with content through a dynamic feed-based interface.

---

## 🚀 Key Features

### 🔐 Authentication

* User registration and login
* Session persistence using `localStorage`
* Auth-based navigation and route control

### 📰 Post Feed

* Fetch and render posts from a real API
* Infinite scrolling for progressive content loading
* Display post metadata (author, avatar, timestamp, image, content)

### ✍️ Post Management

* Create posts with optional image upload (`FormData`)
* Edit and delete posts (ownership-based access)
* Conditional UI rendering based on user identity

### 💬 Comments System

* Lazy-load comments per post
* Submit comments directly from the feed
* Display author details and content

### 👤 User-Centric Pages

* **My Posts:** View and manage only user-owned posts
* **Profile:** Display user data (image, name, email, stats)

### ⚠️ UX Enhancements

* Fallback avatar handling
* Bootstrap alerts for feedback and errors

---

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3, Vanilla JavaScript
* **UI Framework:** Bootstrap 5
* **HTTP Client:** Axios
* **State Management:** Browser `localStorage`
* **API:** Tarmeez Academy API
  https://tarmeezacademy.com/api/v1

---

## 📂 Project Structure

```id="zj4zv5"
.
├── index.html
├── css/
│   └── master.css
├── js/
│   ├── main-index.js
│   ├── main-posts.js
│   ├── main-myposts.js
│   ├── main-profile.js
│   └── main.js
├── html/
│   ├── posts.html
│   ├── myPosts.html
│   └── profile.html
└── imgs/
```

---

## 🏗️ Architecture

The application follows a **multi-page client-side architecture**, where each page is driven by a dedicated script:

* `index.html` → Authentication & redirects
* `posts.html` → Main feed & interactions
* `myPosts.html` → User-specific content
* `profile.html` → Profile rendering

State is managed centrally using `localStorage` (`token`, `userData`) and reused across pages for:

* API authorization
* Conditional UI rendering
* Navigation control

---

## ⚙️ Installation & Setup

```bash id="7wql45"
git clone https://github.com/Ahmed-Mohamed-Abdelaziz-Nassar/your-2nd-home.git
cd your-2nd-home
npm install
```

Run using a local server:

```bash id="r4c9tk"
npx serve .
```

Or use **VS Code Live Server** and open:

```id="c4apdt"
index.html
```

---

## 🎯 Usage

* Start from `index.html`
* Register or log in
* Access the main feed (`posts.html`)
* Create, edit, delete, and comment on posts
* Navigate to:

  * `myPosts.html` for personal posts
  * `profile.html` for account overview

---

## 🔌 API Integration

Integrated endpoints include:

* `POST /register`
* `POST /login`
* `GET /posts`
* `POST /posts`
* `GET /posts/{id}`
* `POST /posts/{id}/comments`
* `POST /posts/{id}` (`_method=put`)
* `DELETE /posts/{id}`
* `GET /users/{id}/posts`

---

## 💡 Key Highlights

* Real API-driven application (no mock data)
* Full authenticated CRUD workflow
* Ownership-aware UI rendering
* File upload support via `FormData`
* Infinite scrolling implementation
* Clean separation between pages and logic

---

## 📈 Future Improvements

* Pre-fill edit forms with existing data
* Refactor shared logic into reusable modules
* Replace full page reloads with local state updates
* Add form validation and better error handling
* Implement route guarding and token expiry handling
* Improve comment rendering performance
* Introduce modular architecture (bundler / framework)

---

## ⚠️ Notes

* The app depends on an external API (availability affects functionality)
* Bootstrap and Axios are loaded via CDN (also listed in `package.json`)
* `main.js` appears to be a legacy or alternate implementation

---

## 👨‍💻 Author

**Ahmed Mohamed Abdelaziz Nassar**
Frontend Developer | Software Engineering Portfolio

🔗 https://github.com/Ahmed-Mohamed-Abdelaziz-Nassar
