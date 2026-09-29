# NovexCare | AI-Powered Cognitive & Memory Companion
> **Smart India Hackathon (SIH) Problem Statement:**  
> *“AI-Based Cognitive Gaming and Memory Assistance Platform for Elderly Dementia Patients in North Eastern Region (NER)”*

---

## 🌟 1. Project Overview

**NovexCare** is a production-grade, patient-centered cognitive health and memory stimulation platform specifically tailored for elderly individuals experiencing mild cognitive impairment (MCI) or early-stage dementia across the **North Eastern Region (NER)** of India (Assam, Meghalaya, Manipur, Nagaland, Arunachal Pradesh, Mizoram, Tripura, and Sikkim).

Unlike generic game websites or static mockups, NovexCare connects **Elderly Patients** with their **Family Caregivers** in an emotionally grounded, scientifically calibrated ecosystem:
- **Personalized Recognition Engine:** Caregivers upload real photographs of sons, daughters, grandchildren, local neighborhoods, and cultural heritage memories. The platform automatically converts these memories into playable cognitive recognition games.
- **NER Cultural Resonance:** Incorporates indigenous cultural anchors—Assam Golden Muga silk, Bihu Dhol & Pepa, traditional CTC tea brewing, Kamakhya Temple, and riverfront landmarks—that trigger long-term nostalgic recall.
- **Rule-Based Adaptive Personalization Engine:** Monitors game precision, response latency, and cognitive assessment screenings to dynamically adjust game difficulty and generate a daily 3-activity cognitive care routine.
- **Clinical Reporting & PDF Export:** Generates standardized, timestamped cognitive activity reports with Recharts longitudinal tracking and print/PDF formatting for physician consultations.
- **Elderly Accessibility Standard:** Scalable typography (`Normal`, `Large`, `Extra Large`), high-contrast viewing mode, Web Audio synthetic feedback, and Web Speech API voice guidance.

---

## 🛠️ 2. Technology Stack

- **Frontend Core:** React 19, TypeScript, Vite
- **Styling & UI:** Tailwind CSS (custom healthcare palette, accessible typography scales, print media rules)
- **Routing:** React Router v7 (role-based protected routes, session persistence)
- **Icons:** Lucide React
- **Data Visualization:** Recharts (score progressions, accuracy trends, category radar distributions)
- **Audio & Speech:** HTML5 Web Audio API (synthetic auditory feedback), Web Speech API (cadenced voice instructions)
- **Visual Celebration:** Canvas Confetti
- **Local Persistence & Data Layer:** Resilient client-side storage with canvas image compression (protects memory bounds by scaling uploads to 480x480 at 0.82 JPEG quality)

---

## 📂 3. Professional Project Structure

```
f:/cognitive-gaming/
├── public/                     # Static assets & icons
├── src/
│   ├── assets/                 # Brand assets
│   ├── components/
│   │   ├── auth/
│   │   │   └── ProtectedRoute.tsx      # Role-based route guard
│   │   ├── common/
│   │   │   ├── AccessibilityBar.tsx    # Font scaler, high-contrast, TTS toggle
│   │   │   └── MedicalDisclaimer.tsx   # Ethical non-diagnostic healthcare notice
│   │   └── layout/
│   │       ├── AppLayout.tsx           # App shell with mobile drawer & desktop sidebar
│   │       ├── Navbar.tsx              # Top app bar with profile avatar & demo switcher
│   │       ├── Sidebar.tsx             # Desktop role-based navigation sidebar
│   │       └── MobileBottomNav.tsx     # Elderly-accessible mobile touch navigation
│   ├── context/
│   │   ├── AccessibilityContext.tsx    # Global accessibility & speech synthesizer state
│   │   └── AuthContext.tsx             # Authentication, session, & active patient context
│   ├── games/
│   │   ├── GameContainer.tsx           # Reusable HUD, timer, difficulty, & result screen
│   │   ├── MemoryMatchGame.tsx         # 6/12/16 card 3D flip matching game
│   │   ├── SequenceRecallGame.tsx      # Working memory temporal item ordering
│   │   ├── FocusFinderGame.tsx         # Odd-one-out visual scanning with latency timer
│   │   ├── DailyLifeOrderGame.tsx      # Tea brewing & morning routine step ordering
│   │   ├── ObjectRecognitionGame.tsx   # NER daily & cultural object identification
│   │   ├── PatternCompleteGame.tsx     # Inductive visual pattern completion
│   │   ├── FamilyRecognitionGame.tsx   # "Who is this?" game with uploaded family photos
│   │   ├── PlaceRecognitionGame.tsx    # "Where is this?" game with uploaded local places
│   │   └── CulturalRecognitionGame.tsx # Traditional NER heritage recognition
│   ├── pages/
│   │   ├── LandingPage.tsx             # SIH hero portal with 1-click test portals
│   │   ├── AssessmentPage.tsx          # 12-question cognitive screening assessment
│   │   ├── auth/
│   │   │   ├── LoginPage.tsx           # Validated login with demo quick-fill
│   │   │   └── SignupPage.tsx          # Patient / Caregiver registration flow
│   │   ├── caregiver/
│   │   │   ├── CaregiverDashboardPage.tsx # Monitored patient KPIs & quick actions
│   │   │   ├── CaregiverProfilePage.tsx   # Credentials & patient linking
│   │   │   ├── ContentManagerPage.tsx     # CRUD for Family, Places, & Cultural photos
│   │   │   └── PatientReportPage.tsx      # Clinical progress report & PDF print layout
│   │   └── patient/
│   │       ├── GamesHubPage.tsx        # Central cognitive gym with adaptive daily plan
│   │       ├── MemoryAssistancePage.tsx # Daily medicine reminders & memory booklet
│   │       ├── PatientDashboardPage.tsx # Patient hub with greeting & real stats
│   │       ├── PatientProfilePage.tsx   # Auto age-calculation & photo upload
│   │       └── PatientProgressPage.tsx  # Longitudinal Recharts graphs & session logs
│   ├── services/
│   │   ├── adaptiveEngine.ts           # Rule-based difficulty & daily session generator
│   │   └── storage.ts                  # Persistent data layer with NER demo seeder
│   ├── types/
│   │   └── index.ts                    # Strong TypeScript models & interfaces
│   ├── utils/
│   │   ├── dateUtils.ts                # Precise Age calculation from DOB
│   │   ├── greetingUtils.ts            # Time-of-day greeting generator
│   │   ├── imageUtils.ts               # In-browser HTML5 canvas image compressor
│   │   ├── soundUtils.ts               # Web Audio API sound synthesizer
│   │   └── ttsUtils.ts                 # Web Speech API voice guidance helper
│   ├── App.tsx                         # Router configuration
│   ├── index.css                       # Tailwind layers, font-size scales, print CSS
│   └── main.tsx                        # React DOM entry point
├── index.html                          # Meta tags, accessible fonts, & SVG icon
├── tailwind.config.js                  # Tailwind theme, custom palettes & print breakpoints
└── package.json                        # Dependencies & run scripts
```

---

## ⚡ 4. Installation & Local Run Commands

Clone or navigate to the repository directory and run:

```bash
# 1. Install all dependencies
npm install

# 2. Run the local development server
npm run dev
```

The application will immediately be accessible at:
👉 **`http://localhost:5173/`**

To compile a production build:
```bash
npm run build
npm run preview
```

---

## 🚀 5. Core Platform Features

### A. Real Authentication & Role-Based Access
- **Dual Portal Security:** Dedicated routes for Elderly Patients (`/patient/*`) and Caregivers (`/caregiver/*`).
- **Protected Routing:** Prevents cross-role access (Patients cannot access caregiver management; Caregivers cannot play patient sessions directly without linked context).
- **Persistent Sessions:** Stored securely in the local application storage.

### B. Patient Profile & Automatic Age Calculation
- **Mandatory Age Formula:** Automatically calculates exact age from the entered Date of Birth (accounting for leap years and boundary dates). The user cannot manually alter the age field.
- **Real Image Upload:** In-browser canvas image compression ensures patient photos are persistent and display seamlessly across the navbar, dashboard, progress pages, and clinical reports.

### C. Patient ↔ Caregiver Connection System
- Caregivers link elderly patients via registered email.
- Caregivers view only their connected patients with data isolation.
- Patients can see their connected caregiver on their dashboard and profile.

### D. 9 Fully Playable Interactive Games

| Game | Domain | Mechanics |
|---|---|---|
| **Memory Match** | Working Memory | 3D card flips, 6/12/16 cards (3 difficulty tiers), move counter & accuracy tracking |
| **Sequence Recall** | Temporal Memory | Memorize symbol sequence (3-6 items), hide, reproduce in order |
| **Focus Finder** | Visual Attention | Spot the odd-one-out in 3x3, 4x4, or 5x5 grids with response time tracking |
| **Daily Life Order** | Procedural Logic | Reorder shuffled daily routines (Assam tea brewing, morning medication) |
| **Object Recognition** | Visual Association | Identify familiar daily & regional objects from clear photographs |
| **Pattern Completion** | Inductive Logic | Determine the sequence rule and select the next item |
| **Family Recognition** | Personalized Recall | **"Who is this?"** game using actual caregiver-uploaded family photos & stories |
| **Place Recognition** | Spatial Orientation | **"Where is this?"** game using caregiver-uploaded local neighborhood landmarks |
| **Cultural Recognition**| Long-Term Memory | Identify authentic North Eastern cultural traditions, Bihu instruments, & Muga silk |

### E. AI-Assisted Adaptive Recommendation Engine
- Rules analyze historical accuracy, response latency, and cognitive assessment screening scores.
- Automatically tunes difficulty between `Easy`, `Medium`, and `Hard`.
- Curates a daily 3-exercise routine to strengthen primary focus areas (e.g. Memory, Attention, or Problem Solving).

### F. Cognitive Activity Screening
- 12-question interactive screening evaluating Memory, Attention, Calculation, Language, Visual Perception, and Practical Problem Solving.
- Calculates domain breakdown (0–100%) and provides adaptive care recommendations.

### G. Caregiver Reporting & One-Click PDF Print
- Comprehensive health document containing patient demographics, radar/bar domain breakdown, longitudinal performance charts, session history, and personalization insights.
- Dedicated `@media print` styling removes navigation bars and buttons, yielding a clean clinical document ready for PDF export or physician review.

---

## 👵 6. Demo & Seed Data Instructions

The platform comes pre-seeded with authentic North Eastern Region (Guwahati, Assam) scenario data:
- **Patient Profile:** *Nirmala Devi* (68 years old, Guwahati, Assam)
- **Caregiver Profile:** *Priya Barua* (Daughter)
- **Pre-Loaded Family Members:** Rajesh Barua (Son), Ananya Barua (Granddaughter), Bhaskar Barua (Brother)
- **Pre-Loaded Places:** Kamakhya Temple Hill, Brahmaputra Riverfront Park, Kaziranga Tea Garden Estate
- **Pre-Loaded Cultural Memories:** Assam Golden Muga Mekhela, Bihu Dhol & Pepa, Traditional Spiced Tea, Jaapi
- **Pre-Recorded History:** 8 realistic cognitive game sessions and formal screening results showing authentic progress charts.

### Instant 1-Click Login:
1. Open `http://localhost:5173/`
2. Click **“👵 Test as Patient (Nirmala Devi)”** to explore the patient companion.
3. Click **“👩‍⚕️ Test as Caregiver (Priya Barua)”** to explore caregiver controls and reports.
4. Or use the credentials:
   - Patient: `nirmala.devi@novexcare.in` / `patient123`
   - Caregiver: `priya.barua@novexcare.in` / `caregiver123`
5. Reset or reload demo data anytime by clicking the **“NER Demo Data”** button in the top navbar.

---

## 🏆 7. Recommended SIH Demonstration Flow

1. **Landing Page:** Showcase the dual-portal entry, NER cultural focus, and senior accessibility bar.
2. **Patient Registration / Profile:**
   - Demonstrate automatic age calculation (change DOB to `1958-08-15` → Age automatically becomes `68 years`).
   - Upload a new patient photo and notice it reflected across all screens.
3. **Caregiver Content Manager:**
   - Go to Caregiver Portal → Recognition Content.
   - Upload a new family photo or familiar place.
4. **Personalized Gaming:**
   - Switch to Patient Portal → Games Hub → Family Recognition ("Who is this?").
   - Experience the game displaying the exact photo uploaded by the caregiver!
5. **Standard Games:**
   - Play a round of *Memory Match* or *Daily Life Order (Brewing Assam Tea)*.
   - Observe live scoring, sound feedback, and celebratory confetti upon completion.
6. **Cognitive Screening:**
   - Complete the 12-question assessment and review the domain score breakdown.
7. **Caregiver Dashboard & Clinical Print:**
   - Switch back to Caregiver Portal → Patient Reports.
   - Observe the live Recharts graph updated with the newly played game.
   - Click **“Print / Save as PDF”** to demonstrate the clean medical document layout.

---

## ⚠️ 8. Ethical Medical Disclaimer

NovexCare is an assistive cognitive stimulation, memory assistance, and family communication platform designed for elderly individuals and caregivers in the North Eastern Region. **It is not a clinical medical diagnostic system and does not claim to detect, diagnose, treat, or cure dementia, Alzheimer's disease, or any neurological disorder.** All screening metrics are intended purely for activity monitoring and to facilitate discussions with licensed medical practitioners.
