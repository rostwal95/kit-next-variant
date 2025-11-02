# Kit Builders — Creator Publishing Platform

<div align="center">
  <br />
  <div>
    <img src="https://img.shields.io/badge/-Next.js_15-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js" />
    <img src="https://img.shields.io/badge/-React_19-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
    <img src="https://img.shields.io/badge/-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
    <img src="https://img.shields.io/badge/-TailwindCSS-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
    <img src="https://img.shields.io/badge/-Zustand-000000?style=for-the-badge&logo=react&logoColor=white" alt="Zustand" />
    <img src="https://img.shields.io/badge/-Tiptap-000000?style=for-the-badge&logo=tiptap&logoColor=white" alt="Tiptap" />
  </div>
  <h3 align="center">Email Marketing & Landing Page Platform Prototype</h3>
  <div align="center">
     Client-side demonstration of creator publishing workflows with broadcasts, A/B testing, and analytics simulation
  </div>
  <br />
  
  <!-- Demo Video -->
  <div align="center">
    <a href="https://github.com/user-attachments/assets/47f81a3e-3cdc-4e6e-9883-2ff4741844e2">
      <img src="docs/demo-poster.png" alt="Dashboard Preview" width="100%" style="max-width: 900px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    </a>
    <p><em>Click to view demo video</em></p>
  </div>
  <br />
</div>

## 📋 Table of Contents

- [Introduction](#-introduction)
- [Tech Stack](#️-tech-stack)
- [Features](#-features)
- [Quick Start](#-quick-start)
- [Architecture](#-architecture)
- [Project Structure](#-project-structure)
- [Development Guide](#-development-guide)
- [Known Limitations](#-known-limitations)


## 🚀 Introduction

This is a **client-side prototype** for a creator publishing platform, containing **40+ components** built to demonstrate complete workflows for email marketing, landing page creation, and experimentation.

**Kit Builders** serves as:

- ✅ **Architectural prototype** for creator economy platforms
- ✅ **Reference implementation** for Next.js App Router patterns
- ✅ **Demo playground** for stakeholder presentations
- ✅ **Learning resource** for modern front-end patterns

> **⚠️ Note:** This is a **prototype/POC**, not production-ready. All data is stored in **localStorage only** — no backend, no database, no authentication. Security hardening, comprehensive testing, and backend integration are intentionally deferred for rapid iteration.

## ⚙️ Tech Stack

### **Frontend** (Client-Side Only)

- **Next.js 15.5** – React framework with App Router & Server Components
- **React 19** – Latest features including enhanced hooks
- **TypeScript 5** – Full type safety across the codebase
- **Tailwind CSS 4** – Utility-first styling with custom design system
- **TipTap v2** – Rich text editor for email/broadcast composition
- **Radix UI** – Accessible component primitives (Dialog, Tooltip, Popover)
- **shadcn/ui** – Pre-built components with Radix + Tailwind
- **Zustand** – Lightweight state management with persist middleware
- **Framer Motion** – Smooth animations and transitions
- **Lucide React** – Icon library
- **Zod** – Runtime validation and type inference

### **Storage & Persistence**

- **localStorage** – Draft storage, published snapshots, event logs
- **Zustand Persist** – State hydration and synchronization

### **Development Tools**

- **pnpm** – Fast, disk-efficient package manager
- **ESLint** – Code linting with Next.js configuration
- **PostCSS** – CSS processing for Tailwind

## ⚡ Features

### 📧 **Email Broadcasting**

- Rich text editor with TipTap (bold, italic, headings, lists, links, images)
- **Subject line editor** with:
  - Character count and optimal length guidance
  - 7 auto-generated subject suggestions (deterministic rotation)
  - A/B variant testing with predicted open rates
  - Lift calculation between variants
- **Preheader field** with character count
- **Draft auto-save** to localStorage
- **Spam detection system**:
  - Keyword-based scoring with weighted triggers
  - Severity classification (low/medium/high)
  - Inline hint display for risky terms
- **Link analysis**:
  - UTM parameter detection
  - Duplicate link identification
  - HTTPS security warnings
  - Domain extraction
- **Merge tag support**:
  - Popover insertion panel
  - Inline `{{` autocomplete trigger
  - 5 built-in tags (first_name, last_name, company, etc.)
- **Content snippets**:
  - CTA button templates
  - Email signature
  - Divider elements
- **Body rewrite variants**:
  - Concise version (removes filler words)
  - Action-oriented close
  - Bullet point extraction
  - Insert or Replace functionality
- **Metrics display**:
  - Word count and reading time estimation
  - Character count
  - Link count
- **Preview modal** with desktop/mobile toggle
- **Assistant side panel** (collapsible, state persisted)
- **Subject history** (last 25 saved)
- **Floating action bar** for Send/Preview/Test

### 🎨 **Landing Page Builder**

- **Template gallery** with 4 starter templates:
  - Creator Newsletter
  - Product Launch
  - Free eBook Lead Magnet
  - Webinar Registration
- **Full-bleed responsive grid** (1-4 columns)
- **Active template selection** with visual glow
- **Draft vs Published snapshot system**:
  - Immutable published versions
  - Dirty state detection badge
  - Timestamp tracking
- **Variant history** with labeled snapshots
- **Theme accent extraction** (synced to email designer)
- **Smart headline generation**:
  - Topic/benefit/tone inputs
  - 5 generated variations
- **Real-time preview** with gradient theming
- **Bullet point editing**
- **CTA customization**

### 🔁 **Event Simulation & Analytics**

- **Traffic simulation controls**:
  - Start/Pause/Resume/Stop
  - Speed adjustment (Calm/Normal/Fast)
  - Progress bar with tick countdown
  - Campaign presets (1h, 24h, launch)
- **Synthetic event generation**:
  - Page views with traffic spikes
  - Signup conversion (4-14% rate)
  - Email sends
- **Event log panel**:
  - Virtualized rendering for performance
  - Incremental load (default 100 events)
  - "Load All" / "Collapse" controls
  - Persisted visible count
  - Timestamp display
- **Conversion funnel metrics**:
  - Page views
  - Signups (with conversion %)
  - Emails sent
- **Sparkline trend visualization**
- **Goal tracking panel**

### 🎯 **Dashboard**

- Quick action cards (Send Email, Newsletter, Landing Page)
- Focus & goals panel
- Funnel metrics overview
- Event log with real-time updates
- Simulation panel
- Reset/refresh controls

### 🎨 **Design System**

- **Layered background system** (`--bg`, `--bg-1`, `--bg-2`, `--bg-3`)
- **Glass/blur surfaces** with gradient overlays
- **Dark mode** with high-contrast tokens
- **Soft shadows** and depth layers
- **Gradient text effects**
- **Accessible focus rings** (Radix-based)
- **Custom scrollbars**
- **Smooth animations** with reduced motion support
- **Responsive typography** with clamp scaling

## 🚀 Quick Start

### Prerequisites

Ensure you have these installed:

- **Node.js 18+**
- **pnpm** (enable with `corepack enable`)

### Local Development

```bash
# 1. Clone the repository
git clone https://github.com/rostwal95/kit-next-variant.git
cd kit-next-variant

# 2. Install dependencies
pnpm install

# 3. Start development server
pnpm dev
```

Visit **http://localhost:3000** → Auto-redirects to `/dashboard`

### Available Scripts

```bash
# Development
pnpm dev              # Start Next.js dev server (port 3000)
pnpm build            # Production build
pnpm start            # Start production server
pnpm lint             # Run ESLint

# Testing
pnpm typecheck        # TypeScript type checking
```

### First Steps After Launch

1. **Dashboard** (`/dashboard`) – View metrics and start simulation
2. **Landing Page** (`/page`) – Select a template and customize
3. **Email Designer** (`/builder/email/demo`) – Compose a broadcast
4. **Published Page** (`/builder/page/demo`) – Publish and view live snapshot

## 🏗️ Architecture

### High-Level Flow

```
┌─────────────────────────────────────────┐
│          Next.js Frontend               │
│       (Client-Side Rendering)           │
│                                         │
│  ┌──────────────┐    ┌──────────────┐   │
│  │   Pages/     │    │  Components/ │   │
│  │   Routes     │◄───┤   UI Layer   │   │
│  └──────┬───────┘    └──────────────┘   │
│         │                               │
│         ▼                               │
│  ┌──────────────┐    ┌──────────────┐   │
│  │   Zustand    │◄───┤  lib/utils   │   │
│  │   Store      │    │  (helpers)   │   │
│  └──────┬───────┘    └──────────────┘   │
│         │                               │
│         ▼                               │
│  ┌──────────────────────────────────┐   │
│  │      localStorage                │   │
│  │  (Drafts, Snapshots, History)    │   │
│  └──────────────────────────────────┘   │
└─────────────────────────────────────────┘
```

### Data Flow Examples

#### 1. **Landing Page Publish Flow**

```
User edits draft → Draft auto-saved to localStorage
                         ↓
              User clicks "Publish"
                         ↓
         Snapshot created with timestamp
                         ↓
      Appended to snapshotHistory array
                         ↓
            hasPublished flag set
                         ↓
         Synthetic views incremented
                         ↓
              Event logged
```

#### 2. **Email Subject A/B Testing**

```
User enters Subject A → Open rate predicted (heuristic)
                              ↓
              User enters Variant B
                              ↓
            Open rate predicted for B
                              ↓
              Lift calculated (B - A)
                              ↓
        Displayed with color-coded indicator
```

#### 3. **Event Simulation Flow**

```
User clicks "Start Simulation" → Timer interval started
                                        ↓
                      runTick() fires every N ms
                                        ↓
              Random traffic spike generated
                                        ↓
           Views/signups/emails incremented
                                        ↓
                 Event log updated
                                        ↓
               Trends array appended
                                        ↓
            localStorage persisted (Zustand)
```

## 📁 Project Structure

```
kit-next-variant/
├── src/
│   ├── app/
│   │   ├── dashboard/
│   │   │   └── page.tsx              # Main dashboard with metrics
│   │   ├── page/
│   │   │   └── page.tsx              # Public landing page viewer
│   │   ├── builder/
│   │   │   ├── page/[pageId]/
│   │   │   │   └── page.tsx          # Landing page editor
│   │   │   └── email/[emailId]/
│   │   │       └── page.tsx          # Email broadcast designer
│   │   ├── broadcast/
│   │   │   └── page.tsx              # Broadcast index
│   │   ├── sequence/
│   │   │   └── page.tsx              # Sequence builder (stub)
│   │   ├── media/
│   │   │   └── page.tsx              # Media library (stub)
│   │   ├── publish/
│   │   │   ├── email/[emailId]/route.ts
│   │   │   └── page/[pageId]/route.ts
│   │   ├── api/
│   │   │   ├── events/route.ts       # Event tracking endpoint
│   │   │   └── unsplash/route.ts     # Image search proxy
│   │   ├── layout.tsx                # Root layout
│   │   ├── page.tsx                  # Home redirect
│   │   └── globals.css               # Global styles + design tokens
│   │
│   ├── components/
│   │   ├── ui/                       # shadcn/ui primitives
│   │   │   ├── button.tsx
│   │   │   ├── card.tsx
│   │   │   ├── input.tsx
│   │   │   ├── dropdown-menu.tsx
│   │   │   ├── tooltip.tsx
│   │   │   ├── badge.tsx
│   │   │   ├── separator.tsx
│   │   │   ├── skeleton.tsx
│   │   │   ├── scroll-area.tsx
│   │   │   └── tag.tsx
│   │   ├── CommandPalette.tsx        # Global command menu
│   │   ├── Drawer.tsx                # Side drawer component
│   │   ├── EmptyState.tsx            # Placeholder UI
│   │   ├── EventLogPanel.tsx         # Virtualized event log
│   │   ├── FieldGroup.tsx            # Form field wrapper
│   │   ├── GoalsPanel.tsx            # Goal tracking display
│   │   ├── MetricCard.tsx            # Metric card with sparkline
│   │   ├── OnboardingDrawer.tsx      # First-run guide
│   │   ├── PageHeading.tsx           # Page header component
│   │   ├── RichTextEditor.tsx        # Tiptap wrapper
│   │   ├── SimulationPanel.tsx       # Traffic simulation controls
│   │   ├── Sparkline.tsx             # Mini trend chart
│   │   ├── SplashScreen.tsx          # Loading screen
│   │   ├── ThemeProvider.tsx         # Dark mode provider
│   │   ├── ToastHost.tsx             # Toast notification system
│   │   └── TopBar.tsx                # Global navigation
│   │
│   ├── lib/
│   │   ├── editor/
│   │   │   └── tiptap.tsx            # Tiptap editor configuration
│   │   ├── stores/
│   │   │   ├── useBuilder.ts         # Page builder store
│   │   │   ├── useFunnel.ts          # Funnel metrics store
│   │   │   └── useTheme.ts           # Theme store
│   │   ├── analytics.ts              # PostHog stub
│   │   ├── db.ts                     # Dexie (unused)
│   │   ├── models.ts                 # Zod schemas
│   │   ├── store.ts                  # Main Zustand store
│   │   ├── utils.ts                  # Helper functions
│   │   └── validation.ts             # Form validation
│   │
├── docs/
│   ├── demo-poster.png               # Video thumbnail
│   └── demo.mp4                      # Demo video
│
├── design_doc.md                     # Comprehensive architecture doc
├── package.json                      # Dependencies
├── tsconfig.json                     # TypeScript config
├── next.config.mjs                   # Next.js config
├── tailwind.config.ts                # Tailwind config
├── postcss.config.mjs                # PostCSS config
└── README.md                         # This file
```

## 🛠️ Development Guide

### State Management

**Zustand Store** (`src/lib/store.ts`):

```typescript
// Main store with persist middleware
const useAppStore = create<AppState>()(
  persist(
    (set, get) => ({
      funnel: { views: 0, signups: 0, emailsSent: 0 },
      publishedSnapshot: null,
      snapshotHistory: [],
      log: [],
      trends: { views: [], signups: [], emails: [] },
      // ... actions
    }),
    { name: "kit_app_store", version: 1 }
  )
);
```

**localStorage Keys:**

| Key                                   | Purpose                     | Max Size  |
| ------------------------------------- | --------------------------- | --------- |
| `kit_app_store`                       | Main Zustand state          | Unlimited |
| `kit_email_draft_<emailId>`           | Email draft (subject, body) | ~1MB      |
| `kit_email_subject_history_<emailId>` | Saved subject variants      | 25 items  |
| `kit_email_assistant_open`            | Assistant panel state       | Boolean   |
| `kit_draft_page`                      | Landing page draft          | ~100KB    |
| `kit_migrated_v2`                     | Migration flag              | Boolean   |

## ⚠️ Known Limitations

### **Architecture & Design**

- ❌ **No Backend** – All data is localStorage only
- ❌ **No Database** – Clearing browser storage wipes all data
- ❌ **No API** – Cannot sync across devices or users
- ❌ **Single-user only** – No multi-tenancy or collaboration
- ❌ **No authentication** – Open access to all features
- ❌ **No rate limiting** – Client-side only

### **Security**

- ❌ **No input sanitization** – XSS vulnerable in email preview
- ❌ **No CSRF protection** – Client-side only
- ❌ **HTML injection risk** – `dangerouslySetInnerHTML` used in preview
- ❌ **No content security policy**
- ❌ **localStorage exposed** – All data readable in DevTools

### **Data & Persistence**

- ❌ **No soft deletes** – Data permanently deleted
- ❌ **No data migration strategy** – Schema changes break storage
- ❌ **No backup/restore** – Manual export/import not implemented
- ❌ **Storage quota limits** – Can hit 5-10MB browser limit
- ❌ **No conflict resolution** – Last write wins

### **Features**

- ⚠️ **AI features are heuristic** – No real LLM integration
- ⚠️ **Email sending is simulated** – Toast notifications only
- ⚠️ **Analytics are synthetic** – Random event generation
- ⚠️ **Image upload disabled** – Base64 only (memory intensive)
- ⚠️ **No deliverability checks** – DKIM/SPF not validated
- ⚠️ **No spam testing** – Keyword-based scoring only
- ⚠️ **No A/B test execution** – Predictions only, no real sending
- ⚠️ **Sequence execution missing** – Draft UI only

### **Performance**

- ⚠️ **Large event logs slow down** – 500 event cap helps but not optimal
- ⚠️ **No pagination** – All data loaded at once
- ⚠️ **No lazy loading** – Components rendered immediately
- ⚠️ **No service worker** – No offline support
- ⚠️ **No code splitting** – Single bundle

### **Testing**

- ❌ **No unit tests** – Zero test coverage
- ❌ **No integration tests** – Component interactions untested
- ❌ **No E2E tests** – User flows not verified
- ❌ **No accessibility audit** – WCAG compliance unknown
- ❌ **No performance testing** – Metrics not tracked

### **Observability**

- ❌ **No error tracking** – No Sentry/Rollbar
- ❌ **No analytics** – PostHog stub only
- ❌ **No logging** – Console only
- ❌ **No monitoring** – No health checks

### **Compliance**

- ❌ **No GDPR flows** – Data deletion not implemented
- ❌ **No consent tracking** – No cookie banners
- ❌ **No data export** – DSAR handling missing
- ❌ **No audit logs** – Changes not tracked

<div align="center">
  <br />
  <p><strong>⚠️ Prototype Disclaimer</strong></p>
  <p>This is a proof-of-concept demonstration. Do not use in production without:</p>
  <p>✓ Backend implementation &nbsp; ✓ Security audit &nbsp; ✓ Authentication &nbsp; ✓ Input sanitization &nbsp; ✓ Testing suite</p>
  <br />
  <p>For more details, see <a href="./design_doc.md">design_doc.md</a></p>
  <br />
</div>
