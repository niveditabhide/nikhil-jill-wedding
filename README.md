# Nikhil & Jill — Wedding Reception website

A self-contained static website. It needs no server code, database or build step.

## 1. Set the RSVP email (one-time)
Open `index.html` in any text editor and find this block near the top of `<body>`:

```js
window.RSVP_CONFIG = {
  email: "YOUR-EMAIL@example.com",
  ccEmail: ""
};
```
Replace `YOUR-EMAIL@example.com` with the address that should receive RSVPs.
`ccEmail` is optional (a second person to copy).

Emails are sent through **FormSubmit.co** (free, no account needed).
**The first time a guest submits, FormSubmit emails that address an "Activate form" link.
Click it once.** Every RSVP after that arrives as a neat table:
name, phone, guests, arrival date and time, travel mode, meal choice, help needed and note.
Tip: submit one test RSVP yourself right after going live, and activate it from that email.

## 2. What happens when a guest taps "Confirm my RSVP"
1. The RSVP is emailed to the address above (in the background).
2. WhatsApp opens with the RSVP pre-filled to Nivedita or Tarun (the guest's choice). The guest presses send.
3. A thank-you card shows the summary, with a backup "Send on WhatsApp" button.

## 3. Hosting (pick one; all free)
- **Netlify Drop (easiest):** go to app.netlify.com/drop and drag the whole unzipped folder in. You get a live link instantly, and can rename it (e.g. nikhil-jill.netlify.app).
- **GitHub Pages:** create a repo, upload all files, then Settings → Pages → deploy from the main branch.
- **Your own domain / cPanel hosting:** upload the folder contents into `public_html` (or a subfolder).
- **Vercel / Cloudflare Pages:** create a new project and upload the folder.

Keep the folder structure as is: `index.html`, `img/`, `fonts/`.

## 4. Link previews on WhatsApp
`img/share.jpg` is the preview image. For the best previews, edit the `og:image` line in `index.html`
to the full URL once hosted, e.g. `https://nikhil-jill.netlify.app/img/share.jpg`.

## 5. Editing content
- Photos are in `img/`. To swap one, replace the file and keep the same name.
- Carousel captions: search `index.html` for `const adv = [`.
- Phone numbers for WhatsApp: search for `918794884304` / `917738341171`.
