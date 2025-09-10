# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev presentation project focused on "Data Engineering with Snowflake and AWS". Slidev is a slides maker and presenter designed for developers that uses Markdown for content and Vue.js for interactive components.

## Common Commands

### Development
- `pnpm install` - Install dependencies
- `pnpm dev` - Start development server at localhost:3030
- `pnpm build` - Build for production
- `pnpm export` - Export slides to PDF, PPTX, PNGs, or hostable SPA

### Package Manager
This project uses pnpm with workspace configuration. The `pnpm-workspace.yaml` specifies build-only dependencies for esbuild and playwright-chromium.

## Architecture & Structure

### Content Organization
- `slides.md` - Main presentation content with frontmatter configuration
- `pages/` - Additional slide pages that can be imported using `src` attribute
- Slides use YAML frontmatter for configuration (theme, background, transitions, etc.)

### Interactive Components
- `components/` - Custom Vue.js components available in slides
- Components use Vue 3 composition API with TypeScript
- UnoCSS is used for styling with utility classes (e.g., `flex="~"`, `border="~ main rounded-md"`)

### Code Integration
- `snippets/` - TypeScript code examples that can be embedded in slides
- Code blocks support syntax highlighting, TypeScript hover information, and live execution
- External code can be imported using `<<< @/snippets/filename.ts#region` syntax
- Monaco editor integration available with `{monaco}` and `{monaco-run}` annotations

### Slide Features
- Supports themes (currently using 'seriph' theme)
- Click animations with `v-click` directive
- Motion animations with `v-motion` and @vueuse/motion
- Draggable elements with `v-drag`
- LaTeX support via KaTeX
- Diagram support (Mermaid, PlantUML)
- Slide importing and organization

### Dependencies
- Vue 3.5+ for component system
- Slidev CLI for presentation engine
- Node.js 22.19.0 (managed by Volta)
- TypeScript support throughout
- Playwright for testing capabilities

## Deployment

### GitHub Pages Configuration
- Configured for deployment at subpath: `/data-engineering-with-snowflake-and-aws/`
- Uses hash router mode for GitHub Pages compatibility
- Base path set in `slides.md` frontmatter: `base: /data-engineering-with-snowflake-and-aws/`
- GitHub Actions workflow in `.github/workflows/deploy.yml` handles automatic deployment

### Custom Domain Setup
- Project is configured to be hosted at `slides.example.com/data-engineering-with-snowflake-and-aws`
- Router mode set to `hash` for static hosting compatibility
- Build artifacts are deployed to `dist/` directory via GitHub Actions