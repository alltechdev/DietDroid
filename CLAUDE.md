# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

DietDroid.com is a static HTML website for semi-dumb phones and minimalist Android devices. The site provides information, tools, and resources for simplified mobile devices with a focus on technical guides, device specifications, and minimal Android apps.

## Site Structure

This is a pure static HTML website with no build system or package managers. The structure is:

- **Root pages**: Main site pages (index.html, devices.html, privacy-policy.html, terms-of-use.html)
- **devices/**: Device-specific pages (f21-pro.html)
- **blog/**: Blog section with individual article pages and blog index
- **blog/images/**: Static images used in blog posts

All pages are standalone HTML files with embedded CSS and minimal JavaScript. No external dependencies, frameworks, or build tools are used.

## Common Development Tasks

Since this is a static HTML site with no build system:

### Local Development
- Serve files locally using any static web server (e.g., `python -m http.server`, `npx serve`, or Live Server extension)
- No compilation or bundling required - just open HTML files directly in a browser

### Adding New Content
- Create new HTML files following the existing template structure
- Copy CSS styles from existing pages to maintain consistency
- Follow the established meta tag patterns for SEO

### Modifying Styles
- All CSS is embedded within `<style>` tags in each HTML file
- No separate CSS files exist - updates need to be applied to each file
- The design uses a consistent blue gradient theme across all pages

## Code Architecture

### Page Template Structure
Each HTML page follows this pattern:
1. **SEO Meta Tags**: Comprehensive OpenGraph and Twitter card metadata
2. **Favicon**: Uses external Android icon from mintmygold.com
3. **Embedded CSS**: Custom styles with gradient backgrounds and responsive design
4. **Header**: Sticky navigation with mobile menu support
5. **Content**: Main content area with device cards, blog posts, or guides
6. **Footer**: Standard footer across all pages

### Design System
- **Color Scheme**: Blue gradient theme (#0d47a1, #1976d2, #1e3c72)
- **Typography**: System font stack (-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto)
- **Layout**: Responsive grid system with max-width containers
- **Mobile**: Collapsible hamburger menu for mobile navigation

### Content Types
- **Device Pages**: Technical specifications and features for semi-dumb phones
- **Blog Posts**: Technical guides and tutorials with step-by-step instructions
- **Static Pages**: Privacy policy, terms of use, and informational content

## SEO and Meta Tags

All pages include comprehensive SEO optimization:
- OpenGraph and Twitter card metadata
- Structured data for social sharing
- Canonical URLs and proper indexing directives
- Mobile-responsive viewport settings

## Asset Management

- **Images**: Stored in blog/images/ directory
- **External Resources**: Uses Android icon from external domain (mintmygold.com)
- **No Dependencies**: All CSS is self-contained, no external libraries or frameworks