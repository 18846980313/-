---
name: li-web-project
description: Enforces this static HTML/CSS course project's conventions — native html/css/js only, local iconfont icons, no cdn or third-party libs, lj_ prefixed names, page header comments, zh-CN pages, prompt logging, git workflow. Use when editing html/css files, creating practice pages, or running git operations. Not for other projects.
---

# li-web-project

Static HTML/CSS course project. No build tooling — edit files directly; changes are live on refresh.

## Conventions

- All CSS class names, id names, and JS variables MUST start with `lj_` (e.g., `lj_container`, `lj_header`, `lj_init`).
- Every new HTML page MUST include a comment near the top (first line of `<head>` or `<body>`): `<!-- 姓名：李佳，建立时间：YYYY-MM-DD，大模型：<使用的大模型名称>，功能：页面功能名称 -->`
- Content language is Chinese (`lang="zh-CN"`); preserve it when editing or creating pages.
- Follow existing page patterns: inline `<style>` in `<head>`, `Microsoft YaHei` font stack, `max-width` centered `.container`.
- Implement pages with native HTML, CSS and JavaScript ONLY — no third-party libraries, no CDN references.
- Icons must use the local iconfont in the `font/` directory (e.g. link `font/iconfont.css` or use the SVG symbols from `font/`).

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
4. Push only when the user explicitly requests it. Remotes:
   - `origin` — Gitee, `https://gitee.com/Better-Lijia/lj.git` — user says "推送 / 推gitee / 推送到 Gitee"
   - `github` — GitHub, `ssh://git@ssh.github.com:443/18846980313/-.git` — user says "提交到github / 推github" (SSH key configured; port 22 is blocked, SSH must go over port 443 via ssh.github.com)
