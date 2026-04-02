# How to Add Links to Lydia's Recommendations

## Overview

Each page is a plain `.html` file in your GitHub repo. You edit the file, save it, and GitHub Pages updates your live site within a minute or two.

---

## Adding a Product Card (Shop / Visit / Listen)

Find the right file for the page you want to update:

| Page | File |
|------|------|
| Recipes | `recipes.html` |
| Bread & Kitchen | `bread.html` |
| Baby Favorites | `baby.html` |
| EC Resources | `ec.html` |

Copy and paste this block wherever you want the new card to appear, inside the `<div class="section">`:

```html
<a class="product-card" href="YOUR_LINK_HERE" target="_blank">
  <div class="product-emoji">🛍️</div>
  <div class="product-info">
    <div class="product-name">Product Name</div>
    <div class="product-note">Short description of why you love it.</div>
  </div>
  <div class="product-cta">Shop</div>
</a>
```

**To customize:**
- `href="YOUR_LINK_HERE"` → paste your Amazon affiliate link (or any URL)
- `🛍️` → swap for any emoji
- `Product Name` → the product name
- `Short description` → one line about why you recommend it
- `Shop` → change to `Visit` or `Listen` if it's a website or podcast

---

## Adding a Recipe

Open `recipes.html` and paste this block inside the `<div class="section">`, before or after any existing recipe:

```html
<div class="recipe-card">
  <div class="recipe-header" onclick="toggleRecipe(this)">
    <div class="recipe-emoji">🍽️</div>
    <div class="recipe-title-wrap">
      <div class="recipe-name">Recipe Name</div>
      <div class="recipe-meta">Serves X · Quick note about the recipe</div>
    </div>
    <div class="recipe-toggle">+</div>
  </div>
  <div class="recipe-body">
    <div class="recipe-section-label">Ingredients</div>
    <ul class="recipe-ingredients">
      <li>Ingredient 1</li>
      <li>Ingredient 2</li>
      <li>Ingredient 3</li>
    </ul>
    <div class="recipe-section-label">Instructions</div>
    <ol class="recipe-steps">
      <li>Step one.</li>
      <li>Step two.</li>
      <li>Step three.</li>
    </ol>
  </div>
</div>
```

**To add multiple ingredient sections** (e.g. "Sauce", "Coating"), repeat the label + list pattern:

```html
<div class="recipe-section-label">Sauce</div>
<ul class="recipe-ingredients">
  <li>...</li>
</ul>
<div class="recipe-section-label">Coating</div>
<ul class="recipe-ingredients">
  <li>...</li>
</ul>
```

---

## Adding a New Page

1. Copy any existing page file (e.g. `ec.html`) and rename it (e.g. `snacks.html`)
2. Update the title, hero heading, and content inside
3. Add a nav link to **every** page's nav bar so people can find it:

Find this block in each `.html` file:
```html
<nav class="nav">
  <a href=".../index.html">Home</a>
  ...
</nav>
```
And add:
```html
<a href="https://lydia-wu.github.io/recommendations/snacks.html">Snacks</a>
```

4. Upload the new file to GitHub — done!

---

## How to Upload Changes to GitHub

1. Go to [github.com/lydia-wu/recommendations](https://github.com/lydia-wu/recommendations)
2. Click the file you want to update
3. Click the **pencil icon** (Edit) in the top right
4. Make your changes
5. Scroll down and click **Commit changes**

Your site updates within ~1 minute.

> **Tip:** You can also edit files directly on GitHub without downloading anything — just click the file, hit the pencil, and edit right in the browser.
