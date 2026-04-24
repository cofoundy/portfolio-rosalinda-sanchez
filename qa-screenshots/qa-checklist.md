# QA Report: Rosalinda Sanchez Chagua

**Date:** 2026-04-05
**URL:** https://rosalinda-sanchez.cofoundy.dev
**Tier:** Pro (S/.120)
**Status:** PASS

## Technical Health
- [x] HTML 200
- [x] CSS 200 (`_astro/index.DpaDnOnV.css`)
- [x] Profile image 200
- [x] Favicon 200
- [x] OG image 200
- [x] Guia PDF 200
- [x] CV PDF 200 (Pro)

## Visual — Desktop (1280px)
- [x] CSS loaded — site is fully styled
- [x] Profile photo visible — professional photo, no broken icon
- [x] Name correct — "Rosalinda Sanchez Chagua" matches config.ts
- [x] Title/tagline visible — "Abogada — Derecho Regulatorio, Ambiental y Arbitral"
- [x] Colors match Annie palette — olive green #6B7B3A on section headers ("Sobre Mi", "Proyectos", "Experiencia", "Educacion"), footer background is olive green. Warm orange #D4874D on CTA button ("Contactame"), stat underlines/accents, experience timeline dots, skill pill borders. Background is peach/cream tones (#F5E6DA / #FDF5EF). No cyan or amber remnants detected.
- [x] Fonts loaded — Google Fonts rendering correctly (serif headings, sans-serif body)
- [x] All 6 sections render — Hero, About (Sobre Mi), Projects (Proyectos), Experience (Experiencia), Education (Educacion), Footer
- [x] No horizontal overflow
- [x] Spacing consistent — sections have even padding/gaps
- [x] Footer — "2026 Rosalinda Sanchez Chagua. Todos los derechos reservados." Year correct, name correct.

## Visual — Mobile (375px)
- [x] Name fits — "Rosalinda Sanchez Chagua" wraps cleanly across two lines, no overflow
- [x] Photo sized correctly — centered, appropriate size, not overflowing
- [x] Nav is mobile-friendly — no desktop nav overflowing (single-page, CTA button visible)
- [x] Text legible — body text and headings appropriately sized
- [x] Cards stack vertically — project cards stack single column
- [x] No horizontal scroll — page fits 375px
- [x] Stats/metrics readable — "4+", "4", "UNMSM" all visible with labels
- [x] Contact info accessible — email and LinkedIn icons in hero and footer

## Color Palette Verification (Primary QA Focus)
- [x] Olive green #6B7B3A — applied to: section titles, footer background, social icon backgrounds
- [x] Warm orange #D4874D — applied to: CTA button ("Contactame"), stat accent lines, experience timeline dots, skill pill borders, education card left borders
- [x] Peach/cream backgrounds — hero section uses light peach, about section uses cream, alternating pattern throughout
- [x] NO cyan remnants detected — old palette fully replaced
- [x] NO amber remnants detected — old highlight fully replaced
- [x] Text readability — dark text on peach/cream backgrounds has sufficient contrast

## Data Validation
- [x] Name: "Rosalinda Sanchez Chagua" — matches research-notes.md
- [x] Email: rosalinda.sanchez@unmsm.edu.pe — matches research-notes.md
- [x] LinkedIn: pe.linkedin.com/in/rosalinda-sanchez-chagua-1b26061b1 — matches research-notes.md
- [x] Companies: UL Energia e Infraestructura — confirmed in research
- [x] Job titles: Abogada Junior, Asistenta Legal, Practicante Profesional, Practicante Preprofesional — match research
- [x] Dates: 2022-2023, 2023-2024, 2024-2025, 2025-Presente — match research
- [x] Education: UNMSM (2017-2023), USS Chile (2021-2022), OEFA/OSITRAN/TC specializations — match research
- [x] Stats: "4+" anos sector energetico (2022-present = 4 years, correct), "4" idiomas (ES/PT/DE/EN per research, correct), "UNMSM" alma mater (correct)
- [x] Achievements: Campeona Debate Defensorial, Moot Ambiental finalista — match research
- [x] No hallucinated data detected

## Clean Deploy
- [x] No template default names
- [x] No placeholder text
- [x] No "undefined" or "null" values
- [x] No template default social links
- [x] Social links point to real profiles (LinkedIn URL verified in research)

## Issues Found
None.

## Evidence
- desktop-full.png
- mobile-full.png
- 12 per-section screenshots (6 desktop, 6 mobile)
