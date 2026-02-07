# 🚀 Project Development Workflow

## 🏗️ System Architecture
This project utilizes a unified backend with a multi-client frontend strategy centered around a shared data layer.

### 1. Backend (The Source of Truth)
- **Stack:** [Convex](https://www.convex.dev/)
- **Auth:** [WorkOS](https://workos.com/) (User Management & SSO)
- **Role:** Handles real-time database, serverless functions, and file storage.
- **Workflow:**
    - Define `schema.ts`.
    - Integrate WorkOS JWT validation in `convex/auth.config.js`.
    - Create shared validation logic using `zod`.
    - Deploy functions to `convex/`.

### 2. Frontend Platforms
| Platform | Framework | UI Kit | Use Case |
| :--- | :--- | :--- | :--- |
| **Landing** | Vite (React) | shadcn/ui | SEO-optimized, fast single-page site. |
| **Web App** | TanStack (React) | shadcn/ui | Complex state, multipage dashboard. |
| **Mobile** | Expo (React Native) | HeroUI / RN-Reusables | Native iOS/Android app via Uniwind. |
