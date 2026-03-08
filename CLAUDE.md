# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

PlusConsulting — a single-page marketing website for an AI-powered Account-Based Marketing agency. The entire site lives in a single `index.html` file with no build tools, frameworks, or dependencies.

## Architecture

- **Single file**: `index.html` contains all HTML, CSS (`<style>` block), and JavaScript (`<script>` block)
- **No build step**: Open `index.html` directly in a browser to preview
- **No package manager or dependencies** (external resource: Google Fonts Inter via CDN)

## Design System

- **Dark theme**: Background `#09090b`, text `#e4e4e7`, muted text `#a1a1aa`
- **Brand colors**: Purple gradient (`#6d28d9` → `#7c3aed`), teal accent (`#2dd4bf`), violet highlight (`#a78bfa`)
- **Gradient text**: Uses `.gradient-text` class (purple-to-teal via `background-clip: text`)
- **Typography**: Inter font, weights 400–800
- **Border radius**: Cards use `20px`, buttons `12px`, badges `999px`
- **Spacing**: `.container` max-width 1200px with 24px padding

## Interactive Behaviors (vanilla JS)

- **Mobile nav**: Hamburger toggles `.active` class on `#navLinks`
- **FAQ accordion**: Click toggles `.active` on `.faq-item`, only one open at a time
- **Scroll reveal**: IntersectionObserver adds `.visible` to `.reveal` elements (threshold 0.15)
- **Animated counters**: Stats section uses `data-target` and `data-suffix` attributes, animates on scroll with eased counting

## Responsive Breakpoints

- 1024px: Feature/step grids → 2 columns, stats → 2 columns
- 768px: Grids → 1 column, mobile hamburger nav shown, hero padding reduced
- 480px: Stats → 1 column
