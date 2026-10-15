---
name: li-web-project
description: Use when working on this static HTML/CSS course project. Covers naming conventions, page patterns, prompt logging, and commit/push workflow. Trigger when editing html/css files, creating practice pages, or running git operations.
---

# li-web-project

Static HTML/CSS course project. No build tooling — edit files directly.

## Conventions

- All CSS class names, id names, and JS variables MUST start with `li` (e.g., `li-container`, `li-header`, `liInit`).
- Content language is Chinese (`lang="zh-CN"`); preserve it when editing or creating pages.
- Follow existing page patterns: inline `<style>` in `<head>`, `Microsoft YaHei` font stack, `max-width` centered `.container`.

## Page Structure

- `index.html` — gallery entry; all practice pages MUST be linked from it.
- `N-M.html` — individual course practice pages (e.g., `1.html`, `2-1.html`, `10-3.html`).
- `css.css` — minimal shared stylesheet; only `5-1.html` links it externally. All others use inline `<style>` blocks.

## Workflow

### Prompt logging (REQUIRED before every user prompt)

Append each prompt to `li_prompt.md` with: timestamp, model name, and full prompt content. Never overwrite existing entries.

### Git workflow

1. `git add` intended files only — never commit secrets.
2. Write a concise commit message matching the repo style.
3. Before push: inspect status, diff, and recent commits.
4. Push to the configured remote only when the user explicitly requests it.
