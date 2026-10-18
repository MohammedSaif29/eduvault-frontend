# 📚 EduVault — Frontend

EduVault is a full-stack **educational resource-sharing platform** where educators upload study material, admins review and approve it, and students discover, save and download resources with personalised recommendations.

This repository is the **React frontend**. The Spring Boot API lives in **[eduvault-backend](https://github.com/MohammedSaif29/eduvault-backend)**.

🔗 **Live demo:** https://fsad-project-frontend-mu.vercel.app

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-06B6D4?logo=tailwindcss&logoColor=white)
![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-000000?logo=vercel)

---

## ✨ Features

**Authentication**
- Email/password sign-up and login with JWT
- **Google OAuth 2.0** sign-in
- Role-based routing for **Student**, **Educator** and **Admin**

**Students**
- Explore, search and filter resources by category
- Save resources, download files and leave feedback
- Personal dashboard with recent activity and **recommended resources**

**Educators**
- Upload resources, see which are pending approval, and track views of their uploads

**Admins**
- Review pending uploads: approve them or remove them
- Manage users and roles
- Analytics dashboard: downloads trend, category statistics, saved resources, platform overview (charts with Recharts)

## 🛠️ Tech Stack

React 19 · React Router 7 · Vite · Tailwind CSS · Axios · Framer Motion · Recharts · Lucide icons · react-hot-toast · deployed on **Vercel**

## 🏗️ Architecture

```
React (Vercel)  ──REST + JWT──►  Spring Boot API (Railway)  ──►  MySQL
       │                                 │
       └──── Google OAuth redirect ──────┘
```

## 🚀 Run Locally

```bash
npm install
cp .env.example .env      # set VITE_API_BASE_URL to your backend, e.g. http://localhost:8080/api
npm run dev               # http://localhost:5173
```

| Variable | Purpose |
|---|---|
| `VITE_API_BASE_URL` | Backend REST API base URL (`…/api`) |
| `VITE_BACKEND_ORIGIN` | Backend origin, used for Google OAuth redirects |
| `VITE_AUTH_API_URL` | Auth endpoints (`…/api/auth`) |
| `VITE_RECAPTCHA_SITE_KEY` | Optional, if reCAPTCHA is enabled |

**Deploying to Vercel:** build command `npm run build`, output directory `dist`, and set the variables above in the project settings.

## 📁 Project Structure

```
src/
  api/          Axios client and API helpers
  hooks/        Custom React hooks
  lib/          Helpers (incl. reCAPTCHA)
  layouts/      Role-based dashboard layouts
  pages/
    Admin/      Dashboard, ManageUsers, ManageResources, Downloads, Categories
    Educator/   Educator dashboard
    Student/    Explore, Saved, MyActivity, Dashboard
    Login, Register, ResourceDetail, Upload …
  components/   Shared UI components
```

## 👤 Author

**Mohammed Saif** — B.Tech CSE
[LinkedIn](https://www.linkedin.com/in/saif-mohammed-939902335/) · [GitHub](https://github.com/MohammedSaif29)
