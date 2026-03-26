# QA Report: Rosalinda Sanchez Chagua

**Date:** 2026-03-26
**URL:** https://rosalinda-sanchez.cofoundy.dev
**Tier:** Pro (S/.120)
**Status:** FAIL

## Technical Health
- [x] HTML 200
- [x] CSS 200
- [x] Profile image 200
- [x] Favicon 200
- [x] OG image 200
- [x] Guia PDF 200
- [ ] CV PDF — **404 (CRITICAL — Pro tier includes Harvard CV)**

## Visual — Desktop (1280px)
- [x] CSS loaded, site fully styled (Pro template)
- [x] Profile photo visible, natural background, cyan/amber frame
- [x] Name correct: "Rosalinda Sanchez Chagua"
- [x] Title correct: "Abogada — Derecho Regulatorio, Ambiental y Arbitral"
- [x] Colors match config: cyan #0891b2 accent + amber #f59e0b highlight
- [x] Fonts loaded (Libre Baskerville + Source Sans 3)
- [x] All 6 sections render: Hero, About, Projects, Experience, Education, Footer
- [x] No horizontal overflow
- [x] Spacing consistent across all sections
- [x] Footer: "© 2026 Rosalinda Sanchez Chagua" — correct year and name

## Visual — Mobile (375px)
- [x] Name fits within 375px viewport, centered
- [x] Photo properly sized within frame, no overflow
- [x] Text legible, appropriate sizing
- [x] Cards stack vertically (projects, experience, education)
- [x] No horizontal scroll
- [x] Stats readable (4+, 4, UNMSM)
- [x] Contact accessible in footer (email + LinkedIn icons)

## Client Preferences (form match)
- [x] Style: "Minimalista y limpio, Colorido y llamativo" — Pro template with cyan+amber balances both
- [x] Colors: "Cyan y otros combinables" — cyan primary + amber highlight matches
- [x] No special requests in form
- [x] No reference sites provided
- [x] LinkedIn: form had /feed/ (invalid), research found real profile URL — correctly used

## Data Validation
- [x] Name matches source exactly
- [x] Email matches source (rosalinda.sanchez@unmsm.edu.pe)
- [x] LinkedIn URL matches research (pe.linkedin.com/in/rosalinda-sanchez-chagua-1b26061b1)
- [x] Company: UL Energía e Infraestructura — all 4 entries match CV
- [x] Job titles match source (Abogada Junior, Asistenta Legal, Practicante Profesional, Practicante Preprofesional)
- [x] Date ranges match source
- [x] Education: UNMSM (2017-2023), USS Chile (2021-2022), OEFA/OSITRAN/TC (2022-2025) — all match
- [x] Skills: 10 skills, all grounded in CV/research
- [x] Projects: 4 entries match research achievements
- [x] Stats: "4+" años, "4" idiomas, "UNMSM" — all verified from source
- [x] No hallucinated data detected

## Clean Deploy
- [x] No template default names or data
- [x] No placeholder text or Lorem ipsum
- [x] No "undefined" or "null" values
- [x] Social links point to real profiles
- [x] No template default colors (custom cyan + amber applied)

## Issues Found
1. **CRITICAL** — CV PDF returns 404. Pro tier includes Harvard CV as part of the deliverable. Must generate and push cv.pdf to gh-pages branch before delivery.

## Evidence
- desktop-full.png
- mobile-full.png
- 12 section-level screenshots (6 desktop, 6 mobile)
