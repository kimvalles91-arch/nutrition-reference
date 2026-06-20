# Nutrition Reference

Internal knowledge base for TRAIN with Coach Kim's nutrition coaching. Supports the client onboarding form and nutrition guide pages (in the `train-app` repo) by giving you structured data and ready-to-use content instead of building everything from scratch per client.

## Structure

```
nutrition-reference/
├── macros/                     # Per-food macro data, organized by category
│   ├── proteins.json
│   ├── starchy-carbs.json
│   ├── fibrous-carbs.json
│   ├── fats.json
│   └── fruit.json
├── meals/                      # Meal idea library, tagged by macro profile
│   ├── breakfast-ideas.md
│   ├── lunch-ideas.md
│   ├── dinner-ideas.md
│   └── snack-ideas.md
├── guidelines/
│   ├── swap-equivalency-guide.md   # The core "teach don't prescribe" reference
│   └── coaching-philosophy.md      # Internal-only: your methodology, not client-facing
└── client-snippets/
    ├── education-snippets.md   # Reusable explainer blurbs for guides/emails
    └── faq.md                  # Pre-written answers to common client questions
```

## How to use this day-to-day

- **Building a client's nutrition guide:** pull meal ideas from `meals/`, swap in their liked foods, reference `macros/` for accurate numbers instead of estimating.
- **Explaining a concept in a session or email:** copy/adapt a blurb from `client-snippets/education-snippets.md` instead of rewriting it each time.
- **Answering a common client question:** check `client-snippets/faq.md` first.
- **Staying consistent on macro/calorie logic:** `guidelines/coaching-philosophy.md` is your own rulebook — useful to re-read periodically, essential if you ever bring on another coach.

## Where this is headed

Right now this is reference content you copy from manually. The macro JSON files are structured so that, eventually, a guide-builder tool could pull macros automatically based on a client's selected foods rather than you calculating each meal's totals by hand. No rush on that — manual works fine for now.

## Maintenance notes

- Add new foods to the relevant `macros/*.json` file as clients request things not yet covered — keep the format consistent (name, serving, calories, protein, carbs, fat).
- Add new meal ideas to `meals/*.md` as you build them for clients — if it worked once, it'll probably work for someone else.
- Update `coaching-philosophy.md` whenever your actual methodology shifts, so it stays a real reference and not a stale snapshot.
