# Samuel's landing page

A single static page announcing Samuel O'Brien's arrival. No build step, no dependencies: `index.html` is the whole site.

## Fill in the real details

Everything below is an **example value** and needs replacing. Each spot is marked with an `<!-- EDIT -->` comment in `index.html`.

| What | Where in `index.html` | Currently |
| --- | --- | --- |
| Arrival sentence and `datetime` (drives the "days old" line) | `.lede` | Friday 28 August 2026, 03:42 |
| Wristband strip | `.band` | O'Brien, Samuel · DOB 28/08/2026 · 03:42 · 3.41 kg · 51 cm · M |
| Details card (born, time, weight, length) | `.card` | as above |
| Note from the parents | `.note` | placeholder text |
| Sign-off | `.sign` | Mum & Dad |
| Message button email | `.btn-primary` `href` | hello@example.com |
| Gift registry link | second `.btn` `href` | `#` |
| Footer date | `footer` | Est. 28 Aug 2026 |
| Share preview text (WhatsApp, iMessage) | `<meta property="og:...">` in `<head>` | mirrors the details above |

## Add the photo

Save a portrait photo as `samuel.jpg` in this folder (4:5 crops best). Until the file exists the page shows a soft placeholder frame instead of a broken image. The same file is used as the share preview image.

## Preview locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```

then visit http://localhost:8000.

## Deploy

- **Vercel:** import the repository, framework preset "Other", no build command, output directory `.`.
- **GitHub Pages:** Settings → Pages → deploy from branch, folder `/ (root)`.
