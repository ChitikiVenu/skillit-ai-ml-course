# Skill IT Education — Advanced AI & ML Certification Program

Static website content for the AI & ML course pages at `skilliteducation.com/courses/AI-ML/`.

Sourced from `SKILL_IT_AI_Engineering_Brochure.pdf` — an 8-month program (6 months core learning
across 7 modules + 2 months real-time internship), prepared by an IITian & AI Architect.

## Structure

- `index.html` — Course Overview (Advanced AI & ML Certification Program)
- `module-1-python-technical-foundations/` through `module-7-ai-solutions-engineering/` — the seven module pages
- `assets/css/style.css` — shared stylesheet (same design system as the Cybersecurity course site)
- `assets/img/` — program diagram + favicons
- `assets/downloads/` — the AI & ML program brochure PDF
- `sitemap.xml`, `robots.txt`

## Design

Same visual system as [skillit-cybersecurity-course](https://github.com/ChitikiVenu/skillit-cybersecurity-course):
wavy H1 underline, mockup-card hero image with floating badges, connected-flow module roadmap,
vertical journey timeline, colored CTA buttons, and a compact single-line lead-capture form
("Get Course Details & Fee Structure" + "Enquire Now") appearing twice on the index page.

## Preview locally

```bash
python3 -m http.server 8766
```

Then open `http://localhost:8766/index.html`.

## Notes for whoever deploys this

- The lead-capture form has no backend — submitting it just shows a client-side confirmation
  message. Wire `[data-lead-form]`'s submit handler to a real endpoint (Formspree, a CRM webhook,
  Google Apps Script, etc.) before relying on it to capture leads.
- "Book Career Counselling" links via `tel:` to the number in `data.py`'s `SITE` dict.
- Course fees (₹7,000 onwards) and per-module week/hour estimates are indicative — the source
  brochure gives total program duration (8 months) but not a per-module hour breakdown, so weeks/
  hours per module were estimated proportionally at ~10 hrs/week and should be confirmed against
  the actual batch schedule before publishing.
