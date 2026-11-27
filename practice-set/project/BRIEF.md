# Phase 1 Project: Responsive Multi-Page Website

**Weeks 2–4 · Individual · Due: end of Week 4 (Day 5)**
**Syllabus outcome:** *A responsive multi-page website built, inspected and debugged with browser DevTools.*

## The client
**Momo Express**, a momo shop in Thamel, Kathmandu, wants its first website. Most of its customers will open it on a phone over mobile data. (You may swap in a real local business you know, with the same requirements.)

## Pages (3 minimum)
| Page | Must contain |
|---|---|
| `index.html`: Home | Hero heading + image, short "about" section, opening hours, a call-to-action link to the order page |
| `menu.html`: Menu | Dishes as cards (name, description, price in Rs) laid out with **Grid**, plus a price **table** (e.g. plate sizes) |
| `order.html`: Order | An accessible order **form**: name, phone (`tel` + pattern), dish (`select`), style (radio group in a `fieldset`), extras (checkboxes), notes, a required checkbox, submit |

Every page shares the same **header with nav** (Flexbox) and **footer**.

## Technical requirements
1. **Valid HTML**: 0 errors on validator.w3.org for every page.
2. **Semantic structure**: `header`, `nav`, `main`, `footer`; one `h1` per page; no skipped heading levels.
3. **Accessible**: alt text, labels, visible focus, contrast ≥ 4.5:1, passes the keyboard test, Lighthouse Accessibility ≥ 95.
4. **SEO basics**: unique `title` + meta description per page, Open Graph tags on the home page.
5. **Responsive**: mobile-first, at least 2 `min-width` media queries, **no sideways scroll at 320px**, `max-width: 100%` images.
6. **CSS architecture**: one shared stylesheet (or the 5-layer split), design tokens in `:root`, BEM-style class names, no `!important`, no ids for styling.
7. **One purposeful transition** (e.g. button hover/focus) + a `prefers-reduced-motion` block.
8. **Git**: a GitHub repo with ≥ 8 meaningful commits across the 3 weeks.
9. File and folder names all **lowercase, no spaces**.

## AI use
Allowed: explaining, reviewing your code and suggesting fixes, generating placeholder text.
**Not allowed:** generating whole pages. You must be able to explain every line (you'll be asked to, live).
Add an `AI-LOG.md` with at least **3 entries** (what you asked, what it said, how you checked it, whether it was right).

## Submit
- GitHub repo link (it will be deployed to GitHub Pages in Week 10)
- `README.md` with: screenshots at 375px and 1280px, your Lighthouse scores, and one bug you found with DevTools and how you fixed it

## Demo (Day 5, 3 minutes)
Show the site at 375px → 1280px in device mode, Tab through the order form, and explain one CSS decision.
