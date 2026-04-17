# FoxConnect docs workspace instructions

This repository is a Zensical-based documentation site for FoxConnect, with English and Thai versions.

## What to edit here

- `docs/en/` — English documentation content and page structure
- `docs/th/` — Thai documentation content and page structure
- `zensical.toml` — English site configuration and navigation
- `zensical.th.toml` — Thai site configuration and navigation
- `assets/images/` — shared image assets copied into the generated site
- `docs/en/stylesheets/nav-always-expanded.css` and `docs/th/stylesheets/nav-always-expanded.css` — site styling overrides
- `.github/workflows/docs.yml` — GitHub Actions workflow that builds and deploys the site

## Build / preview commands

This project uses Zensical to build the documentation site.

- `pip install zensical`
- `zensical build --clean`
- `zensical build --clean -f zensical.th.toml`

The generated static site files are written to `site/`.

## Deployment

GitHub Pages deployment is configured in `.github/workflows/docs.yml`.

The workflow:
- checks out the repo
- installs Python and Zensical
- builds both the English and Thai sites
- copies `assets/images/` into `site/assets/images/`
- copies `CNAME` into `site/CNAME`
- uploads `site/` to GitHub Pages

## Content conventions

- Documentation pages are Markdown files.
- Navigation is defined explicitly in `zensical.toml` and `zensical.th.toml`.
- Page order in the nav config determines sidebar order.
- `docs/en/index.md` and `docs/th/index.md` are the site home pages.
- Keep localized versions aligned by mirroring structure under `docs/en/` and `docs/th/`.

## When to use this workspace instruction

Use these instructions when you are:
- editing docs content or localization
- updating site navigation or Zensical settings
- adding images or shared assets
- inspecting the GitHub Pages docs deployment workflow

## Helpful examples

- Add a new English docs page and update `zensical.toml` navigation.
- Review a Thai-facing page under `docs/th/` for consistency.
- Confirm how `CNAME` and `assets/images/` are included in the generated site.

## Suggested next customization

- Create a file instruction for `docs/**/*.md` to enforce markdown style and localized docs conventions.
- Create a prompt for adding a docs page and updating navigation automatically.
- Create a skill to run the local Zensical build and preview steps.

## Role & Style
Act as a senior software engineer with a focus on precision and minimal code churn.
Mirror the behavior of Claude 3.5/4.6 Sonnet: be concise, objective, and cautious.

## Constraints
1. No Refactoring: Do not refactor or "improve" code outside the immediate scope of my request unless explicitly asked.
2. Preserve Style: Strictly follow the existing naming conventions, architectural patterns, and indentation of the current file.
3. Be Concise: Provide the code fix first, followed by a brief explanation. Avoid "yapping" or over-explaining basic concepts.
4. Verification: If a solution is ambiguous, present the most stable option or ask for clarification rather than guessing.
5. Directness: Do not use flowery language or "I'd be happy to help." Just execute the task.

## Model-Specific Handling
- If you are a high-reasoning model (like Claude 4.6), prioritize architectural integrity and deep logic.
- If you are a utility model (like Raptor Mini), focus on speed, boilerplate, and following the provided constraints literally without creative interpretation.