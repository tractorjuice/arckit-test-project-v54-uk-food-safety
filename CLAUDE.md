# CLAUDE.md

## Project: UK Food Safety

A test project for ArcKit's UK food safety overlay (`arckit-uk-food`). It follows an invented café as it builds its food safety documents from the Food Standards Agency's pack *Safer food, better business for caterers*. The café, its people and its answers are made up.

## Toolkit

This project uses the **ArcKit plugin** (v6.22.1) and the **UK food safety overlay**. All commands come from the plugins: no local command files are needed.

The overlay is not in a published ArcKit release yet. If its commands are missing, say so and stop: do not try to do their work by hand.

### Key commands

- `/arckit-uk-food:uk-food-profile` - the business profile (start here)
- `/arckit-uk-food:uk-food-safe-methods` - one section of safe methods at a time
- `/arckit-uk-food:uk-food-own-methods` - the business's own methods
- `/arckit-uk-food:uk-food-check` - what is finished and what is not
- `/arckit-uk-food:uk-food-sign-off` - a named person signs a finished document

### Rules for this project

- Record only what a named person says. Never suggest or fill in an answer.
- The pack's wording reaches a document only through the overlay's own script.
- Never describe a business, its food or a document as compliant, approved, safe or inspected.
- Use invented names only. Put no real business, person, address or council in this repository.

### Project structure

- `projects/001-*/food-safety/` - answer worksheets and the sign-off record
- `projects/001-*/ARC-001-FOOD*.md` - the documents
- `docs/` - documentation and guides

### Document naming

All documents follow `ARC-{PROJECT_ID}-{TYPE_CODE}-v{VERSION}.md`, for example `ARC-001-FOODCOOK-v1.0.md`.
