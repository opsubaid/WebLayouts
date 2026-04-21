# 🎵 Spotify Web Player Clone

> A pixel-accurate, fully static clone of the Spotify Web Player - built with zero JavaScript.

---

## 📖 Overview

This is a front-end clone of the Spotify Web Player built entirely with HTML and CSS. No JavaScript framework, no JS runtime, no build tools. Every interactive toggle - play/pause, shuffle, repeat, like, mute, content filters, library selection - is driven purely by the CSS `:checked` pseudo-class on hidden `<input>` elements. Built as a personal project to push the boundaries of what CSS alone can do when modeling a real-world, state-driven UI.

---

## ✨ Features

- **CSS-only interactivity** - play/pause, shuffle, repeat, like, mute, and PiP toggles are all controlled via hidden `<input type="checkbox">` elements and CSS sibling selectors. No JavaScript.
- **Content filter pills** - radio-group inputs switch between All, Music, Podcasts & Shows, and Audiobooks views.
- **Library filter chips** - filter your library by Playlists, Albums, Artists, or Podcasts using radio state.
- **Sidebar navigation** - Home and Search tabs with active-state styling via radio inputs.
- **Animated equalizer bars** - the active library item shows a CSS keyframe equalizer animation.
- **7 curated content sections** - Trending Now, Deep Focus, Workout Mix, Jazz & Soul, Podcasts For You, New Releases, and Night Drive - each with 6–8 playlist cards.
- **Player bar** - includes now-playing info, progress track, volume slider, and all transport controls, all styled to match the real Spotify layout.
- **Mobile bottom navigation** - a fixed bottom nav bar with Home, Search, and Your Library tabs for narrow viewports.
- **Custom scrollbar** - styled `::-webkit-scrollbar` to match Spotify's dark UI.
- **Lightweight images** - all artwork is served directly from [Pexels.com](https://www.pexels.com) using their CDN with `?auto=compress&fit=crop` query parameters. No images are bundled in the repository.

---

## 🧠 Concepts Demonstrated

- CSS-only state management using `:checked` + general sibling combinator (`~`) and descendant selectors
- Complex Flexbox layouts (app shell, sidebar, player bar, card rows)
- CSS Grid for the shortcuts/greeting section
- `<input type="radio">` for mutually exclusive UI state (filters, nav tabs, library selection)
- `<input type="checkbox">` for toggle state (play, like, mute, shuffle, repeat)
- CSS `@keyframes` animations (equalizer bars)
- `aspect-ratio` and `object-fit: cover` for uniform image rendering
- Custom scrollbar styling with `::-webkit-scrollbar`
- Google Fonts integration (Montserrat)
- Font Awesome 6 icon library via CDN
- Responsive layout considerations with a mobile bottom nav fallback

---

## 🗂 Project Structure

```
Spotify-Clone/
├── index.html        # Full application markup - layout, all state inputs, and content
├── style.css         # All styles - reset, layout, components, animations, responsive rules
└── assets/
    └── favicon.png   # Browser tab icon
```

> All playlist and track artwork is fetched at runtime from [Pexels.com](https://www.pexels.com) - no image assets are stored locally. URLs use Pexels' CDN query parameters (`auto=compress`, `fit=crop`, `w=`, `h=`) to serve appropriately sized thumbnails, keeping the project footprint minimal.

---

## 🚀 Getting Started

### Prerequisites

- Any modern web browser (Chrome, Firefox, Edge, Safari)
- No package manager, build tool, or server required

### How to Run

1. Download or clone the repository.
2. Open `index.html` directly in your browser:

```bash
# Option A - just double-click index.html in your file manager

# Option B - serve locally with Python (avoids any file:// quirks)
python -m http.server 8080
# then open http://localhost:8080
```

That's it. No `npm install`. No compilation step.

---

## 📝 Notes

- **No audio playback** - this is a UI clone only. The player bar, progress bar, and volume slider are visual and CSS-state-driven; they do not control or play any audio.
- **Progress and volume bars are static** - they are styled div elements and do not respond to drag/click input. Adding real interactivity would require JavaScript.
- **Pexels dependency** - the project requires an internet connection to load artwork images. If Pexels CDN is unavailable, cards will render without thumbnails.
- **Webkit scrollbar styling** - custom scrollbars are visible in Chromium-based browsers. Firefox will use its default scrollbar style.
- **Future improvements** - audio integration via the Web Audio API, drag-to-scrub on the progress bar, and localStorage persistence for toggle states (liked, shuffle mode, etc.) are natural next steps.

---

## 📄 License

This project is for educational and portfolio purposes only. Spotify's name, logo, and brand identity are trademarks of Spotify AB. All images are sourced from [Pexels.com](https://www.pexels.com) and used under the [Pexels License](https://www.pexels.com/license/).
