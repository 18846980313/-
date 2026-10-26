# AGENTS.md

## Project type

Pure static HTML/CSS site — no build tooling, package manager, framework, or tests. Edit files directly; changes are live on refresh.

## Structure

- `index.html` — entry point; gallery linking to practice pages. New pages MUST be linked from this gallery
- `N-M.html` (e.g. `1.html`, `2-1.html`, `10-3.html`) — individual course practice pages
- `学习强国.html` — saved copy of the xuexi.cn page; references a `学习强国_files/` asset directory that is not present in this repo
- `css.css` — minimal shared stylesheet; only `5-1.html` links it externally. All other pages use inline `<style>` blocks.
- `*.png`, `第一个网页.mp4` — image/video assets referenced by the pages

## Naming conventions

- All CSS class names, id names, and JS variables must start with `lj_` (e.g., `lj_container`, `lj_header`, `lj_init`).

## Page header comment

- Every new HTML page must include a comment near the top (first line of `<head>` or `<body>`) with author, creation date, AI model used, and feature name: `<!-- 姓名：李佳，建立时间：YYYY-MM-DD，大模型：<使用的大模型名称>，功能：页面功能名称 -->`

## Technology constraints

- All pages must be implemented with native HTML, CSS and JavaScript only — no third-party libraries, no CDN references.
- Icons must use the local iconfont in the `font/` directory (e.g. link `font/iconfont.css` or use the SVG symbols from `font/`).

## Git remotes

- `origin` — Gitee: `https://gitee.com/Better-Lijia/lj.git` — push when the user says 推送/推gitee.
- `github` — GitHub: `git@github.com:18846980313/-.git` — push when the user says 提交到github/推github. SSH public key is configured.
- Commit and push only when the user explicitly requests it.

## Prompt logging

- Before executing any user prompt, append it to `li_prompt.md` with: timestamp, model name, and full prompt content. Never overwrite existing entries.

## Notes

- Content language is Chinese (`lang="zh-CN"`); preserve this when editing or creating pages.
- Follow existing page patterns: inline `<style>` in `<head>`, `Microsoft YaHei` font stack, `max-width` centered `.container`.
