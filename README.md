# 📌 Todo Backend - Express & Prisma

This is the **backend API** for the Todo List application. It provides a RESTful API for managing tasks, built using **Express.js, Prisma ORM, and SQLite/MySQL**.

## 🚀 Features
- **Create, Read, Update, Delete (CRUD) operations** for tasks
- **Prisma ORM** for database interaction
- **CORS enabled** for frontend communication
- Supports **SQLite (for development)** and **MySQL (for production)**

---

## 📦 Installation & Setup

### 1️⃣ Clone the Repository
```sh
git clone https://github.com/marcusjv85/nooro_todo_backend.git
cd backend
```

### 2️⃣ Install Dependencies
```sh
npm install
```

### 3️⃣ Configure the Database
#### 🛠 SQLite (Development Mode)
If you are using **SQLite**:
```sh
npx prisma migrate dev --name init
```
This will create the database and apply the schema.

#### 🛠 MySQL (Production Mode)
If you want to use **MySQL**, update your `.env` file with your database credentials:
```sh
DATABASE_URL="mysql://user:password@localhost:3306/todo_db"
```
Then run:
```sh
npx prisma migrate deploy
```

### 4️⃣ Start the Server
```sh
npm run dev
```
This starts the backend server at `http://localhost:5000`.

---

## 🔌 API Endpoints

| Method | Endpoint        | Description |
|--------|---------------|-------------|
| **GET**    | `/tasks`         | Retrieve all tasks |
| **POST**   | `/tasks`         | Create a new task |
| **PUT**    | `/tasks/:id`     | Update a task by ID |
| **DELETE** | `/tasks/:id`     | Delete a task by ID |

### 📥 Example Task JSON Body
#### **POST /tasks** - Create Task
```json
{
  "title": "Finish Project",
  "color": "blue"
}
```
#### **PUT /tasks/:id** - Update Task
```json
{
  "title": "Update Backend API",
  "color": "red",
  "completed": true
}
```

---

## 🛠 Development Notes
- Ensure **backend is running before frontend**.
- You can switch between **SQLite and MySQL** by modifying `prisma/schema.prisma`.
- Use **Railway/Render for backend deployment** and **Vercel for frontend deployment**.

## 🤝 Contributions
Feel free to fork and submit pull requests! 🚀

## 📜 License
This project is open-source and available under the **MIT License**. 📄

