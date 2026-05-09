Personal start page. This is a fork of [One Page](https://github.com/R-Jin/One-page) with zero dependencies.

## Features

- Live clock and date
- Weather via [Open-Meteo](https://open-meteo.com/) (no API key needed)
  - Browser geolocation as default
  - Manual coordinate input as fallback
  - One-click clear saved coordinates
- Static quotes, random on each load
- Quick-access links in 3 groups
- Custom artwork background
- Responsive layout

## Setup (Chrome/Edge)

1. Clone the repo or click "Code" on the top of this page and "Download ZIP"  
2. Install a new tab extension (e.g. [New Tab Redirect](https://chromewebstore.google.com/detail/new-tab-redirect/icpgjfneehieebagbmdbhnlpiopdcmna))
3. Go to chrome://extensions and enable "Allow access to file URLs"
3. Open New Tab Redirect settings and fill "Redirect URL" with `index.html` path (e.g. /home/betadyne/hytam-startpage/index.html)

## Customization

### Quick Links

Edit `links.js`:

```javascript
window.links = [
  {
    heading: "~/otaku",
    color: "blue",    // blue | purple | green
    links: [
      { name: "vndb", url: "https://..." },
      // ...
    ]
  }
];
```

### Quotes

Edit `quotes.js`:

```javascript
window.quotes = [
  { content: "Your quote", author: "Author Name" }
];
```

or just use ChatGPT or Gemini to edit `quotes.js`

### Artwork

Replace `image.jpg` with your own image.

### Weather Location

Click the weather widget, enter latitude and longitude in the prompt. Or allow browser location. Click the X button to clear saved coordinates.

[Check your latitude and longitude](https://www.latlong.net/)

### Colors

Edit CSS custom properties in `style.css`:

```css
:root {
  --bg-color: #282C34;
  --red: #E06C75;
  --green: #98C379;
  --blue: #61AFEF;
  --purple: #C678DD;
  /* ... */
}
```
