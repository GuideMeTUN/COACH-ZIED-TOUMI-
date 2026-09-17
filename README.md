# Zied Toumi — Chess Coach Portfolio

A trilingual (Arabic / French / English) portfolio site for chess coach Zied Toumi, with an
embedded interactive "Play & Learn" chess app.

## Files

```
CNAME                tells GitHub Pages to serve this site at coach-zied-toumi.tn
                     — keep this file in the repo root every time you upload
index.html          the portfolio page (the chess app and hero photo are both
                     embedded inside this one file, so it works on its own)
apps/                source copies of the three chess-app files, kept for reference
  check-up-en.html   only — index.html does not depend on this folder
  check-up-fr.html
  check-up-ar.html
images/
  hero.jpg           source copy of the hero photo, kept for reference
```

## Put this on GitHub Pages (free hosting, no server needed)

1. Create a new repository on GitHub (e.g. `zied-toumi-chess`).
2. Upload **both** `CNAME` and `index.html` to the repository root (the `apps/` and
   `images/` folders are optional — `index.html` has everything it needs built in).
   - Easiest way: on the repo page, click **Add file → Upload files**, drag in `CNAME`
     and `index.html` together, then **Commit changes**.
   - **Important:** every time you upload a new `index.html` later, make sure `CNAME`
     is still sitting in the repo root — GitHub Pages silently drops your custom domain
     if that file ever goes missing, even if your DNS records are still correct.
3. Go to the repo's **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Under **Branch**, choose `main` and `/ (root)`, then **Save**.
6. Wait about a minute, then refresh the Pages settings tab — GitHub will show your live
   link, in the form:

   ```
   https://<your-github-username>.github.io/<repo-name>/
   ```

That link is what you share with schools, clubs, and parents. Any time you edit a file and
push the change, the live page updates automatically within a minute or two.

## Editing later

- All the text is in the `I18N` object near the bottom of `index.html` — each language has
  its own block (`en`, `fr`, `ar`), so you can edit copy without touching the layout.
- To change the phone number or email, search for `95 503 414` and
  `toumizied553@gmail.com` in `index.html`.
- The hero photo is embedded directly inside `index.html` (as base64) so it always displays,
  even if the `images` folder gets dropped during upload. To swap the photo, replace the
  `data:image/jpeg;base64,...` string inside the `<img>` tag in the hero section with a new
  one — the `images/hero.jpg` file is kept in this folder as the source copy to re-encode.
