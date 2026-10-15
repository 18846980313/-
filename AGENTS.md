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

- All CSS class names, id names, and JS variables must start with `li` (e.g., `li-container`, `li-header`, `liInit`).

## Prompt logging

- Before executing any user prompt, append it to `li_prompt.md` with: timestamp, model name, and full prompt content. Never overwrite existing entries.

## Notes

- Content language is Chinese (`lang="zh-CN"`); preserve this when editing or creating pages.
- Follow existing page patterns: inline `<style>` in `<head>`, `Microsoft YaHei` font stack, `max-width` centered `.container`.
