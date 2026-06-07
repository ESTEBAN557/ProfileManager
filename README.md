# ProfileManager

> University Software Engineering Project (Fork)

This repository is a fork of the original **ProfileManager** project developed by **SamuelCV12**.

The purpose of this fork is to preserve and document the work completed during the academic development of the project. This repository contains the following branches:

- **main** — synchronized with the original repository.
- **Esteban** — branch containing my personal contributions, improvements, fixes, and modifications.

As this repository is maintained as a fork, the complete Git history is preserved. Contributions from all collaborators can be reviewed through the commit history, while my individual work can be identified through commits made on the **Esteban** branch.

---

## My Contributions

The work completed in the **Esteban** branch includes:

- Functional system improvements.
- Translation and internationalization enhancements.
- Maintenance and bug fixes.
- User interface refinements.
- General platform improvements and testing.

---

## Academic Context

This repository is maintained as part of a university software engineering project and serves as evidence of academic development, collaboration, and software engineering practices.

---

## Project Overview

A full-stack recruitment platform built with **Next.js 16**, **React 19**, **PostgreSQL**, and **Prisma**. It connects candidates and companies through an intelligent job-matching system powered by AI.

---

## Features

### 👤 Candidate

- Register and manage a detailed professional profile.
- Upload CV/resume (PDF or Word) analyzed using Google Gemini AI.
- View personalized job recommendations with AI-powered matching scores.
- Track application status and interview dates.
- Profile completeness indicator.

### 🏢 Company

- Register and manage company information.
- Create, edit, and manage job vacancies.
- Review candidate applications and schedule interviews.
- Define must-have and nice-to-have skill requirements.

### 🤖 AI Integration

#### CV Parsing

Extracts skills, experience, and education from uploaded PDF/Word documents using Google Gemini AI.

#### Smart Matching

Candidate recommendations are generated using a matching algorithm based on:

- Role alignment (30%)
- Must-have skills (40%)
- Nice-to-have skills (10%)
- Profile completeness (20%)

#### Auto Translation

Dynamic user interface translation powered by Gemini AI.

### 🌐 Internationalization

- English, Spanish, and French support.
- Dynamic AI-powered translations.
- Persisted language preferences.

### 🔒 Security

- Password hashing with bcrypt.
- Password reset via email using Nodemailer.
- Session management with HTTP-only cookies.
- Cross-tab session synchronization using BroadcastChannel.

---

## Tech Stack

| Layer | Technology |
|---------|---------|
| Framework | Next.js 16 (App Router) |
| UI | React 19, Tailwind CSS 4, shadcn/ui |
| Language | TypeScript |
| Database | PostgreSQL |
| ORM | Prisma |
| AI | Google Gemini 2.5 Flash |
| Authentication | Custom (bcrypt + cookies) |
| Email | Nodemailer |
| Containers | Docker Compose |

---

## Getting Started

### Prerequisites

- Node.js 20+
- Docker
- PostgreSQL
- Google Gemini API Key

### Installation

```bash
# Clone repository
git clone https://github.com/ESTEBAN557/ProfileManager.git

# Navigate to project
cd ProfileManager

# Install dependencies
npm install

# Start PostgreSQL container
docker compose up -d

# Run Prisma migrations
npx prisma migrate dev

# Start development server
npm run dev
```

Open:

```text
http://localhost:3000
```

---

## Environment Variables

Create a `.env` file in the project root.

```env
DATABASE_URL="postgresql://user:password@localhost:5432/profilemanager"

GEMINI_API_KEY="your-gemini-api-key"

SMTP_HOST="smtp.example.com"
SMTP_PORT=587
SMTP_USER="your-email@example.com"
SMTP_PASS="your-email-password"
```

---

## Project Structure

```text
ProfileManager
│
├── app/
│   ├── actions/
│   ├── api/
│   ├── dashboard/
│   ├── dashboard-company/
│   ├── profile/
│   ├── profile-company/
│   ├── register/
│   ├── register-company/
│   ├── forgot-password/
│   └── reset-password/
│
├── components/
│
├── context/
│
├── hooks/
│
├── lib/
│   ├── i18n/
│   ├── gemini.ts
│   ├── match.ts
│   ├── completitud.ts
│   └── tab-sync.ts
│
├── prisma/
│   └── schema.prisma
│
└── public/
```

---

## Database Schema

Main entities used by the application:

- **User** – Authentication and user management.
- **Profile** – Candidate profile information.
- **Company** – Company profile information.
- **Vacancy** – Job vacancies and requirements.
- **Application** – Candidate applications.
- **PasswordResetToken** – Password recovery workflow.

---

## Original Repository

This repository is a fork of the original project developed by **SamuelCV12**.

The original repository and its complete development history can be accessed through GitHub's fork relationship.

---

## License

MIT License
