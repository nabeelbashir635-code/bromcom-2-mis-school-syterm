# AegisSchool MIS (Single-file)

Open `index.html` in your browser to run the single-file Management Information System (MIS).

Features
- Authentication (local, role-based)
- Student management (add/view, points, detention)
- Attendance marking (P/L/A per day)
- Behaviour logs with auto-detention rules
- Timetable editor (Mon–Fri, P1–P5)
- Assessments (subject/mark records)
- CSV export for attendance & behaviour
- PA text-to-speech announcements
- Data persisted to `localStorage`

Getting started
1. Open `index.html` directly in your browser.
2. Create an account (or use demo/demo123).
3. Use the sidebar to navigate pages.

Notes
- Works offline; no server required.
- Demo credentials: `demo` / `demo123` (role: Teacher).
- Passwords are stored in localStorage (not secure) — for demo/education only.

Deploy
- Upload `index.html` to GitHub Pages, Vercel, Netlify, or static hosting.

Publishing (quick)

- GitHub Pages (simple):
	1. Push this repository to GitHub.
	2. Go to the repo Settings → Pages → Source and select the `main` branch root.
	3. The site will be available at `https://<your-user>.github.io/<repo>` shortly.

- Netlify / Vercel: drag-and-drop `index.html` or connect the repo — they will deploy automatically.

Local preview

```bash
# quick local server using Python 3
python3 -m http.server 8000
# then open http://localhost:8000/index.html
```

SEO & sharing tips
- Update the `<title>` and `<meta name="description">` in `index.html` to match your organisation and keywords.
- Add a README and project description on GitHub so people can find the repo.
- Use social previews (OpenGraph tags are included) when sharing links.

Keeping the site up (high availability)

To keep the static site available and resilient:

- Deploy to GitHub Pages (workflow included) and enable Cloudflare in front of the Pages site for CDN caching and DDoS protection.
- Optionally deploy to a second provider (Netlify) for DNS failover or multi-origin setups — the workflow supports an optional Netlify deploy when you add `NETLIFY_AUTH_TOKEN` and `NETLIFY_SITE_ID` as repository secrets.
- Use Cloudflare's "Always Online" and caching to serve cached pages if the origin is down.
- Add an external uptime monitor (UptimeRobot, Freshping, Pingdom) to alert you if the site becomes unreachable.
- Set up DNS failover or load balancing (Cloudflare Load Balancer or a DNS provider that supports health checks) to switch traffic to a backup origin automatically.

Quick steps:

1. Push repo to GitHub. The included GitHub Actions workflow (`.github/workflows/deploy.yml`) will publish `index.html` to GitHub Pages on every push to `main`.
2. In GitHub, go to Settings → Pages to confirm the published URL.
3. Add the Pages site to Cloudflare and enable caching + Always Online.
4. (Optional) Create a Netlify site and add `NETLIFY_AUTH_TOKEN` and `NETLIFY_SITE_ID` to repository Secrets to enable the optional deploy step.
5. Add an uptime monitor (free tiers available) to get alerts and reduce downtime.

These steps give you a static site served from a fast CDN and a secondary origin, plus monitoring and automatic redeploys, greatly reducing the chance of visible downtime.

If you want I can:
- Add sample student data
- Improve CSV format and add more exports
- Add small UI polish or accessibility fixes
# bromcom-2-mis-school-syterm
it is a attendance behavior detention 
