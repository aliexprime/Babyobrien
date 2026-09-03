# Samuel's Spot

One page, one sentence: *hey Samuel, saved you a spot.*

Built to be kept. `index.html` is the entire site. The typeface (Libre Caslon Text) is embedded inside the file, there is no JavaScript, no build step, and nothing is loaded from anyone else's server. It should render the same in twenty years as it does today, and it prints in its own colour for framing.

## The design

- One deep green, the colour of a painted Dublin door. Warm-white words.
- Samuel's name and the full stop are the boy's blue. The spot is him.
- On a phone the sentence breaks as *hey Samuel, / saved you / a spot.* On a wider screen it sits on two lines.
- The only movement is the spot landing when the page opens. It stays still for anyone with reduced motion turned on.

## Change the words

Edit the one paragraph in `index.html`:

```html
<p class="line"><em>hey <span class="name">Samuel</span>,</em><br>saved you <span class="nb">a spot<span class="spot" aria-hidden="true"></span><span class="sr">.</span></span></p>
```

The blue dot after "spot" is the full stop, and the name shares its colour. Leave the trailing spans in place if you change the sentence.

## Link previews

`og.png` is the card WhatsApp and iMessage show when the link is shared. The `og:image` tag in `<head>` already points at `https://samuelrobertobrien.com/og.png`, so it works as soon as the site is live at that address. If the words change, take a new 1200×630 screenshot of the page and save it over `og.png`.

## Deploy on GitHub Pages

The repo already holds the two files Pages needs: `CNAME` (the custom domain) and `.nojekyll` (serve the files exactly as they are).

1. On GitHub, open **Settings → Pages**.
2. Under **Build and deployment**, set Source to **Deploy from a branch**, pick the branch that holds `index.html`, folder `/ (root)`, and save.
3. The **Custom domain** box should already show `samuelrobertobrien.com` from the `CNAME` file. If not, type it in and save.
4. At the domain registrar, add these DNS records for the bare domain (check them against GitHub's current Pages documentation before entering):

   | Type | Host | Value |
   | --- | --- | --- |
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | aliexprime.github.io |

5. Once DNS has propagated (minutes to a day), tick **Enforce HTTPS** on the Pages settings page.

The repository must be public for Pages on a free GitHub plan.
