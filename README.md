# CLASS_SYNC – Smart Classroom Attendance & Scheduling

A full‑stack web application that helps colleges **automate attendance, timetables, and student notifications**.  
Built as a production‑style project using a modern MERN stack architecture. [web:1179][web:1180]

---

## ✨ Features

- **Role‑based access** – Separate dashboards and flows for students and teachers.
- **Smart attendance** – Create attendance sessions, mark present students, and track per‑subject percentages.
- **Low‑attendance alerts** – Background jobs auto‑calculate attendance and send notifications when a student drops below a threshold.
- **Timetable & class reminders** – Manage weekly timetables; students receive reminders for classes starting soon.
- **Notifications center** – In‑app notifications for attendance warnings, upcoming classes, and other events.
- **Secure authentication** – Bcrypt password hashing and JWT‑based login for both students and teachers. [web:1186][web:1192]

---

## 🏗️ Tech Stack

| Layer     | Technologies                                       |
|----------|-----------------------------------------------------|
| Frontend | React, Vite, JavaScript, CSS                        |
| Backend  | Node.js, Express.js, Mongoose                       |
| Database | MongoDB (local for dev, MongoDB Atlas for deploy)   |
| Other    | JSON Web Tokens (JWT), bcrypt, node‑cron            | [web:1186][web:1192]

---

## 📂 Project Structure

```text
CLASS_SYNC/
  classsync-backend/        # Node/Express API
    models/                 # Mongoose schemas (User, Subject, Timetable, etc.)
    routes/                 # Auth, setup, teacher, student routes
    middleware/             # Auth & other middlewares
    server.js               # App entrypoint + cron jobs
    .env.example            # Backend env template (no secrets)
  classsync-frontend/       # React client (Vite)
    src/                    # Pages, components, hooks
    public/
    .env.example            # Frontend env template
  README.md
```

---

## 🚀 Getting Started (Local Development)

### 1. Clone the repository

```bash
git clone https://github.com/mayank-bajaj-ai24/CLASS_SYNC-WEB-APP.git
cd CLASS_SYNC
```

### 2. Backend setup

```bash
cd classsync-backend
npm install
```

Create a `.env` file (based on `.env.example`):

```env
PORT=4000
MONGO_URI=mongodb://127.0.0.1:27017/classsync    # or your Atlas URI
JWT_SECRET=classsync-secret
```

Run the backend:

```bash
npm run dev
```

The API should now be available on `http://localhost:4000`.

### 3. Frontend setup

In another terminal:

```bash
cd classsync-frontend
npm install
```

Create `.env` (based on `.env.example`):

```env
VITE_API_BASE_URL=http://localhost:4000
```

Run the frontend:

```bash
npm run dev
```

Open the printed local URL (usually `http://localhost:5173`) in your browser.

---

## 🔐 Environment Variables

Backend (`classsync-backend/.env`):

- `PORT` – Port for the Express server (default `4000`)
- `MONGO_URI` – MongoDB connection string (local or Atlas)
- `JWT_SECRET` – Secret key for signing JWT tokens [web:1098][web:1102]

Frontend (`classsync-frontend/.env`):

- `VITE_API_BASE_URL` – Base URL for the backend API

> **Note:** `.env` files are intentionally **not** committed.  
> Use the provided `.env.example` files as a reference. [web:1152][web:1156]

---

## 📝 Roadmap / Future Enhancements

- Admin role for managing departments, semesters, and sections.
- Exportable attendance reports (CSV / PDF).
- Analytics dashboard for teachers and admins.
- Mobile‑first UI polish and PWA support. [web:1179][web:1181]

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome.

1. Fork the repo  
2. Create a feature branch: `git checkout -b feature/my-feature`  
3. Commit your changes: `git commit -m "Add my feature"`  
4. Push to the branch: `git push origin feature/my-feature`  
5. Open a Pull Request [web:1180][web:1181]

---

## 📄 License

This project is open‑source.  
You’re free to clone, learn from it, and adapt it for your own academic or personal projects.
```
