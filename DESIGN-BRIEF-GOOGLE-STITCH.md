# Design brief: Portfolio reimagining (Google Stitch)

Use this document as the single source of truth for redesigning **Sahithi Josyam’s** portfolio. Paste into **Google Stitch** or share with a designer. Goal: **high-fidelity desktop + mobile** layouts that preserve **information architecture** and **content hierarchy** unless explicitly changed.

---

## 1. Project overview

**Purpose:** Personal portfolio positioning **Sahithi Josyam** as **product-minded**, with strengths in **workflow / process discovery**, **data**, **automation & AI**, and **cross-functional collaboration**.

**Primary goals**

- Communicate **who she is** and **what she cares about** (product, automation, AI, user-centered solutions).
- Showcase **selected work** (data/ML, dashboards, leadership).
- Highlight **how she works** (services / “What I Do”).
- Drive **contact** (email + LinkedIn).
- Feature one **deep case study** (referral workflow / browser extension) on a **separate page**.

**Tone:** Thoughtful, professional, approachable—not corporate-stiff. Confident but humble (“not a traditional developer” but technically fluent).

---

## 2. Site map & navigation (“tabs”)

The site is **one long home page** (anchor sections) plus **one secondary page**.

### Global navigation (desktop)

| Label | Home (`index.html`) | Case study page (`case-study.html`) |
|--------|---------------------|-------------------------------------|
| **Home** | `#home` | `/` |
| **About Me** | `#about` | `/#about` |
| **Case Study** | `/case-study` | `/case-study` (current page) |
| **Work** | `#work` | `/#work` |
| **What I Do** | `#services` | `/#services` |
| **Contact** | `#contact` | `/#contact` |

### Mobile

- Today: **menu icon** links to **Contact** (`#contact` / `/#contact`). **Stitch may redesign** to a full mobile nav (hamburger with all links).

### Browser tab titles

- **Home:** `Sahithi Josyam | Product`
- **Case study:** `Case Study | Sahithi Josyam`

### URLs (production)

- On disk: `index.html`, `case-study.html`.
- **Clean URLs** when server is configured: `/`, `/case-study` (no `.html` in the address bar).

---

## 3. Page 1: Home — sections (in order)

### A. Hero (`#home`)

- **Headline (multi-line, very large on desktop):**
  - *I Build / Thoughtful Solutions,*
  - *Not Just Software* (visually secondary / muted).
- **Subcopy:** Automation & AI solutions and product; technology serves the user—not the other way around.
- **CTA:** Text link **“Case Study”** → `/case-study` with arrow icon.
- **Visual intent:** Soft **watercolor-style** radial gradients (sky blue → lavender) behind the main headline; editorial, calm.

**Stitch focus:** Hero is the **emotional anchor**; typography scale should feel **dramatic** on desktop, still readable on mobile.

---

### B. About Me (`#about`)

- **Section heading:** *A Little Bit About Me!*
- **Background:** Dark section (`neutral-900` equivalent) with **cream** body text; subtle **indigo** glow blob (top-right).
- **Layout:** Two columns on desktop—**copy left**, **photo right** (`GradPic.png`, rounded, shadow).
- **Copy themes:**
  - Problem solver; **UC San Diego**, **Mathematics–Computer Science**, graduated **June 2025**; complexity, data, decision-making.
  - **Passionate about product management and ownership**, automation & AI; not a traditional developer but technically fluent; cross-functional collaboration; turning *“This takes up so much time”* into *“This just works.”*
  - Broader draw: improving how things work—products, processes, lasting impact.
  - **Hobbies & Interests:** Singing | Classic Literature | Coffee Enthusiast (smaller / muted line).

**Interaction note:** Nav may use **blend / color inversion** over this dark band—Stitch should ensure **contrast and accessibility**.

---

### C. Tools I’ve Mastered (band between About and Work)

- **Eyebrow:** *TOOLS I'VE MASTERED* (small caps, wide tracking).
- **Content:** Chip/pill tags (wrap on small screens), including:  
  PowerBI, Tableau, Python, User Research, Product Design, Process Discovery, Painpoint Discovery, Agile, Scrum, User Stories, Workflow Mapping, Workflow Engineering, Stakeholder Communication, Predictive Modeling, Kanban, Dashboarding, Continuous Improvement, Change Management.
- **Visual:** White pills, light border, hover → indigo accent.

---

### D. Selected Work (`#work`)

- **Heading:** *Selected Work*
- **Three projects**, stacked vertically; alternating **image left / image right** on desktop.

**Project 1 — Predictive Diabetes Assessment**

- Decorative panel: metrics + pseudo-terminal / “training” vibe.
- **Title + paragraph** + tag pills: Python, Pandas, Logistic Regression, Random Forest Classifier.
- **Link:** GitHub (`gp-predictive-diabetes`).

**Project 2 — Customer Churn Analysis**

- Layout **flipped** vs project 1 on desktop.
- Decorative dashboard cards (e.g. Churn, CSAT, simple chart).
- Tags: Pandas, Seaborn, Customer Segmentation, Predictive Modeling, Dashboarding.
- **Link:** Streamlit app.

**Project 3 — Robotics Business Lead**

- Kanban-style decorative (To Do / In Progress / Done).
- Copy: **Legacy Robotics**—PM/business lead; budgeting; cross-functional team; timelines; marketing/sponsorship.
- Tags: Kanban, Excel, Microsoft Office Suite.

**Visual note:** Organic / asymmetric rounded corners on panels; indigo accents; optional purple glow on dark panels.

---

### E. What I Do (`#services`)

- **Heading:** *What I Do*
- **Layout:** Title column + **2×3 grid** of service cards (desktop).

**Six services (title + short description each):**

1. **Workflow Analysis & Improvement** — SIPOC, As-Is mapping, gaps/bottlenecks → product requirements.  
2. **User Stories & Acceptance Criteria** — clarity for development.  
3. **User Research & Interviews** — pain points, validation, user-grounded decisions.  
4. **Stakeholder Communication & Alignment** — product, engineering, operations.  
5. **Process Discovery & Documentation** — As-Is / To-Be, handoffs.  
6. **Product Design** — user-centered design; intuitive products and experiences; adoption.

Each card: small **icon in a circle** (workflow, checklist, user-search, handshake, document, layout metaphors).

---

### F. Contact (`#contact`)

- **Heading:** *Let's Connect!*
- **Subcopy:** Hiring or coffee chat + coffee icon.
- **Email (prominent):** `sahithi.josyam@gmail.com`
- **Button:** *See my LinkedIn* — pill, indigo background, LinkedIn icon in white circle.

---

### G. Footer

- Current implementation is minimal; Stitch may add **©, repeat nav, optional socials**.

---

## 4. Page 2: Case study — full structure

**Route:** `/case-study`  
**Document title:** *Case Study | Sahithi Josyam*  
**Page H1:** *Case Study: Improving Referral Submission Efficiency & Accuracy*

**Sections (single column, max-width readable line length):**

1. **Problem** — Manual referrals across many portals; errors, rework, delays, patient dissatisfaction.  
2. **Discovery & Research** — Intro + **bulleted** activities (interviews/shadowing, SIPOC, As-Is workflows, error sources) + closing paragraph on cognitive load and rework.  
3. **Definition & Requirements** — Success criteria bullets + paragraph on functional requirements (single entry point, navigation, pre-population).  
4. **Solution** — Browser extension + AI; MRN once; workflow alignment.  
5. **Outcome** — Results + bullet impacts + documentation value for onboarding.  
6. **What I Learned** — Bullet list (process discovery, impact, adoption, documentation, product design).

**Navigation:** Same global nav as home; links to home sections use **`/#section`**.

---

## 5. Visual system (reference for Stitch)

**Background:** Cream `#fcfbf9`.  
**Text:** Near-black neutrals for primary body; mid-gray for secondary.  
**Accent:** Indigo for links, hovers, primary buttons, small dots.  
**Selection / highlights:** Sky blue `#87CEEB` (optional in UI polish).

**Typography**

- Headings: **Plus Jakarta Sans** (semibold on major headings).  
- **Recommendation for redesign:** Consolidate to **1–2 font families** max.

**Motion / effects (current site — optional to simplify)**

- Scroll **reveal** (fade + translate).  
- **Cursor glow** on desktop only.  
- **Magnetic** hover on interactive elements.  
- **Watercolor** hero background.  
- Nav treatment over dark **About** section.

**Accessibility:** Respect **`prefers-reduced-motion`**; ensure sufficient contrast on dark About section; keyboard-navigable menus.

---

## 6. SEO & meta (optional cleanup)

- Home **meta description** in HTML may still reference older automation-tool wording; align copy with **Product** positioning and current case study when finalizing content.

---

## 7. Assets & external links

**Assets:** `GradPic.png` (About).  
**External:** GitHub (diabetes project), Streamlit (churn dashboard), LinkedIn profile, `mailto:`.

---

## 8. Success criteria

- Recruiter can scan **Hero + About + Selected Work** in under one minute.  
- Projects and case study feel **substantive**, not only decorative.  
- **Visual consistency** across home and case study.  
- **Contact** paths are obvious without clutter.  
- **Mobile** layouts are as intentional as desktop.

---

## 9. One-line prompt for Stitch (optional)

> Generate high-fidelity **desktop and mobile** UI layouts for this portfolio redesign using the structure and sections in this document; preserve all section names and hierarchy unless the design system explicitly improves hierarchy or accessibility.
