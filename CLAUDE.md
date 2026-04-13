# Soulmigo Marketing

## Overview

Marketing website for Soulmigo, a UK-based yoga essentials brand specializing in anatomical flow grip socks. The site includes landing pages and an interactive product recommendation quiz that helps users discover personalized yoga gear based on their experience, goals, and preferences.

## Structure

```
Marketing/
├── index.html              # Main landing page - "Build Your Yoga Starter Kit"
├── quiz-landing/
│   ├── index.html          # Quiz landing page - "Find Yoga Essentials That Fit You"
│   └── assets/images/      # Quiz-specific assets (beach yoga background, etc.)
├── assets/
│   └── images/             # Shared images (yoga stock photos, illustrations, product shots)
├── Product/                # Product specifications and assets
└── soul.svg                # Logo/silhouette
```

## Design System

**Colors:**

- Primary (Green): `#1A7A3A`
- Secondary (Terracotta): `#C4704B`
- Champagne: `#F2E8DF`
- Ebony: `#1A1A1A`
- Glass background: `rgba(255, 255, 255, 0.08-0.45)`

**Typography:**

- Display: `Bodoni Moda` (elegant, editorial)
- Headings: `DM Sans` (600 weight)
- Body: `Inter` (300-500 weight)
- Logo: `Outfit` (500 weight, -1.2px letter-spacing)

**Effects:**

- Glass morphism backgrounds with backdrop-filter blur
- Noise texture overlay (`https://grainy-gradients.vercel.app/noise.svg`)
- Animated gradient borders (green → terracotta)
- Slow/fast transitions: `0.5s` and `0.3s` cubic-bezier easing
- Float animation for hero images

## Quiz Features

The quiz landing page includes a 6-question interactive quiz:

1. **Workout frequency** - How often they exercise
2. **Yoga experience** - Never → Advanced
3. **Age** - Slider (18-80)
4. **Goals** - Fitness, flexibility, fun, mental health
5. **Studio finder** - Google Maps integration for local studios
6. **Yoga type preference** - Hatha, Vinyasa, Yin, Restorative, Ashtanga

**Recommendation logic** generates:

- Main product (Anatomical Flow Grip Socks) with personalized reasoning
- Mat recommendations based on experience/style
- Additional items (blocks, strap, bolster) as relevant
- External resources (Yoga With Adriene, apps)

**Email capture** via MailerLite integration (form ID: 182677428452197540).

## Conventions

- All pages are single HTML files with embedded CSS and JavaScript
- Mobile-first responsive design with breakpoints at 600px, 900px, 1200px
- Use semantic HTML5 elements (`<main>`, `<header>`, `<footer>`)
- Maintain consistent spacing using the established design tokens
- All images are stored in `assets/images/` or subdirectory-specific `assets/` folders
- Logo text is lowercase: "soulmigo yoga socks"

## Deployment

Pages deploy to Cloudflare Pages (see memory for pending deployment details).

---

## My Behavior for This Project

When working on Soulmigo marketing materials:

### Communication Style

- **Concise and direct** - Get to the point, no filler words or lengthy explanations
- **Show, don't tell** - Provide actual copy/code, not just descriptions
- **Spanish or English** - Match the user's language preference

### How I Work

1. **Read before writing** - Always read existing files before modifying them
2. **Maintain consistency** - Follow the established design system and voice
3. **Single HTML files** - Keep pages self-contained with embedded CSS/JS
4. **Mobile-first** - Design for mobile, enhance for desktop

### When I Use Agents

| Agent | When to Call | Trigger Words |
| :--- | :--- | :--- |
| **copywriting** | Writing/improving marketing copy, headlines, CTAs | "escribe copy", "mejora el texto", "headline", "CTA", "copywriting" |
| **marketing-psychology** | Applying psychology to influence behavior, understand why people buy | "psicología", "mental models", "persuasion", "por qué compran", "behavior" |
| **digital-marketing-web-creator** | Full marketing strategy, website architecture, SEO, funnels | "estrategia de marketing", "web architecture", "SEO", "funnel", "landing page strategy" |

### Before Making Changes

- Read the existing file first
- Check if an agent should handle the task
- Maintain the design system (colors, fonts, effects)
- Test responsive breakpoints

### Saving Steps to CLAUDE.md

**Important**: After completing work, ask if the user wants to save the steps taken to this file. Only add if the user confirms - don't auto-save every action.

Ask: *"¿Quieres que guarde estos pasos en el CLAUDE.md?"* or *"Should I add these steps to CLAUDE.md?"*

If yes, add a brief summary under a new `## Recent Work` section at the end of the file.

### Copywriting Conventions

- **Benefits over features** - What it means for the customer
- **Customer language** - Use words yoga practitioners use
- **Specific over vague** - Real numbers, concrete outcomes
- **One idea per section** - Build logical flow
- **No exclamation marks** - Let the copy speak for itself

### Brand Voice

- **Calm and grounded** - Reflect yoga values
- **Expert but accessible** - Not overly technical
- **Warm but professional** - Friendly without being casual
- **Lowercase logo** - "soulmigo yoga socks"

---

## Recent Work

### 2026-04-07 - Quiz Results Redesign

**Goal**: Improve quiz ending which was too basic/poor.

**What was done**:

1. **Created 6 dynamic archetypes** based on quiz answers:
   - Mindful Beginner (new + mental health + Hatha/Restorative)
   - Fitness Seeker (new/beginner + fitness + Vinyasa/Ashtanga)
   - Flexibility Hunter (any level + flexibility + Yin/Vinyasa)
   - Dedicated Flow (intermediate/advanced + Vinyasa/Ashtanga)
   - Restorative Soul (any level + mental health + Yin/Restorative)
   - Balanced Yogi (intermediate + fun + Hatha/Vinyasa)

2. **New result page structure**:
   - Archetype title + "Welcome to your practice" subtitle
   - Personalized story (2-3 sentences reflecting their answers)
   - Why Anatomical Grip Socks (customized reasoning)
   - Action plan (4 concrete steps)
   - Mat + clothing recommendations (no brand names)
   - Highlighted resource per archetype

3. **Created yoga-expert agent** (`.claude/agents/yoga-expert/SKILL.md`) for yoga-specific guidance.

**Files changed**:
- `quiz-landing/index.html` - Complete redesign of results section

**Commit**: `a4ab862` - "Redesign quiz results with dynamic archetypes"
