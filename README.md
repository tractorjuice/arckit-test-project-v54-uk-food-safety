# UK Food Safety

A test project for ArcKit's UK food safety overlay (`arckit-uk-food`). It follows an invented café as it builds its food safety documents from the Food Standards Agency's pack *Safer food, better business for caterers*.

The café, its people and its answers are made up. Nothing here describes a real business.

## Overview

This repository uses **ArcKit v6.22.1** with the UK food safety overlay.

The overlay is experimental and community-maintained, and covers small caterers in England and Wales. It is not legal advice. The food business operator is responsible for the safety of the food it sells, and the council's environmental health team is the authority. The Food Standards Agency has not reviewed or endorsed the overlay or anything in this repository.

**The overlay is not in a published ArcKit release yet.** Until it is, `arckit-uk-food` will show as not found when the plugins load, and only the core ArcKit commands will be available.

## Getting Started

### Prerequisites

- [Claude Code](https://claude.ai/code) 2.1.319 or later
- GitHub Codespaces (recommended) or a local clone

### Setup

1. Open this repo in a GitHub Codespace (or clone it locally)
2. Claude Code installs itself through `.devcontainer/devcontainer.json`
3. The ArcKit core plugin and the food safety overlay are enabled in `.claude/settings.json`
4. Restart Claude Code once so the marketplace plugins resolve

### First commands

Work in this order. Each command asks its questions in conversation and records only what a named person tells it.

```text
/arckit-uk-food:uk-food-profile        the business, what it does, and who is answering
/arckit-uk-food:uk-food-safe-methods   one section at a time: XC, CL, CH, CK, MG
/arckit-uk-food:uk-food-own-methods    the business's own methods
/arckit-uk-food:uk-food-check          what is finished and what is not
/arckit-uk-food:uk-food-sign-off       a named person signs a finished document
```

## Project structure

```text
projects/
├── 000-global/              # Cross-project artefacts (not used by the overlay)
└── 001-<business>/          # Created by the profile command
    ├── food-safety/         # Answer worksheets and the sign-off record
    └── ARC-001-FOOD*.md     # The documents
```

## What to test here

- An answer nobody gave stays `NOT YET ANSWERED`.
- A command never suggests an answer.
- A document reads as signed off only after the sign-off command records a named person.
- A special process is flagged and not written up.

## Links

- [ArcKit documentation](https://arckit.org)
- [ArcKit repository](https://github.com/tractorjuice/arc-kit)
- [ArcKit Claude plugin marketplace](https://github.com/tractorjuice/arckit-claude)

The overlay is built on *Safer food, better business for caterers*, published by the Food Standards Agency. Contains public sector information licensed under the Open Government Licence v3.0.
