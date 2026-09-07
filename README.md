# MealStack

A weekly meal planner: plan recipes across the week, browse a recipe box, and auto-generate a grocery list grouped by aisle (and optionally by store).

## Status: fully standalone

No account, no login, no server. It's a single self-contained HTML file (`index.html`) — plain HTML/CSS/JavaScript, no build step, no framework.

- **Saving** — uses the browser's `localStorage`. Your data lives only in the browser you're using; it doesn't sync across devices, and clearing site data/using private browsing means it won't persist.
- **Calorie estimates** — computed locally from a small built-in table of calories-per-100g and typical gram weights for ~60 common ingredients, converting whatever unit you entered (cups, tbsp, oz, lb, cloves, each, etc.) into grams. This is a rough estimate, not a certified nutrition label — ingredients outside the built-in list simply aren't counted, and it's shown as "estimated from N of M ingredients" when some are missing.
- **Recipe import** (Paste Text / PDF) — uses a small rule-based text parser (regex + keyword matching for "Ingredients"/"Instructions" sections, quantity/unit patterns, etc.), not AI. It works reasonably well on typical recipe formats but is much less reliable than AI parsing — always review the result before saving.

## Running it

Open `index.html` directly in any browser, or serve the repo via GitHub Pages / any static host.
