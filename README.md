# My Customisable Site

A single-file, no-build website with a **looping video/image background** and a built-in visual editor. Open it, tweak everything from a side panel, then **download a finished, self-contained site** you can host anywhere.

No frameworks, no installs, no internet required — it's one `index.html` file.

---

## Quick start

1. Double-click **`index.html`** to open it in any modern browser.
2. Click **Customise** (top-right) to open the editor panel.
3. Change text, colours, background, animations and social links — everything updates live.
4. Click **Download My Site** to save a ready-to-use copy with all your choices baked in.

---

## Features

### Background
- **Import Video / Photo / GIF** — pick any local file. Videos **loop** the entire time the page is open.
- **Default background colour** — shown when no media is set.
- **Background brightness** — a dark overlay slider so text stays readable over busy videos.
- **Mute / unmute** the background video (videos must start muted to autoplay — that's a browser rule).
- **Clear Media** to remove the imported background.

### Animations
- **Startup animation** — plays once when the site opens: *Fade in, Slide up/down, Zoom in, Blur in, Drop in.*
- **Animation speed** slider.
- **Continuous motion** — always-on movement: *Float, Pulse, Sway, Glow.*
- **Startup video** — import a video that plays full-screen **once** on load, then fades into the site (click it to skip).
- **Replay** — a button on the page re-plays the intro/animation **without reloading** the page.

### Text
- Editable **title** and **subtitle**.
- **Optional button** ("Get Started") with a **Show the button** toggle (off by default), custom **text**, and a custom **link** (URL opens in a new tab, `#anchor` works too).

### Colours
- Pickers for **accent/button**, **title text**, **subtitle text**, **button text**, and **social icon** colours.
- **Per-icon colours** — give each social icon its own glyph and background colour, or reset it back to the global colours.

### Social links
- Fields for **TikTok, YouTube, Twitter/X, Instagram, Discord, GitHub, and Email**.
- Only the links you fill in appear — empty ones are hidden automatically.
- Email turns into a `mailto:` link; other handles auto-prepend `https://`.

### Saving & exporting
- **Save** — keeps your text, colours, links and animation choices in the browser (via `localStorage`).
- **Download My Site** — exports a single standalone `my-site.html` with **everything baked in**, including the imported background and startup video (embedded directly in the file).
- **Reset Everything** — clears saved settings (with a confirmation prompt).

---

## How to customise the code

Everything you'd commonly tweak lives in **one place**: the `:root` block at the top of `index.html`.

```css
:root {
  --title-color:     #ffffff;   /* title text colour      */
  --subtitle-color:  #e9e9e9;   /* subtitle text colour   */
  --accent:          #6c5ce7;   /* button / accent colour */
  --overlay-opacity: 0.45;      /* 0 = none, 1 = black     */
  --default-bg:      linear-gradient(135deg, #1e1e2f, #2d2d44);
  --anim-speed:      0.8s;      /* startup animation speed */
}
```

- **Default text** lives in the `#hero` section of the HTML — edit the `<h1>` and `<p>` directly, or just type in the panel.
- **Add another social platform** — add one entry to the `SOCIALS` array in the `<script>` (key, label, placeholder, and an SVG icon). The panel field and on-page icon are generated automatically.

---

## Important notes

- **Downloaded file size:** embedding a video as a background or intro makes the exported HTML large (a ~30 MB video → a ~40 MB file). Images and GIFs stay small.
- **Saved settings don't include media:** browser storage is too small for video, so the **Save** button keeps text/colours/links only. Use **Download** for a portable copy that includes the media — or just keep `index.html` as your editor and re-import media when you reopen it.
- **Autoplay:** background and intro videos start **muted** because browsers block autoplay with sound.

---

## Browser support

Works in any up-to-date browser (Chrome, Edge, Firefox, Safari). No server needed — it runs straight from the file.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The whole site **and** its editor. |
| `my-site.html` | What gets created when you click **Download My Site** (your finished site). |
| `README.md` | This file. |
