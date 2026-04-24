# Laurent — Restaurant Landing Page

A responsive landing page I built for a fine‑dining restaurant concept called **Laurent**. It's a static site — no backend, no build step — put together with plain HTML, CSS and a bit of JavaScript. The goal was to practice layout, motion and all the small UI details that make a food site feel appetising rather than generic.

Live demo: open `index.html` in a browser, or host the folder on any static server.

## What's on the page

- Full‑width rotating hero slideshow (custom circular navigation built on GSAP / TweenMax)
- Sticky header with a responsive menu and a custom hamburger animation for mobile
- Intro / about section with scroll‑reveal animations
- "Featured items" drinks carousel powered by Swiper
- Menu sections for food and drinks with pricing cards
- Footer with contact details and social links

## Tech

| Area | Tools |
| --- | --- |
| Markup | HTML5 |
| Styling | CSS3 (Flexbox, Grid, custom properties, media queries) |
| Interactions | Vanilla JavaScript, jQuery |
| Animations | GSAP / TweenMax, ScrollReveal |
| Carousel | Swiper.js |
| Icons / fonts | Font Awesome, Google Fonts (Miniver, Montserrat, Josefin Sans, Fredoka One) |

No framework, no bundler. Everything runs straight from the files in this repo.

## Project structure

```
.
├── index.html              # Main page
├── cicle.html              # Small circular-hover experiment
├── index.css               # Base styles + layout
├── slider.css              # Hero slideshow styles
├── cardSlider.css          # Swiper card styles
├── lastflex.css            # Menu / flex section styles
├── footer.css              # Footer styles
├── script.js               # Swiper init
├── javascript/
│   ├── allLogicsjavascript.js   # Mobile menu toggle
│   ├── slider.js                # Hero slideshow logic (GSAP)
│   └── scrollRevael.js          # ScrollReveal setup
├── swiper-bundle.min.css
├── swiper-bundle.min.js
└── assets (logo.ico, food.png, drink.png, screenshots, …)
```

## Running it locally

Clone the repo and open `index.html` directly:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
# either open index.html in your browser, or run a tiny static server:
python3 -m http.server 8000
# then visit http://localhost:8000
```

A static server is recommended so relative asset paths and Google Fonts preconnects behave the same way they would in production.

## Browser support

Tested on the latest Chrome, Edge, Firefox and Safari. The layout is responsive down to ~360px wide; below that things will still work but were not a design target.

## Known rough edges

Being transparent — this was a practice project, so a few things are not production‑ready:

- The navigation links are placeholders (`href` with no target).
- Some layout values are pixel‑based rather than fluid.
- There's a small hard resize‑reload in `javascript/slider.js` that exists purely because the slideshow maths were written for a fixed viewport during the demo phase.

I've left them in on purpose so the code stays honest about what it is.

## Credits

- Hero slideshow technique adapted from the original "circular navigation" demo by COIDEA (MIT licensed) — see the header comment in `javascript/slider.js`.
- Food and drink photography used in the mock is from Pexels, Unsplash and Freepik stock — swap in your own before using this anywhere real.

## License

Released under the MIT License. Do whatever you like with it — attribution is appreciated but not required.
