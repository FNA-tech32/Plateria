# Plateria

Plateria is a Next.js website for a private chef and charcuterie business. It presents services, a photo gallery, a tasting board, and event offerings, and it gives guests a way to request a booking.

## Contact

These details are placeholders. Change them in the site before you publish.

- Email: hello@plateria.com
- Handle: @plateria
- Location: Private chef · your city

Where they live:

- Chef card, handle, and about copy: `pages/components/About.js`
- Footer contact line, brand, and copyright: `pages/components/Footer.js`

## Run the site

You need Node.js and npm installed.

```bash
npm install
npm run dev
```

Open http://localhost:3000. The first screen is the landing page. It moves to the home page after 60 seconds, or click **Taste** to go there right away.

Production:

```bash
npm run build
npm start
```

`npm start` serves the built site. Run `npm run build` first.

Scripts in `package.json`:

- `dev` — `next dev`
- `build` — `next build`
- `start` — `next start`

## Folder layout

```
pages/
├── index.js              # Landing route (/)
├── landing.js            # Intro screen
├── home.js               # Main page (/home)
├── 404.js
├── _app.js
├── _document.js
├── api/hello.js
└── components/
    ├── Navbar.js
    ├── Splash.js
    ├── About.js
    ├── Services.js
    ├── Gallery.js
    ├── Board.js
    ├── Event.js
    └── Footer.js
styles/
├── globals.css
├── style.css
└── Home.module.css
package.json
```

## Manage the content

- Brand name and page titles: `pages/components/Navbar.js`, `pages/components/Footer.js`, `pages/landing.js`, and the `<title>` tags in `pages/index.js` and `pages/home.js`
- Chef story and contact: `pages/components/About.js`
- Home slider copy: `pages/components/Splash.js`
- Services: `pages/components/Services.js`
- Events: `pages/components/Event.js`
- Gallery: `pages/components/Gallery.js`
- Tasting board: `pages/components/Board.js`
- Look and layout: `styles/style.css` and `styles/globals.css`

The **Book Your Event** button in the navbar opens a form on the page. That form does not send email or save a request yet. Wiring it to a mail service or API is a later step.

Privacy, terms, and site policy text open from the footer in `pages/components/Footer.js`.
