# MealStack

A weekly meal planner: plan recipes across the week, browse a recipe box, and auto-generate a grocery list grouped by aisle (and optionally by store).

## Status

This app was originally built as a [Claude Artifact](https://claude.ai), which means saving data and the AI-powered features (recipe import from pasted text/PDF, calorie estimates) currently rely on `window.claude`, a runtime only available inside Claude's own viewer.

**Hosted here on GitHub Pages, those two things do not work yet:**
- Changes (recipes, week plan, grocery list) are not saved — they reset on every page reload.
- Recipe import and calorie estimation are unavailable.

Everything else (browsing, adding/editing recipes and grocery items in the current session, the week planner UI) works normally in any browser.

## Roadmap

- [ ] Rework persistence to use the browser's `localStorage`, so visitors get a real, saved planner without needing a Claude account.
- [ ] Add a small backend to proxy AI recipe import/calorie estimation without exposing an API key client-side, with a free-tier cap (e.g. 6 recipes) before requiring payment.
