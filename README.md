# Rich Think Technologies – One Page Website

A modern, responsive one-page homepage. Pure HTML + CSS + JavaScript, so there is no build step and no npm.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The full website (styles and script included) |
| `favicon.svg` | Browser tab icon |
| `README.md` | This guide |

## 1. Edit contact details

Open `index.html` and scroll to the bottom. Find the `CONFIG` block:

```js
const CONFIG = {
  phone:    "+92 300 0000000",
  whatsapp: "923000000000",   // country code + number, no + or spaces
  email:    "info@richthinktech.com",
  address:  "Your Office Address, City, Pakistan",
  facebook: "https://www.facebook.com/RichThinkTechnology"
};
```

Change these values and every phone, email, WhatsApp and Facebook link on the page updates.

The stats numbers (Projects, Clients, Years) are in the `stats` section. Search for `data-count` and change the numbers.

## 2. Upload to GitHub

1. Go to https://github.com/new
2. Repository name: `richthink-website` (Public or Private, both work)
3. Click **Create repository**
4. Click **uploading an existing file**, drag `index.html`, `favicon.svg` and `README.md`, then **Commit changes**

Or with Git:

```bash
git init
git add .
git commit -m "Rich Think Technologies homepage"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/richthink-website.git
git push -u origin main
```

## 3. Deploy on Cloudflare Pages (free)

1. Log in at https://dash.cloudflare.com
2. Go to **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
3. Connect your GitHub account and select `richthink-website`
4. Build settings:
   - Framework preset: **None**
   - Build command: *(leave empty)*
   - Build output directory: `/`
5. Click **Save and Deploy**

In about a minute your site will be live at:
`https://richthink-website.pages.dev`

Every time you push a change to GitHub, Cloudflare updates the site automatically.

## 4. (Optional) Connect a custom domain

In your Cloudflare Pages project → **Custom domains** → **Set up a domain** → enter e.g. `richthinktech.com` and follow the DNS steps.

## 5. (Optional) Show on Google search

1. Go to https://search.google.com/search-console
2. Add your site URL and verify it
3. Use **URL Inspection** → **Request Indexing**

Google usually lists a new site within a few days to a couple of weeks.

> If this is only a demo for a client and you **don't** want it on Google yet, add this line inside `<head>` in `index.html`:
> `<meta name="robots" content="noindex" />`
