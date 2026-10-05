# 🐾 Budget Pet Finds

A simple link list for an Instagram bio.

One website address → a list of product names → tap one → it opens that
product's Meesho link in a new tab. No images, no cart, no checkout.

Plain HTML, CSS and JavaScript. Free forever on GitHub Pages.

**Live site:** https://kvathul7.github.io/budget-pet-finds/

---

## Files

```
index.html     the page
style.css      colours and layout
products.js    YOUR LINKS - the only file you edit
README.md      this guide
```

To preview it, double-click `index.html`.

---

## HOW TO ADD A NEW PRODUCT

1. Open **`products.js`**.
2. Copy one whole line (the part starting with `{` and ending with `}`).
3. Paste it below the last one.
4. Change the **name**, the **price**, and the **link**.
5. Save.

One product is one line:

```js
{ name: "New Product", price: "₹299", link: "PASTE_MEESHO_COMMISSION_LINK_HERE" }
```

**The one rule:** every line needs a comma `,` after its `}` — except the last
one. If the page goes blank, a missing or extra comma is almost always why.

Don't want prices shown? Set `price: ""`.

---

## Where to paste Meesho links

In `products.js`, on the `link:` part of each line.

```js
link: "PASTE_MEESHO_COMMISSION_LINK_HERE"
```

becomes

```js
link: "https://www.meesho.com/your-real-link"
```

Keep the quotation marks `"` around it.

Until you paste a real link, that row shows a greyed-out **COMING SOON** and
cannot be tapped, so the page never sends anyone to a dead page. Paste a real
link and the row goes live by itself.

### Collection link vs product link

- A `/collection/` link opens a **group** of products.
- A normal product link opens **that one product**.

If you want a tap to land straight on a single product, copy that product's own
share link from Meesho rather than a collection link.

---

## Updating the live site

1. Go to <https://github.com/kvathul7/budget-pet-finds>
2. Click **`products.js`**
3. Click the **✏️ pencil**
4. Make your change
5. Scroll down → **Commit changes**

The live site updates in about a minute. If you don't see it, refresh with
`Ctrl+Shift+R`.

---

## Publishing from scratch (already done, kept for reference)

1. Create a GitHub account at <https://github.com>.
2. Click **+** → **New repository**, name it, set it **Public**, create it.
3. Click **uploading an existing file** and drag these files in.
   `index.html` must sit at the top level, not inside a folder.
4. Go to **Settings** → **Pages**.
5. Under **Source** pick **Deploy from a branch**.
6. Choose branch **main**, folder **/ (root)**, then **Save**.
7. Wait a minute, refresh, and copy the URL that appears.
8. Put that URL in Instagram:
   **Profile** → **Edit Profile** → **Links** → **Add external link**.

That one URL never changes, however many products you add later.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| Page is blank | A comma is missing or doubled in `products.js`. |
| Row says COMING SOON | That product still has the placeholder link. |
| Nothing shows at all | `products.js` must sit next to `index.html`. |
| 404 after publishing | `index.html` must be at the top level of the repository. |
| Change not showing | Wait a minute, then hard-refresh with `Ctrl+Shift+R`. |

---

## Changing the colour

In `style.css`, the first colour sets the accent used by prices and hover:

```css
--accent: #e64a19;
```
