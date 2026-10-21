# Visitor Globe — example

A rotating globe showing where your visitors are, with a glowing dot per country. Hover a dot for the country name and its visit count. Refreshes every 15 to 30 seconds.

No cookies. No signup. One script tag.

## Quick start

Get a site ID from https://feed-pulse.com (free, no card), then paste:

```html
<script async src="https://feed-pulse.com/api/embed/visitor-globe.js?site_id=YOUR_SITE_ID"></script>
Options
Param	Values	Default
map	globe, flat	globe
sz	sm, md, lg	md
theme	sky, obsidian, indigo, ivory, neon and more	sky
speed	off, slow, normal, fast, turbo	normal
Flat map, dark theme, static:

<script async src="https://feed-pulse.com/api/embed/visitor-globe.js?site_id=YOUR_SITE_ID&map=flat&theme=obsidian&speed=off"></script>
Privacy
Resolution is country-level only — never a city, street or individual visitor. No tracking cookies are set, which is why this widget does not oblige you to add a cookie banner. Visitor IPs are hashed with a daily-rotating salt, used only to derive a country code, then discarded. Country lookup runs against a local database rather than a third-party geolocation API, so visitor IPs are never sent to an outside service.

Live customizer
https://feed-pulse.com/free-visitor-globe-widget

License
MIT


**Commit changes**.

## Step 2.3 — Add index.html

**Add file ▾ → Create new file**, filename `index.html`, paste:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Visitor Globe — example</title>
  <style>
    body { font-family: ui-sans-serif, system-ui, sans-serif; max-width: 42rem; margin: 4rem auto; padding: 0 1.5rem; line-height: 1.6; }
    h1 { font-size: 1.5rem; margin-bottom: .25rem; }
    p { color: #555; }
    .globe-slot { margin: 2.5rem 0; }
  </style>
</head>
<body>
  <h1>Visitor Globe</h1>
  <p>Glowing dots where your visitors are. Country-level only, no cookies.</p>

  <div class="globe-slot">
    <script async src="https://feed-pulse.com/api/embed/visitor-globe.js?site_id=demo"></script>
  </div>

  <p>Replace <code>site_id=demo</code> with your own.
     Themes and flat-map mode: <a href="https://feed-pulse.com/free-visitor-globe-widget">customizer</a>.</p>
</body>
</html>
