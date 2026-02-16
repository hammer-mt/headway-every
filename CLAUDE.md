# Headway Tutorial Page

This is a recreation of a Headway therapist directory page, used for teaching the Headway marketing team how to use Claude Code.

## Tech Stack

- **Vanilla HTML, CSS, and JS only** — no frameworks, no build tools, no npm
- **No server needed** — just double-click `index.html` to open it in your browser
- All styles are inline in `<style>` tags within each HTML file
- All scripts are inline in `<script>` tags within each HTML file
- No external dependencies (no CDNs, no external CSS/JS files)

## File Structure

- `index.html` — Main therapist directory/listing page with search and filter
- `provider.html` — Individual therapist profile page (loaded via `?id=therapist-id` query param)
- `therapists.js` — Fake database of therapist data used by both pages (loaded via `<script src>`)
- `therapists.json` — Same data in JSON format (reference copy, not used at runtime)

## How It Works

- Both pages load `therapists.js` via a `<script src="therapists.js">` tag, which defines a global `THERAPISTS_DATA` array
- `index.html` dynamically renders therapist cards from `THERAPISTS_DATA`
- The **Zip code** input and **Insurance** dropdown filter the therapist list when "Find care" is clicked
- Each therapist card links to `provider.html?id=<therapist-id>` for the full profile
- `provider.html` reads the `id` query parameter and populates the profile from `THERAPISTS_DATA`

## Guidelines

- Use placeholder avatars (CSS gradient circles with initials) instead of real photos
- Maintain the same visual structure and layout as the original Headway care.headway.co pages
- Use the Headway brand green (#166534 for dark green, #16a34a for medium green) and their warm neutral palette
- To add a new therapist, add an entry to the `THERAPISTS_DATA` array in `therapists.js` — both pages will pick it up automatically
