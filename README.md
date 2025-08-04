# 🐳 React + Node.js + MongoDB (Dockerized Fullstack App)

This is a fullstack web application containerized using Docker and orchestrated with Docker Compose.

### 🧰 Tech Stack
- **Frontend**: React (served with Nginx)
- **Backend**: Node.js + Express
- **Database**: MongoDB
- **Tools**: Docker, Docker Compose

---

### 🚀 Features
- Multi-stage Docker build for optimized image size
- MongoDB runs as a container with persistent volume
- Internal networking via Docker Compose
- Custom Nginx config for React SPA routes (fixes 404 on refresh)
- Secure environment variables using Compose only

---

### ⚙️ Run Locally

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
docker-compose up --build

Frontend: http://localhost:3000
Backend: http://localhost:4000

🧠 What I Learned
Creating optimized Dockerfiles for frontend/backend
Fixing React routing issues in Nginx
Handling MongoDB auth and Docker volume persistence
Cleaning up broken Docker snapshots with builder prune

| Problem             | Solution                             |
| ------------------- | ------------------------------------ |
| React subroute 404  | Used `try_files $uri /index.html;`   |
| MongoDB connection  | Used `database:27017` + `authSource` |
| Docker cache issues | Fixed via `docker builder prune`     |
