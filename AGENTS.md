# Repository Guidelines

## Project Structure & Module Organization

This is a small, dependency-free collection of shelf design pages. `shelf-design.html` documents the 15 × 15 mm profile; `shelf-design-10x20.html` documents the separate 10 × 20 mm version. Each page contains its own CSS, SVG diagrams, cut list, and assembly notes. `assets/` holds the box, caster, and profile reference images. `README.md` compares the two designs. There is no application source directory or test directory.

## Build, Test, and Development Commands

No build step, package manager, or formatter is configured. Open either HTML file directly, or run `python3 -m http.server 8765` from the repository root and visit `http://localhost:8765/shelf-design.html` or `/shelf-design-10x20.html`. Run `git diff --check` before submitting changes to catch whitespace errors.

## Coding Style & Naming Conventions

Follow the existing two-space HTML indentation and keep CSS and SVG in the page they describe. Use descriptive lowercase, hyphenated file names such as `shelf-design-10x20.html`. Keep dimensions in millimetres and update related SVG labels, captions, cut lengths, and README values together. Give diagrams a `<title>` and `<desc>`; provide `alt` text for images. Preserve both variants when editing one.

## Testing Guidelines

There is no automated test suite or coverage target. Check both pages in a browser after visual edits, including narrow-screen layout and print view when affected. Confirm local image and page links resolve. Recalculate the outer dimensions, five support elevations, box clearance, total height, and stock-cut totals after changing geometry. Treat load capacity and connector fit as unverified until checked against the actual parts.

## Commit & Pull Request Guidelines

The initial commit uses the simplified Angular format `feat(shelf): 添加双盒五层移动货架设计`. Continue with `<type>(shelf): <concise Chinese imperative summary>`, for example `docs(shelf): 更新层距标注`. Keep commits scoped to the changed design. Pull requests should describe the affected variant, dimension changes, and checks performed; include before/after screenshots for diagram changes and link an issue when one exists.
