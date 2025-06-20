# 🧾 Task Manager API – Built with Node.js & MongoDB

A full-featured task management RESTful API built by **Chhatrapal Varma**, designed with production-level practices in authentication, file uploads, and cloud deployment. This backend app allows users to securely manage their personal tasks, with email notifications, profile avatars, and JWT-based session handling.

> 🔗 **Live API**: [https://api-taskmanager-5ups.onrender.com](https://api-taskmanager-5ups.onrender.com)  
> 📦 **GitHub Repo**: [cybertron1408/api-taskmanager](https://github.com/cybertron1408/api-taskmanager)

---

## 🚀 Key Features

- ✅ JWT Authentication and Login Sessions
- ✉️ Email notifications using SendGrid (on signup and deletion)
- 🔐 Secure password hashing with bcrypt
- ☁️ MongoDB Atlas for cloud-based document storage
- 📁 Avatar Uploads using `multer`
- 📄 Task Filtering, Pagination, and Sorting
- 🛠️ Built using Express.js, Mongoose, and deployed on Render

---

## 📚 API Overview

| Method | Endpoint                           | Auth     | Description                               |
|--------|------------------------------------|----------|-------------------------------------------|
| POST   | `/users`                           | ❌ Public | Register a new user                       |
| POST   | `/users/login`                     | ❌ Public | User login                                |
| GET    | `/users/me`                        | ✅ Private| Get logged-in user's profile              |
| PATCH  | `/users/me`                        | ✅ Private| Update user profile                       |
| POST   | `/users/me/avatar`                 | ✅ Private| Upload profile picture                    |
| GET    | `/users/:userId/avatar`            | ❌ Public | Fetch user's profile picture              |
| DELETE | `/users/me/avatar`                 | ✅ Private| Delete profile picture                    |
| DELETE | `/users/me`                        | ✅ Private| Delete user account                       |
| POST   | `/users/logout`                    | ✅ Private| Logout current session                    |
| POST   | `/users/logoutall`                 | ✅ Private| Logout all sessions                       |

#### 🗂 Task Management Routes

| Method | Endpoint                            | Auth     | Description                              |
|--------|-------------------------------------|----------|------------------------------------------|
| POST   | `/users/tasks`                      | ✅ Private| Create a new task                        |
| GET    | `/users/tasks/:taskId`              | ✅ Private| Fetch a single task                      |
| GET    | `/users/tasks`                      | ✅ Private| Fetch all tasks                          |
| PATCH  | `/users/tasks/:taskId`              | ✅ Private| Update a task                            |
| DELETE | `/users/tasks/:taskId`              | ✅ Private| Delete a task                            |

##### 🔍 Query Options

- `?limit=2` → Paginate results
- `?skip=3` → Skip first 3 results
- `?sortBy=createdAt:asc` or `desc` → Sort tasks by creation date

---

## 🔐 Environment Variables

Before running locally, create a `.env` file:

```env
DB_URL=mongodb+srv://<user>:<pass>@cluster.mongodb.net/taskmanager
JWT_SECRET_KEY=your_jwt_secret
SENDGRID_API_KEY=your_sendgrid_api_key
