# Samuel's Spot

A single page that says one thing: *hey Samuel, I saved you a spot.*

`index.html` is the whole site. No build step, no dependencies. It loads one typeface (Fraunces) from Google Fonts and falls back to Georgia if that's unavailable.

## Change the words

Edit the one paragraph in `index.html`:

```html
<p class="line"><em>hey Samuel,</em><br>I saved you <span class="nb">a spot<span class="spot" aria-hidden="true"></span><span class="sr">.</span></span></p>
```

The green dot after "spot" is the full stop. Leave the trailing spans in place if you change the sentence.

## Deploy

- **Vercel:** import the repository, framework preset "Other", no build command, output directory `.`.
- **GitHub Pages:** Settings → Pages → deploy from branch, folder `/ (root)`.
