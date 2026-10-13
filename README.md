# Kiwi brand guidelines

A brand guidelines site in `index.html`. It opens on a cover page (`#home`) that links into two views:

- **Brand** (`#brand`): strategy (values, audience, positioning), voice (tone, key messages, writing style, example headlines), logo, clear space and usage, colour, typography.
- **Templates** (`#templates`): email signature generator, Word letterhead, newsletter (Word file and PDF example).

Any section can be linked directly, for example `#signature` or `#letterhead`. The page switches to the right view. The Kiwi logo in the top band always goes back to the cover.

## Start here

1. Unzip this folder.
2. Upload everything inside it (not the zip itself) to the root of a new GitHub repository, keeping the folders as they are. GitHub's web uploader takes up to 100 files at a time; this folder has fewer than that.
3. Turn on GitHub Pages (steps below).
4. Once it's live, open the site and check the logo and template downloads work.
5. Set up email signatures from the live site, not from a local copy, so the logo images link to the hosted files.

## Files

```
index.html                    The whole site (HTML, CSS and JavaScript in one file)
assets/logo/                  Logo suite: primary, strap right, strap beneath (black and white,
                              with and without clear space), profile images and favicon,
                              as SVG, PNG and PDF
  kiwi-logo-suite.zip         Every logo file in one download
  sets/                       One zip per version and format, holding both colours
                              (used by the SVG/PNG/PDF buttons on each logo card)
assets/favicon/               The icon shown in the browser tab for this site
  favicon.svg                 Switches to white when the browser is in dark mode
  favicon-32.png              Fallback for browsers that don't use SVG icons
  apple-touch-icon.png        180 × 180 px, used when the page is saved to a phone home screen
assets/email/                 Images used inside the email signature
  kiwi-logo.png               400 × 113 px, shown at 200 px wide
  safecontractor.png          shown at 30 px tall
  ssip.png                    shown at 30 px tall
assets/templates/             Downloadable templates
  kiwi-letterhead.dotx        Word template (opens as a new letter)
  kiwi-letterhead.docx        Plain copy of the same letterhead
  letterhead-preview.png      Preview image shown on the page
  kiwi-newsletter.docx        Newsletter template (edit in Word, save as PDF)
  kiwi-newsletter.pdf         PDF example of the newsletter
  newsletter-p-1..2.png       Page previews shown on the page
assets/guidelines/            Downloads in the band at the bottom of every page
  kiwi-brand-guidelines.pdf   A4 PDF version of the brand guidelines
  how-to-use-the-kiwi-brand-guidelines.txt   Plain-text guide for the team
```

## Publish on GitHub Pages

1. Create a repository and upload everything in this folder.
2. In the repository, go to **Settings › Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
4. After a minute or two the site is live at `https://<account>.github.io/<repository>/`.
5. Share that link with the team. The Email signature section is at `#signature`.

GitHub Pages sites are public, including ones built from private repositories on paid plans. Everything on this site is already public information (address, company number, logo).

## How the signature images work

The signature points to the images in `assets/email/` on whatever site hosts this page. Once the page is on GitHub Pages, the images are hosted there too, so no other hosting is needed.

**Keep the images where they are.** Signatures people have already set up link to these files. If you move or rename them, the logo disappears from those signatures.

To move the images to wearekiwi.com later:

1. Upload the three files in `assets/email/` to the WordPress media library (or any public folder).
2. In `index.html`, find `SIGNATURE SETTINGS` and set `imageBase` to that folder's address, ending with a `/`. For example:
   `imageBase: 'https://wearekiwi.com/wp-content/uploads/email/',`
3. Publish, then ask everyone to copy and paste their signature again.

## Changing company-wide details

The website, address and T&Cs are in the `SIGNATURE SETTINGS` block near the bottom of `index.html`. Edit the text between the quotes, publish, and ask the team to set up their signature again.

Personal details (name, job title, email, phones) are typed in on the page by each person. Nothing is saved.

## Updating the letterhead

Open `kiwi-letterhead.dotx` in Word (right-click › Open, so you edit the template itself rather than a new letter). Edit the header, then save. The body is left blank on purpose. Save a copy as `.docx` too, and replace both files in `assets/templates/`. If the layout changes, update `letterhead-preview.png` with a fresh screenshot.

Familjen Grotesk (header) and Inter Light (body text) are embedded in the letterhead, so it shows correctly on computers without the fonts. Keep **File › Options › Save › Embed fonts in the file** ticked when saving.

## Updating the newsletter

Edit `kiwi-newsletter.docx` in Word, then save it again as `.docx` and as `.pdf` (File › Save As › PDF) and replace both files in `assets/templates/`. Update the two `newsletter-p-*.png` previews if the layout changes. Keep **Embed fonts in the file** ticked when saving.

## Updating the logo files

Replace the files in `assets/logo/` keeping the same names, then rebuild `kiwi-logo-suite.zip` and the zips in `assets/logo/sets/` so the download buttons match.

The site's own tab icon is in `assets/favicon/`. If the favicon changes, replace those three files too, keeping the same names.

## After it goes live

Open `assets/guidelines/how-to-use-the-kiwi-brand-guidelines.txt` and replace `[guidelines web address]`, `[name]` and `[email address]` with the live link and a contact, then upload it again.

## Technical notes

- The signature is built with tables and inline styles so it renders consistently in Outlook.
- The signature HTML is about 5,000 characters. Gmail allows up to 10,000.
- Familjen Grotesk is used where the reader has it installed. Everyone else sees Arial.
- Classic Outlook for Windows can send signature images as attachments. IT can stop this with the registry value `Send Pictures With Document` set to `0` under `HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Outlook\Options\Mail`.
