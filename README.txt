BACDA Calgary website - hosting notes
=====================================

What this is
- A static website: plain HTML, CSS and JavaScript. No database, no server-side code,
  no build step, no plugins. It runs on any static web host (cPanel/Apache, Nginx,
  Netlify, Cloudflare Pages, GitHub Pages, S3, etc.).

Files
- index.html                     the whole site (all 8 pages)
- logo.jpg                       logo, also used as the browser-tab icon
- photos/*.jpg                   gallery photos
- photos/fundraiser-2018.mp4     video on the Events page (H.264/AAC, ~5 MB)

How to deploy
1. Upload everything in this folder, keeping the folder structure, to the web root
   (e.g. public_html/ or the site's root directory).
2. index.html must be the default document for the domain root.
3. Make sure .mp4 is served as video/mp4 (default on almost every host).
4. Enable HTTPS (e.g. a free Let's Encrypt certificate).

Notes
- Pages are switched with links like /#about and /#events, so no server rewrite
  rules are needed.
- Fonts load from Google Fonts (fonts.googleapis.com / fonts.gstatic.com). No other
  external services, cookies, tracking or forms.
- There is no contact form; visitors see the email address bacdacalgary@gmail.com.

Domain
- The domain (e.g. bacdacalgary.ca / .org) should point to this hosting via DNS
  (A/AAAA records or a CNAME, as the host specifies).
