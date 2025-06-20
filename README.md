You're right — thanks for your patience! Here's **everything in one complete Markdown block** — fully combined, copy-paste ready, and already formatted exactly as you'd want for your `README.md` file:

---

````markdown
# 🧾 Task Manager API – Node.js & MongoDB

A full-featured **task management RESTful API** built by **Chhatrapal Varma**. This backend service enables users to manage personal tasks securely with features like **JWT authentication**, **email notifications**, **avatar uploads**, and **cloud deployment**. Built using **Node.js**, **Express.js**, and **MongoDB**, the project follows industry best practices.

> 🔗 **Live API**: [https://api-taskmanager-5ups.onrender.com](https://api-taskmanager-5ups.onrender.com)  
> 📦 **GitHub Repository**: [cybertron1408/api-taskmanager](https://github.com/cybertron1408/api-taskmanager)

---

## 🚀 Features

- ✅ JWT-based authentication with login sessions
- ✉️ Email notifications (via SendGrid) on signup & account deletion
- 🔐 Secure password hashing using `bcrypt`
- 📁 Avatar uploads using `multer`
- ☁️ MongoDB Atlas for cloud-hosted document storage
- 🔎 Task filtering, pagination, and sorting
- 📦 Built with `Express.js`, `Mongoose`, and deployed on Render

---

## 📚 API Endpoints

### 👤 User Routes

| Method | Endpoint                      | Access   | Description                        |
|--------|-------------------------------|----------|------------------------------------|
| POST   | `/users`                      | Public   | Register a new user                |
| POST   | `/users/login`                | Public   | User login                         |
| GET    | `/users/me`                   | Private  | Get current user profile           |
| PATCH  | `/users/me`                   | Private  | Update user profile                |
| POST   | `/users/me/avatar`            | Private  | Upload profile avatar              |
| GET    | `/users/:userId/avatar`       | Public   | Fetch user's avatar                |
| DELETE | `/users/me/avatar`            | Private  | Delete profile avatar              |
| DELETE | `/users/me`                   | Private  | Delete user account                |
| POST   | `/users/logout`               | Private  | Logout from current session        |
| POST   | `/users/logoutall`            | Private  | Logout from all sessions           |

### ✅ Task Routes

| Method | Endpoint                     | Access   | Description                        |
|--------|------------------------------|----------|------------------------------------|
| POST   | `/users/tasks`               | Private  | Create a new task                  |
| GET    | `/users/tasks`               | Private  | Fetch all tasks                    |
| GET    | `/users/tasks/:taskId`       | Private  | Fetch a single task                |
| PATCH  | `/users/tasks/:taskId`       | Private  | Update a task                      |
| DELETE | `/users/tasks/:taskId`       | Private  | Delete a task                      |

---

## 🔍 Task Query Parameters

You can use the following parameters to filter, paginate, and sort tasks:

- `?limit=2` → Limit results to 2 tasks  
- `?skip=3` → Skip the first 3 results  
- `?sortBy=createdAt:asc` → Sort by oldest first  
- `?sortBy=createdAt:desc` → Sort by newest first  

---

## 🔧 Environment Variables

Create a `.env` file in the root directory with the following keys:

```env
DB_URL=your_mongodb_atlas_connection_url
JWT_SECRET_KEY=your_secure_jwt_secret
SENDGRID_API_KEY=your_sendgrid_api_key
````

---

## 🛠️ Installation & Local Setup

Follow the steps below to run the project locally:

```bash
# Clone the repository
git clone https://github.com/cybertron1408/api-taskmanager.git

# Move into the project folder
cd api-taskmanager

# Install dependencies
npm install

# Start the server
npm start
```

> The server will be available at: `http://localhost:5991`
> You can test the endpoints using Postman, Insomnia, or cURL.

---

## 👨‍💻 About the Developer

**Chhatrapal Varma**
A passionate Backend Developer who enjoys building scalable APIs, cloud integrations, and RESTful services with Node.js and MongoDB.

* 🌐 [LinkedIn](https://www.linkedin.com/in/jay-varma-472615225/)
* 💻 [GitHub](https://github.com/cybertron1408)
* 📧 Email: [chhatrapal.varma.dev@gmail.com](mailto:chhatrapal.varma.dev@gmail.com)

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

Feel free to raise an issue if you spot bugs or have improvement suggestions.

---

## 🔐 Security

If you find any security vulnerabilities or issues:

* Open an issue on GitHub
* Or email directly at **[chhatrapal.varma.dev@gmail.com](mailto:chhatrapal.varma.dev@gmail.com)**

All reports will be taken seriously and handled as a priority.

---



