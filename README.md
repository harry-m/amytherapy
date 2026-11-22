# Amy Metcalfe: practice website

A small static website for a psychotherapy practice. Plain HTML and CSS: no build step, no JavaScript, no cookies, no external fonts or services.

## Pages

- `index.html`: Therapy (home page)
- `about.html`: About me
- `faq.html`: FAQs (fees, location, consultations, frequency, length of therapy)
- `contact.html`: Contact details and a button that opens the enquiry form
- `privacy.html`: Privacy notice (linked from the footer and the contact page)
- `styles.css`: all the styling, shared by every page
- `images/`: photos and the BACP logo

## Preview it locally

From this folder:

```
python3 -m http.server 8000
```

Then open http://localhost:8000, or just open `index.html` in a browser.

## Still to finish

Anything unfinished is highlighted in yellow. To list every one:

```
grep -n 'class="ph' *.html
```

At the time of writing these remain:

- `contact.html`: the Google Form link (see below)
- `privacy.html`: ICO registration number, anything else recorded at first contact, the list of services you use, web host and what it stores, and how you keep information secure

When a placeholder is filled in, delete the `<mark class="ph">` tags around it (or `class="ph-block"` on a paragraph). Once none are left, the `.ph` and `.ph-block` rules in `styles.css` can go too.

## Contact form

The Contact page has a button that opens a Google Form, so the site needs no server code and sets no cookies itself. To set it up:

1. In Google Forms (signed in to your Workspace account), create a form with name, email, phone (optional) and message.
2. Check it is accepting responses, then use Send, then the link tab, to copy the form's link.
3. In `contact.html`, replace `href="#"` on the "Open the contact form" button with that link, and delete the yellow note under it.
4. In the form's Responses tab, turn on email notifications so you hear about new enquiries.

## Photos

- `images/therapy-hero.jpg`: wide photo at the top of the Therapy page (stock photo: keep the licence, and check it covers website use)
- `images/room.jpg`: your room, on the Therapy page (check you have permission to use it)
- `images/portrait.jpg`: About page
- `images/bacp-logo.png`: BACP registered member logo, About page (follow BACP's rules for using it)

Resize photos before adding them (around 1800px wide is plenty) and remove location data (EXIF) from any photo you take yourself. Give every image a short `alt` description.

## Before publishing

- Fill in or remove every yellow placeholder.
- Check `privacy.html` matches how you actually work, and update it if you add analytics, cookies or new suppliers. Consider having BACP or your insurer look it over.
- Check the confidentiality wording against BACP and UKCP codes of ethics.
- Replace `href="#"` on the contact button with your Google Form link.

## Hosting

Any host that serves static files works: GitHub Pages, Netlify, Cloudflare Pages, or any web server. Upload the files in this folder as they are.
