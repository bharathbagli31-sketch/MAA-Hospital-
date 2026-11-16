# HealthAssistAI

HealthAssistAI is a modern, responsive, AI-assisted healthcare guidance web application designed to help users understand symptoms, review potential health conditions, browse an extensive medical encyclopedia, track their personal health profile, and communicate assessments with emergency contacts or healthcare professionals.

> **Medical Disclaimer**: HealthAssistAI is for informational and educational purposes only. It is not a substitute for professional medical advice, clinical diagnosis, or medical treatment. Always consult a qualified healthcare professional regarding any medical conditions.

---

## Features

- **AI-Powered Symptom Checker**: Select from 60+ symptoms across 10 body systems, specify symptom duration, enter free-form symptom descriptions, and receive instant condition likelihood assessments with confidence scoring.
- **Emergency Symptom Detection**: Real-time detection of high-risk warning signs (e.g., chest pain, difficulty breathing, neurological deficits) with prominent urgent care guidance.
- **Health Encyclopedia**: Comprehensive database of diseases and medical conditions detailing descriptions, common causes, risk factors, typical symptoms, and recommended next steps.
- **My Health Dashboard**: Track past health assessments, review condition frequency charts, and visualize assessment history trends over time using interactive Chart.js graphs.
- **Patient Health Profile**: Record physical metrics (height, weight, BMI automatic calculation, blood group, chronic conditions, lifestyle factors).
- **Patient Contacts & Emergency Sharing**: Store trusted contacts and quickly export/share health assessment reports via Email, WhatsApp, PDF download, or clipboard copy.
- **Dark & Light Mode**: Accessible, modern healthcare UI featuring smooth transitions between light and dark themes.

---

## Technologies Used

- **Framework**: [React 18](https://react.dev/) with [TypeScript](https://www.typescriptlang.org/)
- **Bundler & Dev Server**: [Vite 5](https://vitejs.dev/)
- **Styling**: [Tailwind CSS 3](https://tailwindcss.com/) with custom healthcare design system
- **Routing**: [React Router DOM v7](https://reactrouter.com/)
- **Icons**: [Lucide React](https://lucide.dev/)
- **Charts & Data Visualization**: [Chart.js](https://www.chartjs.org/) & [react-chartjs-2](https://react-chartjs-2.js.org/)
- **PDF Generation**: [jsPDF](https://github.com/parallax/jsPDF)
- **Backend & Database**: [Supabase](https://supabase.com/) (PostgreSQL & Supabase Auth)
- **Code Quality**: ESLint 9 & TypeScript Compiler (`tsc`)

---

## Project Structure

```text
├── public/                 # Static assets (favicon, hero images)
├── src/
│   ├── components/         # Reusable UI components (Navbar, Layout, PredictionResults, etc.)
│   ├── contexts/           # React context providers (AuthContext, ThemeContext)
│   ├── data/               # Medical datasets, disease info, symptom mapping, prediction engine
│   ├── lib/                # Supabase client configuration, PDF export & share utilities
│   ├── pages/              # Main view pages (Home, SymptomChecker, Encyclopedia, Dashboard, etc.)
│   ├── App.tsx             # Root application component and route configuration
│   ├── index.css           # Global Tailwind CSS definitions and custom utility classes
│   └── main.tsx            # Vite application entry point
├── supabase/
│   └── migrations/         # Supabase SQL migrations for profiles, contacts, and assessments
├── .env.example            # Template for environment variables
├── .gitignore              # Git ignore rules for node_modules, build outputs, and credentials
├── package.json            # Project manifest, scripts, and dependencies
├── tailwind.config.js      # Custom theme colors, typography, and animation keyframes
├── tsconfig.json           # TypeScript configuration
└── vite.config.ts          # Vite configuration with chunk optimization and path aliases
```

---

## Environment Variables

Copy `.env.example` to create your local `.env` file:

```bash
cp .env.example .env
```

Define the following environment variables:

| Variable | Description | Example / Format |
|---|---|---|
| `VITE_SUPABASE_URL` | Your Supabase project URL | `https://your-project-id.supabase.co` |
| `VITE_SUPABASE_ANON_KEY` | Your Supabase public anonymous API key | `eyJhbGciOi...` |

> **Note**: HealthAssistAI is built with resilient fallback handling. The Core Symptom Checker and Health Encyclopedia work completely offline even if Supabase credentials are not configured. Supabase credentials are only required for user sign in, saved cloud assessments, and remote contact synchronization.

---

## Installation

Ensure you have [Node.js](https://nodejs.org/) (v18 or later) installed on your system.

Install all project dependencies:

```bash
npm install
```

*(On Windows PowerShell, if script execution is restricted, run `npm.cmd install`)*

---

## Run Locally

Start the Vite development server:

```bash
npm run dev
```

*(On Windows PowerShell: `npm.cmd run dev`)*

The application will be accessible at:
```text
http://localhost:5173
```

---

## Build

Compile and bundle the production-ready application:

```bash
npm run build
```

The optimized static files will be generated in the `dist/` directory.

---

## Preview Production Build

Preview the built application locally:

```bash
npm run preview
```

---

## Code Quality & Verification

Run the TypeScript typechecker:
```bash
npm run typecheck
```

Run ESLint to check for code issues:
```bash
npm run lint
```

---

## GitHub Setup

Follow these steps to initialize and push this project to a new GitHub repository:

1. **Initialize Git repository**:
   ```bash
   git init
   ```

2. **Add all files**:
   ```bash
   git add .
   ```

3. **Create the initial commit**:
   ```bash
   git commit -m "Initial commit: Standalone HealthAssistAI project"
   ```

4. **Link to your GitHub repository** (create a new empty repo on GitHub first):
   ```bash
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo-name>.git
   ```

5. **Push to GitHub**:
   ```bash
   git push -u origin main
   ```
