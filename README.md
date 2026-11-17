# CitConnect

Social networking platform for Canadian Institute of Technology (CIT) students to share projects, ideas, and connect with peers.

## Features

- **Student Authentication**: Academic email registration (`@cit.edu.al` / `.edu`), login, and OTP-based password recovery (with automatic sandbox fallback on static hosts like GitHub Pages).
- **Projects & Ideas Feed**: Publish academic projects and collaboration ideas with tags and images, filter by category, like, comment, and collaborate.
- **Discovery & Networking**: Search peers by name, program, or skills, send/accept connection requests, and view student profiles.
- **Direct Messaging & Notifications**: Peer-to-peer chat threads and academic activity alerts.
- **Admin Console**: Moderation dashboard for reviewing and managing accounts, posts, and comments.
- **Light & Dark Mode**: Responsive desktop and mobile layouts with theme persistence.

## Tech Stack

- **Frontend**: React 19, TypeScript, Vite, Tailwind CSS v4, Lucide Icons, Motion
- **Backend (Optional Full-Stack Mode)**: Express, Nodemailer (for live SMTP password recovery emails)

## Local Development

1. Install dependencies:
   ```bash
   npm install
   ```

2. (Optional) Configure environment variables by copying `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```
   The app will be available at `http://localhost:3000`.

## Available Scripts

- `npm run dev` — Start the Express + Vite development server on port 3000
- `npm run lint` — Run TypeScript typechecking (`tsc --noEmit`)
- `npm run build` — Build both the Vite frontend and bundled Node server (`dist/server.cjs`)
- `npm run build:pages` — Build only the static frontend into `dist/` for GitHub Pages
- `npm run start` — Run the production Node server (`dist/server.cjs`)

## GitHub Pages Deployment

The repository includes a GitHub Actions workflow at `.github/workflows/deploy.yml` that automatically typechecks, builds the static Vite bundle (`npm run build:pages`), and deploys `./dist` to GitHub Pages on pushes to `main` or `master`.

To enable it on GitHub:
1. Go to **Settings → Pages** in your repository.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
