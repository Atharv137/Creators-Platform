# Creator's Platform

A full-stack MERN application that enables authenticated users to create, manage, and organize their blog posts with a clean, modern interface.

## Deployment Links

- **Frontend (Live Application):** [https://creators-platform-client.vercel.app/](https://creators-platform-client.vercel.app/)
- **Backend (API Base URL):** [https://creator-platform-api-dgyf.onrender.com](https://creator-platform-api-dgyf.onrender.com)

## Technology Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18, React Router v6, Axios, React Toastify |
| Backend | Node.js, Express.js |
| Database | MongoDB with Mongoose |
| Auth | JWT (JSON Web Tokens) |
| Build Tool | Vite |

## Features

- **User Registration & Login** — Secure JWT-based authentication
- **Persistent Sessions** — Token stored in localStorage; login survives page refresh
- **Protected Routes** — Frontend guards + backend middleware enforce access control
- **Full CRUD** — Create, Read, Update, and Delete blog posts
- **Pagination** — Posts loaded in pages (5 per page) using limit/skip
- **Ownership Checks** — Users can only edit/delete their own posts (enforced backend-side)
- **Error Handling** — Centralized Express error middleware + React toast notifications
- **Authorization** — 403 Forbidden responses for unauthorized actions

## Project Structure

```
creators-platform/
├── client/                 # React frontend (Vite)
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── context/        # AuthContext (global auth state)
│   │   ├── pages/          # Page-level components
│   │   └── services/       # Axios API utility with interceptors
│   └── package.json
├── server/                 # Express backend
│   ├── config/             # MongoDB connection
│   ├── controllers/        # Route logic (auth, users, posts)
│   ├── middleware/         # JWT auth + global error handler
│   ├── models/ 
```
