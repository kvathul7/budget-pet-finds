# 🐾 Budget Pet Finds

A tiny product link page for an Instagram bio.

One website address → a list of products → tap a product → that product's
Meesho link opens in a new tab.

Plain HTML, CSS and JavaScript. No backend, no database, no accounts, no
paid services. It runs free on GitHub Pages forever.

---

## Project structure

```
budget-pet-finds/
├── index.html      the page itself
├── style.css       all the styling (colours, layout)
├── products.js     YOUR PRODUCT LIST - this is the file you edit
├── README.md       this guide
└── images/
    ├── dog-leash.jpg
    └── (add your other product photos here)
```

To preview it right now, just **double-click `index.html`**. It opens in your
browser and works straight away — no installing anything.

---

## ⚠️ Read this first

Every product currently has `PASTE_MEESHO_COMMISSION_LINK_HERE` instead of a
real link. Those buttons show **🔗 LINK COMING SOON** and do nothing, on
purpose, so visitors never land on a dead page.

As soon as you paste a real Meesho link, that button turns into
**🛒 SHOP NOW** automatically. You don't change anything else.

---

## HOW TO ADD A NEW PRODUCT

1. Open **`products.js`** in any text editor (Notepad works).
2. Copy an existing product — everything from `{` to `}`, including both braces.
3. Change the product **name**.
4. Change the **price**.
5. Change the **description**.
6. Change the **image** filename.
7. Paste your **Meesho commission link** in place of
   `PASTE_MEESHO_COMMISSION_LINK_HERE`.
8. **Save** the file.
9. Upload / push the change to GitHub (see "Updating your site" below).

A product block looks exactly like this:

```js
{
  name: "New Product",
  price: "₹299",
  description: "Product description",
  image: "images/new-product.jpg",
  link: "PASTE_MEESHO_COMMISSION_LINK_HERE"
}
```

**The one rule:** every product block needs a comma `,` after its closing `}`
— except the very last one in the list. If the page ever goes blank, a missing
or extra comma is almost always why.

You can add as many products as you like. The page lays them out by itself.

---

## Where to paste Meesho commission links

Inside `products.js`, on the `link:` line of each product.

```js
link: "PASTE_MEESHO_COMMISSION_LINK_HERE"
```

becomes

```js
link: "https://www.meesho.com/your-real-affiliate-link"
```

Keep the quotation marks `"` around the link. That's the whole change.

---

## How to add product images

1. Save your photo into the **`images/`** folder.
2. Name it in lowercase with dashes, no spaces — e.g. `pet-bowl.jpg`.
3. Write that exact filename on the `image:` line in `products.js`:

```js
image: "images/pet-bowl.jpg"
```

Tips:

- **Square photos look best** (e.g. 800×800). The page crops to a square.
- Keep each file under about 200 KB so the page loads fast on mobile data.
- `.jpg`, `.png` and `.webp` all work.
- **Filenames are case-sensitive on GitHub Pages.** `Pet-Bowl.JPG` and
  `pet-bowl.jpg` are different files there, even though Windows treats them as
  the same. Stick to lowercase everywhere and you'll never hit this.

If an image is missing, the card still looks fine — it shows a 🐾 instead of a
broken-image icon.

---

## Publish it free with GitHub Pages

### 1. Create a GitHub account
Go to <https://github.com> and sign up. It's free.

### 2. Create a new repository
Click the **+** in the top-right → **New repository**.

- **Repository name:** `budget-pet-finds`
- Set it to **Public** (GitHub Pages needs this on free accounts)
- Don't tick "Add a README" — you already have one
- Click **Create repository**

### 3. Upload these files
On the new empty repository page, click **uploading an existing file**.

Drag in `index.html`, `style.css`, `products.js`, `README.md` **and the
`images` folder**.

> Important: upload the **contents** of the `budget-pet-finds` folder, not the
> folder itself. `index.html` must sit at the top level of the repository, or
> the site won't load.

Then click **Commit changes**.

### 4. Go to Settings → Pages
In your repository, click **Settings** (top bar), then **Pages** in the left
sidebar.

### 5. Select the main branch
Under **Build and deployment**:

- **Source:** Deploy from a branch
- **Branch:** `main`, folder `/ (root)`
- Click **Save**

### 6. Publish the website
GitHub builds it automatically. Wait about 1–2 minutes, then refresh the
Settings → Pages screen.

### 7. Copy the GitHub Pages URL
A green box appears at the top with your live address:

```
https://YOUR-USERNAME.github.io/budget-pet-finds/
```

Open it on your phone to check it looks right.

### 8. Put that ONE URL into Instagram
Instagram app → **Profile** → **Edit Profile** → **Links** → **Add external
link** → paste the URL → **Done**.

That's it. That single link never changes again, no matter how many products
you add later.

---

## Updating your site

Whenever you edit `products.js` or add an image:

1. Go to your repository on GitHub.
2. To edit text: click the file → the ✏️ pencil icon → make the change →
   **Commit changes**.
3. To add an image: open the `images` folder → **Add file** → **Upload files**.

The live site updates by itself in about a minute. If you don't see the change,
refresh with `Ctrl+Shift+R` — your browser is showing a cached copy.

---

## Changing the look

Open `style.css`. The second line sets the accent colour used by the price and
the SHOP NOW buttons:

```css
--accent: #e64a19;
```

Change that one value to recolour the whole page. The heading and tagline text
live in `index.html`, near the top.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| Page is blank | A comma is missing or doubled in `products.js`. Check that every `}` has a `,` after it except the last. |
| Products don't appear | `products.js` must sit next to `index.html`, in the same folder. |
| Images don't show | Check spelling and lowercase; the filename in `products.js` must match the file in `images/` exactly. |
| Button says LINK COMING SOON | That product still has the placeholder link. Paste the real Meesho link in `products.js`. |
| 404 after publishing | `index.html` is probably inside a subfolder in the repository. It must be at the top level. |
| Changes not showing | Wait a minute, then hard-refresh with `Ctrl+Shift+R`. |
