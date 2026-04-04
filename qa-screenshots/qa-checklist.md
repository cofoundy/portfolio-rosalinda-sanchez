# QA Report: Rosalinda Sanchez Chagua

**Date:** 2026-03-31
**URL:** https://rosalinda-sanchez.cofoundy.dev
**Tier:** Pro (S/.120)
**Status:** PASS WITH WARNINGS

## Technical Health
- [x] HTML 200
- [x] CSS 200 (/_astro/index.BKMl1mhV.css)
- [x] Profile 200 (profile.png)
- [x] Favicon 200 (favicon.svg)
- [x] OG image 200 (og.jpg)
- [x] Guia PDF 200 (guia.pdf)
- [x] CV PDF 200 (cv.pdf)
- [x] All 14 icon files in /icons/ return HTTP 200
- [x] Google Fonts loaded (Libre Baskerville + Source Sans 3)

## Visual — Desktop (1280px)
- [x] CSS loaded and styled correctly
- [x] Profile photo visible — high-quality professional photo, no broken image
- [x] Name correct — "Rosalinda Sanchez Chagua" matches config.ts
- [x] Title visible — "Abogada — Derecho Regulatorio, Ambiental y Arbitral"
- [x] Colors match — cyan (#0891b2) accent + amber (#f59e0b) highlight, consistent with form request
- [x] Fonts loaded — Libre Baskerville (headings) + Source Sans 3 (body)
- [x] All 6 sections render (hero, about, projects, experience, education, footer)
- [x] No horizontal overflow
- [x] Spacing consistent across all sections
- [x] Footer — copyright 2026, name correct, email + LinkedIn icons visible

## Visual — Mobile (375px)
- [x] Name fits at 375px — no horizontal overflow
- [x] Photo sized correctly — proportional within frame
- [x] Text legible — appropriate sizes
- [x] Cards stack vertically — projects and experience cards single-column
- [x] No horizontal scroll
- [x] Stats readable — "4+", "4", "UNMSM" all fit
- [x] Contact info accessible — email and LinkedIn icons in hero + footer
- [ ] Nav is mobile-friendly — no visible hamburger menu (nav links are anchor scrolls only, acceptable for this layout)

## Client Preferences (form match)
- [x] Style matches — "Minimalista y limpio" + "Colorido y llamativo" → Pro template with cyan+amber is a good blend
- [x] Colors match — "Cyan y otros combinables" → cyan #0891b2 accent + amber #f59e0b highlight
- [x] LinkedIn included — correct verified URL (pe.linkedin.com/in/rosalinda-sanchez-chagua-1b26061b1)
- [x] No domain requested — using cofoundy.dev subdomain (correct)
- [x] No special requests — form said "No"
- [x] No reference sites provided

## Data Validation
- [x] Name matches source (CV + form + LinkedIn)
- [x] Email matches source (rosalinda.sanchez@unmsm.edu.pe from CV/LinkedIn)
- [x] LinkedIn URL verified and real
- [x] Company "UL Energía e Infraestructura" matches CV
- [x] Job titles match CV progression (Practicante Preprofesional → Profesional → Asistenta Legal → Abogada Junior)
- [x] Date ranges match CV
- [x] Education matches CV (UNMSM 2017-2023, USS Chile 2021-2022, OEFA/OSITRAN/TC courses)
- [x] Achievements verified against research-notes.md (debate championship, Moot finalist, EJIDA coordinator)
- [x] Stats accurate — "4+" years at UL (2022-present), "4" idiomas (ES/PT/DE/EN from CV), "UNMSM" correct
- [x] No hallucinated data detected

## Clean Deploy
- [x] No template default names
- [x] No Lorem ipsum or placeholder text
- [x] No "undefined" or "null" values
- [x] No template default social links
- [x] Social links point to real profiles
- [x] No "<<" markers or TODO comments

## Issues Found

### WARNING: Universidad San Sebastian icon not rendering
- **Severity:** WARNING
- **Location:** Education section, 2nd card
- **Details:** The `BrandIcon` component receives `name="Universidad San Sebastián — Chile"` but the regex `[\s./+#\-]+` does not strip the em dash (U+2014) or accented characters (á in Sebastián). The computed key becomes `universidadsansebastián—chile` which does not match the file `universidadsansebastianchile.png`. The component renders nothing (clean absence, not a broken image), leaving an empty 12x12 placeholder box.
- **Fix:** Either update `icons.ts` regex to also strip em dashes and normalize accents: `name.toLowerCase().normalize('NFD').replace(/[\u0300-\u036f]/g, '').replace(/[\s./+#\-\u2014\u2013]+/g, '')`, or change the school name in config.ts to `"Universidad San Sebastian - Chile"` (ASCII hyphen, no accent).

### WARNING: 12 orphaned icon files in /public/icons/
- **Severity:** WARNING (no user impact, minor bloat)
- **Files not referenced by any component:** defensoriadelpueblo.png, linkedin.svg, minam.png, oefa.png, osinergmin.png, ositran.png, pucp.png, tribunalconstitucional.png, universidadnacionaldeatrujillo.png, universidadsansebastian.png, universidadsansebastianchile.png (would match if regex fixed), unmsm.png
- **Details:** Only 2 of 14 icon files are actually rendered in HTML. The rest were placed in /public/icons/ but no component references their matching name strings. Education uses `edu.school` (matches UNMSM and OEFA/OSITRAN/TC combo), Experience uses `exp.company` (UL Energia has no icon file). Icons like MINAM, Defensoria, PUCP are mentioned in research-notes.md achievements/courses but those entities don't appear as `school` or `company` values in config.ts.
- **Fix:** Either remove unused files to reduce deploy size, or add them where relevant (e.g., individual education entries for OEFA, OSITRAN, PUCP courses if config allowed per-achievement icons).

### INFO: Experience section has no company logos
- **Severity:** INFO (not a bug)
- **Details:** All 4 experience entries are at "UL Energía e Infraestructura" — there is no icon file for this company, so BrandIcon renders nothing. The timeline circles (numbered 1-4) serve as visual anchors instead. This is acceptable since UL is a niche Peruvian firm unlikely to have a public logo in any icon library.

### INFO: Form LinkedIn URL was generic
- **Severity:** INFO (resolved correctly)
- **Details:** The Google Form captured `https://www.linkedin.com/feed/` (generic feed URL, not a profile). The correct profile URL `https://pe.linkedin.com/in/rosalinda-sanchez-chagua-1b26061b1` was found during research and used in config.ts. This was the right call.

## Evidence
- desktop-full.png
- mobile-full.png
- desktop-hero.png, desktop-about.png, desktop-projects.png, desktop-experience.png, desktop-education.png, desktop-footer-5.png
- mobile-hero.png, mobile-about.png, mobile-projects.png, mobile-experience.png, mobile-education.png, mobile-footer-5.png
- manifest.json
