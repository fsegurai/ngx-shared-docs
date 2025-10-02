<p align="center" class="intro">
  <img alt="NGX Docs Shared Logo" src="https://raw.githubusercontent.com/fsegurai/ngx-shared-docs/main/public/ngx-shared-docs.png">
</p>

<p align="center" class="intro">
  <a href="https://github.com/fsegurai/ngx-shared-docs">
      <img src="https://img.shields.io/azure-devops/build/fsegurai/93779823-473d-4fb3-a5b1-27aaa1a88ea2/22/main?label=Build%20Status&"
          alt="Build Main Status">
  </a>
  <a href="https://github.com/fsegurai/ngx-shared-docs/releases/latest">
      <img src="https://img.shields.io/github/v/release/fsegurai/ngx-shared-docs"
          alt="Latest Release">
  </a>
  <br>
  <img alt="GitHub contributors" src="https://img.shields.io/github/contributors/fsegurai/ngx-shared-docs">
  <img alt="Dependency status for repo" src="https://img.shields.io/librariesio/github/fsegurai/ngx-shared-docs">
  <a href="https://opensource.org/licenses/MIT">
    <img alt="GitHub License" src="https://img.shields.io/github/license/fsegurai/ngx-shared-docs">
  </a>
  <br>
  <img alt="Stars" src="https://img.shields.io/github/stars/fsegurai/ngx-shared-docs?style=square&labelColor=343b41"/> 
  <img alt="Forks" src="https://img.shields.io/github/forks/fsegurai/ngx-shared-docs?style=square&labelColor=343b41"/>
  <a href="https://www.npmjs.com/package/@fsegurai/ngx-shared-docs">
    <img alt="NPM Downloads" src="https://img.shields.io/npm/dt/@fsegurai/ngx-shared-docs">
  </a>
</p>

`@fsegurai/ngx-shared-docs` is an [Angular](https://angular.dev/) library that combines...

`@fsegurai/ngx-shared-docs` is a modern [Angular](https://angular.dev/) library providing reusable components,
directives, pipes, and utilities for documentation sites and developer portals. It is built with Angular v20+, embracing
signals, standalone components, and the latest best practices for performance and maintainability.

## Table of Contents

- [Features](#features)
- [Library Structure](#library-structure)
    - [Components](#components)
    - [Constants](#constants)
    - [Directives](#directives)
    - [Icons](#icons)
    - [Interfaces](#interfaces)
    - [Pipes](#pipes)
    - [Providers](#providers)
    - [Services](#services)
    - [Styles](#styles)
    - [Types](#types)
    - [Utils](#utils)
- [Installation](#installation)
- [Usage](#usage)
    - [Basic Usage](#basic-usage)
- [Development Guidelines](#development-guidelines)
- [Demo](#demo)
- [Contributing](#contributing)
- [License](#license)

---

## Features

- **Reusable UI Components**: Banner, cookie popup, clipboard button, icon, select, table of contents (TOC) navigation, doc viewer,
  and more.
- **Directives**: Click outside, and external link.
- **Pipes**: Common pipes for documentation needs.
- **Providers & Services**: Content loader, markdown, local storage, anchor navigation, raw HTTP loader.
- **Utilities**: Device detection, analytics, navigation, markdown factory, URL helpers.
- **Styles**: SCSS partials for theming, resets, typography, and component styles.
- **SVG Icons**: Ready-to-use icons for documentation UIs.

---

## Library Structure

The `@fsegurai/ngx-shared-docs` library is organized into the following categories:

### Components
Reusable UI components for building documentation sites:
- **ClipboardButton**: Button to copy text to clipboard.
- **CookiePopup**: Cookie consent popup.
- **DocsViewer**: Renders documentation content.
- **Icon**: SVG icon renderer.
- **Select**: Custom select dropdown.
- **TableOfContents**: Navigation for table of contents.
- **Tooltip**: Tooltip component.
- **TopLevelBanner**: Displays a banner at the top of the page.

### Constants
Predefined constants for consistent usage:
- **StorageKeys**: Keys for local storage management.

### Directives
Custom directives to enhance functionality:
- **ClickOutsideDirective**: Detects clicks outside an element.
- **ExternalLinkDirective**: Marks links as external.

### Icons
SVG icons for documentation UIs:
- **chevron-down.svg**
- **chevron-up.svg**
- **discord.svg**
- **github.svg**
- **youtube.svg**

### Interfaces
Type definitions for structured data:
- **DocContent**: Interface for documentation content.
- **DocsContentLoader**: Interface for content loader.
- **Languages**: Supported languages.
- **Select**: Select component options.
- **TableOfContentsItem**: Table of contents structure.
- **Themes**: Theme definitions.

### Pipes
Reusable pipes for transforming data:
- Various pipes for formatting and transforming documentation data.

### Providers
Dependency injection providers:
- **DocsContentLoader**: Loads documentation content.
- **LocalStorage**: Manages local storage.
- **Markdown**: Renders Markdown using its respective configuration and specified extensions.
- **Window**: Provides window-related utilities.

### Services
Singleton services for application logic:
- **AnchorService**: Handles anchor navigation.
- **HttpRawLoaderService**: Loads raw HTTP content.
- **TableOfContentsLoaderService**: Loads table of contents.

### Styles
SCSS partials for theming and styling:
- **_api-item-label.scss**
- **_button.scss**
- **_colors.scss**
- **_media-queries.scss**
- **_resets.scss**
- **_typography.scss**
- **_utils.scss**
- **_z-index.scss**
- **global-styles.scss**
- **components/**: Component-specific styles.
- **docs/**: Documentation-specific styles.
- **themes/**: Theme management styles.

### Types
Type definitions for structured data:
- **SelectOptionValue**: Type for select options.

### Utils
Utility functions for common tasks:
- **animations.utils.ts**: Animation utilities.
- **device.utils.ts**: Device detection utilities.
- **html-sanitizer.utils.ts**: HTML sanitizer utilities.
- **markdown.utils.ts**: Markdown rendering utilities.
- **markdown-factory.utils.ts**: Markdown generation helpers.
- **navigation.utils.ts**: Navigation helpers.
- **url.utils.ts**: URL manipulation utilities.

---

## Installation

Install the library via npm:

```bash
npm install @fsegurai/ngx-shared-docs --save
```

## Usage

### Basic Usage

All components are standalone and use signals for state management. Import them directly in your Angular app:

```typescript
import {TopLevelBannerComponent, ClipboardButtonComponent} from '@fsegurai/ngx-shared-docs/components';

@Component({
    selector: 'app-root',
    imports: [TopLevelBannerComponent, ClipboardButtonComponent],
    template: `
    <ngx-docs-top-level-banner text="Welcome to NGX Shared Docs!" />
    <ngx-docs-clipboard-button [text]="'Copy this text!'" />
  `,
    changeDetection: ChangeDetectionStrategy.OnPush,
})
export class AppComponent {
}
```

---

## Development Guidelines

This section outlines the best practices and coding standards followed in this library to ensure maintainability, performance, and modern Angular paradigms.

### Angular Version
This library is built with Angular v20+ and leverages the latest features, including:
- **Signals** for reactive state management.
- **Standalone Components** for streamlined architecture.
- **Native Control Flow** for intuitive template logic.

### Coding Standards
- **TypeScript**:
  - Use strict type checking.
  - Prefer type inference when the type is obvious.
  - Avoid the `any` type; use `unknown` when type is uncertain.
- **Angular**:
  - Always use standalone components over `NgModules`.
  - Use signals for state management.
  - Implement lazy loading for feature routes.
  - Use `NgOptimizedImage` for all static images.

### Components
- Keep components small and focused on a single responsibility.
- Use `input()` signals and `output()` functions instead of decorators.
- Use `computed()` for derived state.
- Set `changeDetection: ChangeDetectionStrategy.OnPush` in `@Component` decorator.
- Prefer inline templates for small components.
- Prefer Reactive forms instead of Template-driven ones.

### Templates
- Keep templates simple and avoid complex logic.
- Use native control flow (`@if`, `@for`, `@switch`) instead of `*ngIf`, `*ngFor`, `*ngSwitch`.
- Use the async pipe to handle observables.
- Use built-in pipes and import pipes when being used in a template.

### Services
- Design services around a single responsibility.
- Use the `providedIn: 'root'` option for singleton services.
- Use the `inject()` function instead of constructor injection.

### State Management
- Use signals for the local component state.
- Use `computed()` for derived state.
- Keep state transformations pure and predictable.

### Styles
- Use SCSS partials for theming and styling.
- Follow the Angular Style Guide for consistent naming and structure.

For more details, refer to the [Angular Style Guide](https://angular.dev/style-guide).

---

## Demo

See the components in action: [Demo](https://fsegurai.github.io/ngx-shared-docs)

To run the demo locally:

```bash
git clone https://github.com/fsegurai/ngx-shared-docs.git
bun install
bun start
```

The app will be served at [http://localhost:4200](http://localhost:4200).

## Contributing

Contributions are welcome! Please follow the [Angular Style Guide](https://angular.dev/style-guide) and use signals,
standalone components, and the latest Angular features.

## License

Licensed under [MIT](https://opensource.org/licenses/MIT).