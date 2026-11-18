# IDShield

**Automata-Powered Digital Identity Authentication, Access Control and Fraud Prevention Simulator**

Verify identities. Enforce trust. Detect invalid actions.

Independent educational simulation for Automata Theory. No UIDAI affiliation, Aadhaar API, real identifiers, real OTPs or biometrics. Choose only built-in DEMO-USER profiles.

## Run locally (PowerShell)

```powershell
cd IDShield
npm ci
npm run dev -- --host 127.0.0.1
```

Open http://127.0.0.1:5173 (use the port Vite prints if occupied). Installed dependencies already exist in this workspace. Node 20+ recommended.

```powershell
npm test
npm run build
npm run preview -- --host 127.0.0.1
```

The development application needs no external account or service. Production assets are in `dist/`; serve them through HTTP, not file://. Browser localStorage persists synthetic portal applications; sessions reset on reload. Attack Lab uses a separate in-memory store.

## Working features

- Explicit total finite-state protocol with Mealy decisions, configurable retry bounds, consent, mock OTP, offline alternative, expiry guards, logout and replay rejection.
- Ten step/play/pause/replay scenarios, actual event counters and explanations.
- Scholarship eligibility, accepted/rejected/review outcomes and persistent duplicate checks.
- Bank onboarding, examination and public-service presets sharing the same engine (manual-review outcomes).
- Compiled policy DSL and graph/product BFS verification with shortest safety counterexamples.
- Preserved PatternGuard regex/automata visualizer, scanner, lexer, form validator and exports; bounded worker benchmark replaces unsafe synchronous timing.
- Epsilon elimination, right-linear grammar generation, Mealy-to-Moore conversion, scoped grammar simplification/normal forms and bounded PCP search.
- Stack PDA, unary successor and a^n b^n TM with step budget and UNKNOWN outcome.

## Documentation

Start with DEMO_SCRIPT.md and VIVA_PREPARATION.md. EXISTING_PROJECT_AUDIT.md records the original assessment. PROJECT_ARCHITECTURE.md, FORMAL_MODELS.md and ALGORITHMS.md explain the implementation. SYLLABUS_MAPPING.md distinguishes implemented, theoretical and unsupported topics. TEST_REPORT.md and SECURITY_AND_LIMITATIONS.md record evidence and scope.

Original app retained as `src/LegacyApp.tsx`; original README as PATTERNGUARD_LEGACY.md. Legacy marketing claims are superseded by this documentation.

## Mission interface

The front end uses an original GTA V-inspired mission-control aesthetic: fictional city-map geometry, selectable mission signals, district briefings, compact event HUD and responsive tactical panels. Mission launch buttons start a playable top-down city with walking, sprinting, vehicle controls, dialogue, checkpoints, and saved chapter completion. Objectives dispatch real identity events or analyze real finite models. This is a 2D educational game, not a 3D open-world engine. `src/identity/MissionControl.tsx`, `StoryGame.tsx`, `story.ts`, and their styles implement the interface and missions. Controls: WASD/arrows move, Shift sprint, E interact, V vehicle, M map, Escape pause.
