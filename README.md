# Samuel's Spot

One page, one sentence: *hey Samuel, I saved you a spot.*

Built to be kept. `index.html` is the entire site. The typeface (Libre Caslon Text) is embedded inside the file, there is no JavaScript, no build step, and nothing is loaded from anyone else's server. It should render the same in twenty years as it does today, and it prints in its own colour for framing.

## The design

- A painted green door, in the Dublin Georgian manner. One colour, warm-white words.
- Samuel's name and the full stop are the boy's blue. The spot is him.
- A small brass-plate line at the foot records the day the spot was saved.
- On a phone the sentence breaks as *hey Samuel, / I saved you / a spot.* On a wider screen it sits on two lines.
- The only movement is the spot landing when the page opens. It stays still for anyone with reduced motion turned on.

## Change the words

Edit the one paragraph in `index.html`:

```html
<p class="line"><em>hey <span class="name">Samuel</span>,</em><br>I saved you <span class="nb">a spot<span class="spot" aria-hidden="true"></span><span class="sr">.</span></span></p>
```

The blue dot after "spot" is the full stop, and the name shares its colour. Leave the trailing spans in place if you change the sentence. The date line is the paragraph just below it.

## Link previews

`og.png` is the card WhatsApp and iMessage show when the link is shared. Once the page has a permanent address, change the `og:image` meta tag in `<head>` from `og.png` to the full `https://` address of that file, because most messaging apps ignore relative paths. If the words change, take a new 1200×630 screenshot of the page and save it over `og.png`.

## Deploy

- **Vercel:** import the repository, framework preset "Other", no build command, output directory `.`.
- **GitHub Pages:** Settings → Pages → deploy from branch, folder `/ (root)`.
