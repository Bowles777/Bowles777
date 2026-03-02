# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a GitHub profile README repository for the GitHub user `Bowles777`. The sole content file is `README.md`, which renders on the GitHub profile page. There are no build steps, dependencies, or tests — changes are deployed by pushing to `main`.

## Architecture

- **`README.md`** — The GitHub profile page. Written in HTML/Markdown with shields.io badges. Structured into sections: intro, skills, education, and contribution snake animation.
- **`.github/workflows/snake.yml`** — GitHub Action that runs daily (cron `0 0 * * *`) and on manual dispatch. Uses `Platane/snk@v3` to generate contribution grid SVGs, then pushes them to the `output` branch via `crazy-max/ghaction-github-pages@v3`. The README references these SVGs from the `output` branch.

## Badge Convention

All shields.io badges use `style=flat-square`. Skill category colors:
- Languages: `#c8873a`
- Frameworks: `#a06b28`
- Testing: `#666666`
- Tools & DevOps: `#2d2d2d`
- Management & Design: `#1a1a1a`

## Snake Workflow

To manually trigger the snake SVG regeneration, go to **Actions → Generate Contribution Snake → Run workflow** in the GitHub UI, or push to `main`. The SVGs are committed to the `output` branch and served via `raw.githubusercontent.com`.
