# Baby Reveal – Couples Study (scratch card pregnancy reveal)

Fake psychology survey -> register Mom & Dad -> 10 questions -> 3 scratch cards -> jackpot -> "We're Pregnant!" reveal, with reaction video recording, Google Drive upload and WhatsApp sharing.

## Host on GitHub Pages
1. Create a new repository on github.com (e.g. `baby-reveal`).
2. Upload everything in this folder (`index.html`, `.nojekyll`, `drive-upload.gs`, `README.md`) via **Add file > Upload files**.
3. Go to **Settings > Pages**, set Source to **Deploy from a branch**, Branch **main** and folder **/ (root)**, then Save.
4. After about a minute your site is live at `https://<your-username>.github.io/baby-reveal/`.
5. Open that link on a phone in Chrome or Safari. It is https, so camera and microphone work.

## Customize (top of the `<script>` in index.html)
- `DUE`: due date text
- `BABY_LINE`: line under "Surprise ...!"
- `HOST_NAME`, `HOST_WHATSAPP`: who receives messages (country code + number, digits only)
- `UPLOAD_URL`, `UPLOAD_KEY`: your Google Apps Script URL and secret (see below)
- `REVEAL_IMAGE`: add a photo named `reveal.jpg` to the repo (or use a full URL)

## Google Drive upload
Deploy `drive-upload.gs` as a web app (steps are in the file) and paste its URL into `UPLOAD_URL`. Keep `UPLOAD_KEY` identical to `SECRET` in the script. Files land in a Drive folder called "Baby Reveal Uploads".

## Notes
- Everything in a public repo is visible, including the WhatsApp number and the upload key. Use a private repo with GitHub Pages (needs a paid plan) or a throwaway key if that matters.
- Recording starts when the couple registers and stops 15 seconds after the reveal.
- Test once end to end on your own phone before sharing the link.
