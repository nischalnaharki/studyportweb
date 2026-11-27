# Debugging Lab: "It Looks Perfect on My Laptop!"
**Phase 1 · Week 4 · Day 4 · 2 hours** · Prereqs: P1.12–P1.17

The owner tested the new Momo Express home page on a laptop and loved it. Then customers complained:

> - "On my phone the page is tiny, I have to pinch-zoom." *(Bug A)*
> - "I can scroll sideways. The page is wider than my phone." *(Bugs B, C, D, E: several causes!)*
> - "The momo photo is missing." *(Bug F)*
> - "On my big laptop, the opening hours box should be on the RIGHT. It's at the bottom." *(Bug G)*
> - "Our header should be brand red. My friend's server shows it grey." *(Bug H: see the note below)*

## Tools
- **Device toolbar** (Ctrl+Shift+M): test at **320px, 375px, 768px, 1280px**
- **Find the overflow:** in the Console run
  `document.querySelectorAll("*").forEach(el => { if (el.scrollWidth > document.documentElement.clientWidth) console.log(el) })`
  *(watch-only JS: it lists every element wider than the screen)*
- **Network** tab: look for red (404) rows
- **Styles** panel: an invalid media query shows as… nothing. It's silently ignored.

## Bug H note: a "works on my laptop" bug
Windows and macOS don't care about upper/lower case in file names. **Linux servers do** (Netlify, Render, any VPS).
On Windows Live Server, bug H may look fine! Find it by comparing **every path in the HTML** with the **real file names**, letter by letter.

## Run sheet
| Time | Activity |
|---|---|
| 0:00–0:10 | Open at 1280px: "looks fine". Switch to 375px: chaos. |
| 0:10–1:20 | Pairs: find and fix A–H. Log evidence first, fix second. |
| 1:20–1:45 | Pairs demo their page at 320px with no sideways scroll |
| 1:45–2:00 | Recap: write a "before I ship" responsive checklist together |

## Fix rules
- No `overflow-x: hidden` on `body` to hide the problem. **Fix the cause.**
- The finished page must have **no sideways scroll at 320px**, and the sidebar on the right from 900px up.
