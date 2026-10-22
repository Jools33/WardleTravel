# Wardle Travel demo site

A static, placeholder-content demo of the Wardle Travel website for stakeholder review. Styling (colours, Inter font, rounded cards) is borrowed from Wardle Compass; layout takes the best bits of jlmtravel.co.uk and wonderlingtravel.co.uk.

There's no build step: plain HTML, CSS and JavaScript, so it runs as-is on GitHub Pages.

## Pages

- `index.html` – home: hero with quick search, inclusions, why us, offers, reviews, welcome, destinations, branches
- `offers.html` – filterable offers
- `destinations.html` – filterable destinations
- `about.html` – story, stats, team, FAQs
- `contact.html` – branches and quote form
- `booking.html` – placeholder booking journey and Manage My Booking

All forms, booking, WhatsApp and newsletter are placeholders that show a "coming soon" message.

## Passcode

Every page is hidden behind a passcode screen (`assets/site.js`). This is only a basic hiding mechanism: GitHub Pages is public and anyone determined can read the page source. Don't put anything confidential on the site.

To change the passcode, hash the new one and replace `PASSCODE_SHA256` in `assets/site.js`:

```sh
echo -n "new-passcode" | sha256sum
```

## Business details

Branch names, addresses and phone numbers live in `BUSINESS` at the top of `assets/site.js`. They are placeholders for now (phone numbers use the Ofcom 01632 960xxx range reserved for fiction); swap in the real details once confirmed.

## Run locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy

Settings → Pages → Build and deployment → Deploy from a branch → pick the branch and `/ (root)`.
