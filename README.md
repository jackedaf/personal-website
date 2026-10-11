# Personal website

A two-page static site: **about** (`index.html`) and **love** (`love.html`).
No build step, no frameworks, no CSS. Edit the HTML, push, done.

## Editing your copy

Open `index.html` and `love.html`.
Each paragraph is a `<p> ... </p>`.


## Preview locally

Just open `index.html` in a browser. That's it.

## Putting it online (GitHub Pages, free)

1. On GitHub, open this repo → **Settings** → **Pages**.
2. Under **Build and deployment**, set Source to **Deploy from a branch**,
   pick branch `main`, folder `/ (root)`. Save.
3. After a minute, the site is live at `https://jackedaf.github.io/personal-website/`.

## Pointing your Namecheap domain at it

### On GitHub
1. Still in **Settings → Pages**, under **Custom domain**, enter your domain
   (`aashganda.com`) and save. The `CNAME` file in this repo already holds it.
2. Tick **Enforce HTTPS** once it becomes available (can take up to an hour after DNS is set).

### On Namecheap
1. Log in → **Domain List** → **Manage** next to your domain.
2. Go to the **Advanced DNS** tab.
3. Delete any existing `A`, `CNAME`, or `URL Redirect` records for `@` and `www`
   (the parking page records).
4. Add these records:

   | Type  | Host | Value                                   | TTL       |
   |-------|------|-----------------------------------------|-----------|
   | A     | @    | 185.199.108.153                         | Automatic |
   | A     | @    | 185.199.109.153                         | Automatic |
   | A     | @    | 185.199.110.153                         | Automatic |
   | A     | @    | 185.199.111.153                         | Automatic |
   | CNAME | www  | `jackedaf.github.io.`     | Automatic |

5. Wait. DNS changes usually take a few minutes but can take up to a day.
   Check progress at https://dnschecker.org by entering your domain.

Once it resolves, both `aashganda.com` and `www.aashganda.com` will show the site.
