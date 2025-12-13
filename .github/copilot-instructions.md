# Pneu Forte - Sistema de Análise de Pneus Instructions

This document provides instructions for AI coding agents to effectively contribute to the Pneu Forte project.

## Project Overview

This is a static web application for managing and analyzing scrapped tires. It's built with plain HTML, and styled with Tailwind CSS. Interactive charts are rendered using Plotly.js.

The entire application is contained within the `pneus-sucateados/` directory. There is no build process or backend code in this repository; all files are static assets.

## Key Files and Structure

- `pneus-sucateados/`: The root directory for the application.
- `pneus-sucateados/*.html`: Each HTML file represents a different page or view in the application (e.g., `main.html` is the dashboard, `clientes.html` manages clients).
- `pneus-sucateados/main.html`: The main dashboard page. This is a good reference for the overall layout, including the header and sidebar that are reused across pages.

## Development Workflow

1.  **Styling**: The project uses Tailwind CSS via a CDN. All styling is done using Tailwind's utility classes directly in the HTML. Custom styles and theme extensions are defined in a `<style>` block in the `<head>` of each HTML file. When adding new UI elements, conform to the existing color palette (`primary`, etc.) and design patterns.

2.  **Navigation**: The application is a collection of static HTML pages. Navigation between pages is handled by standard anchor (`<a>`) tags. The main navigation menu is in the `<aside>` element in each HTML file. When adding a new page, ensure you add a link to it in the sidebar navigation on all other relevant pages.

3.  **Charting**: The dashboard (`main.html`) uses Plotly.js to render charts. The chart data is currently hardcoded in the `<script>` tag at the bottom of the file. See `main.html` for examples of how to create bar, pie, and line charts.

4.  **Icons**: The project uses Font Awesome for icons, included via a CDN. Use `<i>` tags with the appropriate Font Awesome classes to add icons.

## How to Add a New Page

1.  Create a new `.html` file in the `pneus-sucateados/` directory.
2.  Copy the basic structure from an existing file like `clientes.html` or `main.html`. This includes the `<!DOCTYPE>`, `<head>` (with CSS and JS links), and the main layout with `<header>`, `<aside>`, and `<main>`.
3.  Update the `<aside>` navigation section in *all* HTML files to include a link to your new page, ensuring the active state is correctly applied on the new page itself.
4.  Build the content for your new page within the `<main>` element using HTML and Tailwind CSS classes.
