# FoxDocs Guide

This guide is intended for an AI or new contributor with no prior memory of this repo. It summarizes the repository purpose, Zensical configuration, localization layout, build process, and where to add or update documentation.

## Repo purpose

- This repository is a Zensical-based documentation site for FoxConnect.
- It publishes an English site and a Thai site.
- The docs are built and deployed to GitHub Pages using a GitHub Action.

## Site structure

- `docs/en/` contains the English documentation content.
- `docs/th/` contains the Thai documentation content.
- `assets/images/` contains shared image assets used by both sites.
- `site/` is the generated output directory produced by Zensical builds.

## Key config files

- `zensical.toml`
  - Primary English site configuration.
  - `docs_dir = "docs/en"`
  - `site_url = "https://docs.foxconnect.app"`
  - `language = "en"`
  - Defines navigation order explicitly in `nav = [...]`.
  - Adds extra CSS from `stylesheets/nav-always-expanded.css`.

- `zensical.th.toml`
  - Thai site configuration.
  - `docs_dir = "docs/th"`
  - `site_dir = "site/th"`
  - `site_url = "https://docs.foxconnect.app"`
  - `language = "th"`
  - Uses the same navigation structure as English.

- `.github/workflows/docs.yml`
  - Trigger: push to `master` or `main`.
  - Steps:
    - Checkout repository.
    - Setup Python 3.x.
    - Install Zensical via `pip install zensical`.
    - Build English site: `zensical build --clean`.
    - Build Thai site: `zensical build --clean -f zensical.th.toml`.
    - Copy shared images into `site/assets/images/`.
    - Copy `CNAME` into `site/CNAME`.
    - Upload `site/` artifact and deploy to GitHub Pages.

## Documentation layout

English pages:
- `docs/en/index.md`
- `docs/en/Get_Started/index.md`
- `docs/en/Get_Started/1-setup-you-business-info.md`
- `docs/en/Get_Started/2-how-to-add-working-hours.md`
- `docs/en/Get_Started/3-how-to-setup-line-oa.md`
- `docs/en/Get_Started/4-create-line-liff.md`
- `docs/en/Get_Started/5-get-booking-system-link.md`
- `docs/en/Configure/index.md`
- `docs/en/Configure/add-branches.md`
- `docs/en/Configure/add-staff.md`
- `docs/en/Configure/adding-services.md`
- `docs/en/Configure/course_booking.md`
- `docs/en/Configure/event-booking-tickets.md`

Thai pages mirror the same structure under `docs/th/`.

## Localization and URLs

- English site builds to `site/`.
- Thai site builds to `site/th/`.
- English home page: `/index.html`.
- Thai home page: `/th/index.html`.
- Navigation is explicitly defined; adding new articles requires updating the appropriate `nav` list in `zensical.toml` and `zensical.th.toml`.

## Recommended update workflow

1. Add or edit Markdown content in `docs/en/` or `docs/th/`.
2. Keep English and Thai structures aligned if both languages are needed.
3. Update navigation objects in `zensical.toml` and `zensical.th.toml`.
4. Run local build to verify:
   - `zensical build --clean`
   - `zensical build --clean -f zensical.th.toml`
5. Commit changes and push to `main`/`master`.
6. GitHub Actions will rebuild and deploy automatically.

## Notes for this repo

- Both Zensical configs use explicit `nav` arrays, so the sidebar order is controlled by the TOML files.
- `extra_css` is used for layout styling in both languages.
- The workflow copies shared images and `CNAME` after build, ensuring the generated site includes branding assets and custom domain settings.
- The Thai site `site_dir` is nested inside `site/th`, so the final published site contains both languages under the same `site` artifact.

## Useful files

- `README.md` — repo overview.
- `zensical.toml` — English site config.
- `zensical.th.toml` — Thai site config.
- `.github/workflows/docs.yml` — build and deploy automation.
- `docs/en/` and `docs/th/` — Markdown content.
- `assets/images/` — shared assets copied into the published site.
