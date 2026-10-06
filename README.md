# ToolBox v1.0

A lightweight static utility website. No database, accounts, backend, or server-side file storage is required.

## Included tools
- QR Code Generator
- Image Resizer
- Image Compressor
- Percentage Calculator
- PDF Merger

## Production additions in v1.0
- About, Privacy, Terms, Contact, and 404 pages
- favicon and consistent branding
- responsive navigation and footer
- SEO titles/descriptions and basic Open Graph metadata
- robots.txt and sitemap.xml templates
- reserved advertising space after each tool
- pinned QRCode.js 1.0.0 and pdf-lib 1.17.1 dependencies

## Before public launch
Search the project for `YOUR-DOMAIN.example` and replace it with your real domain. Update the placeholder contact email. Then uncomment and update the Sitemap line in `robots.txt`.

Open Graph `og:url` and `og:image` are intentionally not included yet because they require the final canonical domain/image URL. Add them after the domain is selected.

## Run locally
Open `index.html`, or use a simple static development server such as VS Code Live Server. The QR and PDF tools require internet access to load their pinned cdnjs libraries; the other tools have no external runtime dependency.

## Libraries
- QRCode.js 1.0.0 (MIT)
- pdf-lib 1.17.1 (MIT)

The pages load pinned versions from cdnjs. If you later self-host these libraries, update the two script references and keep the same pinned versions.

## Deploy
The project can be deployed to any static hosting service. For Cloudflare Pages with a Git repository, the site does not require a framework build step. Keep `index.html` at the deployed site root.

## Add a tool
1. Create the tool HTML file in `tools/`.
2. Create its focused JavaScript file in `js/`.
3. Reuse the existing `.tool-page` / `.tool-box` structure.
4. Add the tool to the homepage and related-tool navigation.
5. Add its public URL to `sitemap.xml`.

## Privacy note
The current image and PDF tools use browser APIs for client-side processing. If analytics, advertising, uploads, accounts, or backend services are introduced later, review and update the Privacy Policy before launch of those features.
