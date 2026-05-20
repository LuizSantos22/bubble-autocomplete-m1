## Very fast autocomplete feature for Magento
![Magento Autocomplete](http://i.imgur.com/pc1KD3A.gif)

## Overview
Bubble Autocomplete is an implementation of the [Twitter Typeahead](https://twitter.github.io/typeahead.js/) plugin for Magento, extended with a custom full-width dropdown, fuzzy search, and voice search support.

## Features
- **Full-width dropdown (desktop)** — two-column layout with text suggestions, category links, and a product grid with images and prices
- **Mobile dropdown** — simplified vertical list with product image, name, price, and a "see all results" link
- **Fuzzy search** — Levenshtein-based typo tolerance with accent normalization and hyphen handling (e.g. "audio tecnica" matches "Audio-Technica")
- **Voice search (desktop)** — microphone button in the search bar using the Web Speech API (Chrome/Edge, requires HTTPS)
- **Voice search (mobile)** — same implementation with `continuous: true` and `interimResults: true` for reliable capture on Android browsers; requires microphone permission granted explicitly in browser settings

## Installation on Magento 1 / OpenMage

## Configuration
Go to System > Configuration > Bubble Autocomplete
![Magento Autocomplete Configuration](http://i.imgur.com/jdOztwo.png)

## Voice Search — Mobile Notes
On Chrome Android, microphone permission must be explicitly granted at least once:
1. Tap the lock icon in the address bar (or go to Settings → Site Settings → Microphone)
2. Find your domain and set it to **Allow**
3. After the first grant, "Ask" mode works normally on subsequent visits

Voice search is hidden on mobile via CSS (`display: none`) if you prefer to disable it and keep only the desktop version.
