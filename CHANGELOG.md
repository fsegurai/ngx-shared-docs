# 📦 Changelog

All notable changes to this project will be documented in this file.  
This project adheres to [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)

---

## [Unreleased]

No changes have been made yet.

---

## [20.0.0] - 2025-xx-xx

### 🚀 Features

- **Clipboard Button Component** — A reusable button for copying text to the clipboard.
- **Cookie Popup Component** — A customizable cookie consent banner.
- **Docs Viewer Component** — A component for rendering and navigating documentation content.
- **Table Of Contents Component** — Automatically highlights navigation items based on scroll position.
- **Top-Level Banner Component** — A banner for displaying important announcements.
- **Directives** — Added `ClickOutsideDirective` and `ExternalLinkDirective` for enhanced interactivity.
- **Utility Functions** — Added utilities for analytics, animations, device detection, and URL handling.
- **Theming Support** — Introduced SCSS variables and mixins for consistent theming.
- **Icons** — Added SVG icons for common use cases (e.g., GitHub, YouTube, Discord).
- **Providers** — Added services for managing local storage, markdown rendering, and window interactions.
- **Pipes** — Added reusable pipes for transforming data in templates.
- **Interfaces** — Defined TypeScript interfaces for consistent data modeling.

### 🛠 Changed

- Refactored components to use Angular standalone architecture.
- Updated all components to leverage Angular signals for state management.
- Improved SCSS structure for better maintainability and reusability.
- Enhanced documentation for components, utilities, and directives.
- Optimized utility functions for better performance and reusability.

---

## 📦 Dependencies

### Runtime

- Angular 20+ — Leveraging the latest features like signals and standalone components.
- SCSS — For styling and theming.

### Development

- [`bun`](https://bun.sh/) — JS runtime and package manager.
- [`typescript`](https://www.typescriptlang.org/) — Static type checking.
- [`eslint`](https://eslint.org/) — Code linting and formatting.
- [`karma`](https://karma-runner.github.io/) — Test runner.
- [`jest`](https://jestjs.io/) — Testing framework.

---

## 🔁 Migration Guide

### From 0.x → 20.0.0

- Refactor components to use standalone architecture.
- Replace `@Input` and `@Output` decorators with signal-based inputs and outputs.
- Update templates to use Angular's native control flow (`@if`, `@for`, etc.).
- Update SCSS files to align with the new theming structure.

---

## 💥 Breaking Changes

- Components now require Angular 20+ due to the use of signals and standalone architecture.
- Removed support for `ngClass` and `ngStyle` in favor of class and style bindings.
- Updated utility function signatures for consistency.

---

## ✅ Compatibility

- ✅ Chrome
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Angular 20+ required
- ⚠️ Internet Explorer is **not supported**, try it on your own, but it probably won't work.

---

[unreleased]: https://github.com/fsegurai/ngx-shared-docs/compare/v20.0.0...HEAD

[20.0.0]: https://github.com/fsegurai/ngx-shared-docs/releases/tag/v20.0.0