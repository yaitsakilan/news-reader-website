# 🏗️ Architecture & Design Guide

This document describes the architectural layout, core design choices, and CSS patterns used to build the static **News Reader Website** project.

---

## 🎨 Layout & UI Architecture

The application is a multi-page static site designed around classic news mastheads. It relies on a few key layout strategies:

### 1. Traditional Newspaper Grid (`mainpage.html`)
The landing page displays top news in a horizontal grid structure using a borderless `<table>` with `cellspacing="50"`.
- **Odisha Train Tragedy** (Left Cell) and **IPL Final** (Right Cell) are positioned in two sibling `<td>` elements.
- The `tops01` class provides padding and size guidelines for consistent alignment.
- A float-based sidebar layout is used for the detailed featured story.

### 2. Hub-and-Spoke Navigation (`city.html`)
The regional section is structured as a hub page (`city.html`) containing high-level summaries and navigation to detailed city reports:
- [Chennai Page (Pen Monument Controversy)](file:///d:/news-reader-website/web/chennai.html)
- [Coimbatore Page (DIG News Report)](file:///d:/news-reader-website/web/coimbatore.html)
- [Mumbai Page (Multi-City Section Layout)](file:///d:/news-reader-website/web/mumbai.html)

### 3. Split-Screen Layout (`mumbai.html`)
The `mumbai.html` page implements a split-screen design:
- **Left Column:** A fixed-position background image container (`.class`) occupying 50% of the screen width and 100% of the viewport height.
- **Right Column:** A scrollable text container with a `margin-left: 50%` offset for the news content.

---

## 💅 CSS Stylesheet Patterns (`cssfile.css`)

The stylesheet defines the visual hierarchy and interaction rules:

### 1. Pure-CSS Dropdown Navigation
The dropdown menu is built entirely without JavaScript using standard CSS selectors:
- The sub-menu `div` has `.dropdown-content` set to `display: none` by default.
- When hovering over the parent `li.dropdown`, the selector `.dropdown:hover .dropdown-content` changes the display mode to `display: block`.
- Dynamic shadow properties (`box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2)`) and relative/absolute positioning provide context styling over background elements.

### 2. Newspaper Typography
- **Masthead Font:** Standard sans-serif typeface configured with an ultra-wide letter spacing (`letter-spacing: 10px`) to recreate a press header style.
- **Category Indicators:** Decorative underlines and bold caps indicate news genres (e.g. "TOP NEWS" using `font-family: Stencil`).

---

## 📈 Future Modernization Roadmap

While the current setup works exceptionally well for static showcase layouts, future upgrades can incorporate:
1. **Transition to CSS Grid:** Replace HTML `<table>` cells with modern `display: grid` containers for better responsive grid control.
2. **Shared Layout Header:** Migrate layout headers to reusable JavaScript components or templating tools to avoid repeating navigation code across pages.
