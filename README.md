<div align="left">

# 🍽️ **Foodie – Full-Stack Restaurant App**

A full-stack web application for browsing, listing, and managing a variety of food items.  
Built with **React (Frontend)**, **Express.js (Backend)**, and **MongoDB**.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#-contributing)
[![GSSoC'25](https://img.shields.io/badge/GSSoC-2025-orange.svg)](https://gssoc.girlscript.tech/)
[![Dockerized](https://img.shields.io/badge/Containerized-Docker-blue.svg)](#-docker-setup-recommended)
[![Stars](https://img.shields.io/github/stars/Abhishek2634/Foodie.svg?style=social)](https://github.com/Abhishek2634/Foodie)

---

![Foodie Homepage Light Mode](images/foodie-home-light.png)
<sup>Homepage – Light Mode</sup>

</div>

---

## 🌟 GSSoC

![GSSoC Logo](https://github.com/dimpal-yadav/Foodie/blob/main/images/GSSoC.png)

🌟 **Exciting News!**

🚀 This project is now officially part of **GirlScript Summer of Code – GSSoC’25!** 💻  
We’re thrilled to welcome contributors from across India and beyond to collaborate, build, and grow *Foodie!*  

GSSoC is one of India’s **largest open-source programs**, empowering developers of all levels to contribute to real-world projects and grow together.

🌈 With **mentorship**, **community support**, and **collaborative coding**, it’s the perfect platform to:

- ✨ Improve your development skills  
- 🤝 Contribute to impactful projects  
- 🏆 Get recognized for your work  
- 📜 Receive certificates and cool swag  

🎉 **Welcome, GSSoC’25 Contributors!** Let’s build, learn, and grow — one commit at a time.

---

## 🚀 Quick Navigation

> **📚 New to Foodie? Start Here:**  
> 👉 **[LEARN.md](./LEARN.md)** – Architecture, setup, and contribution guide.

> **⚡ Ready to dive in?**  
> Jump to [Getting Started](#-getting-started) for quick setup instructions.

---

## 📑 Table of Contents

- [🔧 Tech Stack](#-tech-stack)
  - [🖥️ Frontend](#️-frontend)
  - [🌐 Backend](#-backend)
  - [🗄️ Database](#️-database)
- [🚀 Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [📦 Installation](#-installation)
  - [🐳 Docker Setup (Recommended)](#-docker-setup-recommended)
  - [📦 Manual Installation](#-manual-installation)
  - [🔧 Development Setup](#-development-setup)
- [📁 Project Structure](#-project-structure)
- [🐳 Docker Commands](#-docker-commands)
- [🧪 Linting](#-linting)
- [🧰 Scripts](#-scripts)
- [📝 Notes](#-notes)
- [🧩 Common Issues & Fixes](#-common-issues--fixes)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [🔗 References](#-references)

---

## 🔧 Tech Stack

### 🖥️ Frontend
- **React 18.3** – User interface  
- **Vite** – Lightning-fast build tool  
- **React Router DOM** – Client-side routing  
- **ESLint** – Code style enforcement  

### 🌐 Backend
- **Node.js + Express** – REST API server  
- **CORS + JSON Middleware** – Cross-origin handling  
- **Multer** – File upload management  
- **Modular Routing** – Organized API structure  

### 🗄️ Database
- **MongoDB** – NoSQL database for scalable storage  

### 🐳 DevOps
- **Docker** – Containerization  
- **Docker Compose** – Multi-service orchestration  

---

## 🚀 Getting Started

### Prerequisites

#### For Docker Setup (Recommended)
- Docker Desktop  
- Docker Compose  

#### For Manual Setup
- Node.js (v16 or above)  
- npm or yarn  
- MongoDB (local or cloud instance)  

---

### 📦 Installation

#### 🐳 Docker Setup (Recommended)

**One-command setup for the entire app:**
```bash
# Clone the repository
git clone https://github.com/your-username/foodie.git
cd foodie
npm install

# Start all services
docker-compose up --build
````

**Access the app:**

* 🌐 Frontend: [http://localhost:3000](http://localhost:3000)
* 🛠️ Admin Panel: [http://localhost:5173](http://localhost:5173)
* 🔌 Backend API: [http://localhost:4000](http://localhost:4000)
* 🗄️ MongoDB: localhost:27017

**Docker Services:**

* `foodie-frontend` – React app
* `foodie-admin` – Admin dashboard
* `foodie-backend` – Express API
* `foodie-mongodb` – Database

---

#### 📦 Manual Installation

```bash
# Clone the repository
git clone https://github.com/your-username/foodie.git
cd foodie

# Install dependencies
cd frontend && npm install && cd ..
cd backend && npm install && cd ..
cd admin && npm install && cd ..
```

---

### 🔧 Development Setup

#### Docker Development

```bash
docker-compose up
# or in detached mode
docker-compose up -d

# View logs
docker-compose logs backend
```

#### Manual Development

```bash
# Start frontend
cd frontend && npm run dev

# Start admin panel
cd admin && npm run dev

# Start backend
cd backend && npm run server
```

Ensure MongoDB is running locally:

```bash
mongod
```

---

## 📁 Project Structure

```
Foodie/
├── .github/                # GitHub configurations & workflows
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
├── admin/                  # Admin panel code
├── backend/                # Backend API
├── frontend/               # Frontend client
├── images/                 # Project images
├── docker-compose.yml      # Docker setup
├── CONTRIBUTING.md
├── LEARN.md
├── LICENSE
└── README.md
```

---

## 🐳 Docker Commands

```bash
# Build & start services
docker-compose up --build

# Start in background
docker-compose up -d

# Stop services
docker-compose down

# Remove volumes (⚠️ Deletes DB)
docker-compose down -v

# View running containers
docker-compose ps
```

---

## 🧪 Linting

```bash
# Frontend
cd frontend && npm run lint

# Admin
cd admin && npm run lint
```

---

## 🧰 Scripts

### Frontend & Admin

| Command           | Description              |
| ----------------- | ------------------------ |
| `npm run dev`     | Start Vite dev server    |
| `npm run build`   | Build for production     |
| `npm run preview` | Preview production build |
| `npm run lint`    | Run ESLint checks        |

### Backend

| Command          | Description                |
| ---------------- | -------------------------- |
| `npm start`      | Start production server    |
| `npm run server` | Start dev server (nodemon) |

---

## 📝 Notes

* Ensure MongoDB is running before starting the backend.
* Update `connectDB()` in `backend/config/db.js` if using remote DB.

**Environment Variables:**

| Service  | Variable                            | Description          |
| -------- | ----------------------------------- | -------------------- |
| Backend  | `MONGODB_URI`, `JWT_SECRET`, `PORT` | DB & API config      |
| Frontend | `REACT_APP_API_URL`                 | Backend API URL      |
| Admin    | `VITE_API_URL`                      | Backend API for Vite |

**File Uploads:**
Multer stores uploaded files in `backend/uploads/`.
Docker mounts this folder for persistence.

---

## 🧩 Common Issues & Fixes

| Issue                               | Possible Fix                                           |
| ----------------------------------- | ------------------------------------------------------ |
| ❌ MongoDB connection fails          | Ensure Docker is running, or check your `MONGODB_URI`. |
| 🐳 Docker build error               | Run `docker system prune -a` and rebuild.              |
| 🚫 Port conflict                    | Stop previous containers: `docker-compose down`.       |
| ⚙️ “npm not found” inside container | Run `docker-compose build` to reinstall dependencies.  |

---

## 🤝 Contributing

We welcome contributions to **Foodie**! ⭐
If you find this project useful, consider **starring** it or submitting a **PR**.

### Development Workflow

1. Fork the repo
2. Create a feature branch
3. Use Docker for consistency
4. Test with `docker-compose up --build`
5. Submit a pull request 🚀

See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed steps.

---

## 💖 Contributors

A heartfelt thanks to everyone who has contributed!

<a href="https://github.com/Abhishek2634/Foodie/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Abhishek2634/Foodie" />
</a>

---

## 📄 License

This project is licensed under the **[MIT License](./LICENSE)**.

---

## 📬 Contact

**Maintainer:** [Abhishek Farswal](https://github.com/Abhishek2634)

📎 **Connect with me:**

* [LinkedIn](https://www.linkedin.com/in/abhishekfarswal/?originalSubdomain=in)
* [Twitter/X](https://x.com/Abhishek899620)
* [Instagram](https://www.instagram.com/abhishekfarswal/)

---

## 🔗 References

* [React](https://reactjs.org/)
* [Vite](https://vitejs.dev/)
* [Express](https://expressjs.com/)
* [MongoDB](https://www.mongodb.com/)
* [Docker](https://www.docker.com/)
