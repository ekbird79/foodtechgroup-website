# Food Tech Group website

Static site, no build step required. `index.html` + `images/` folder.

All images (logo, Ellen's headshot, hero photo grid) are now local files in
`images/` — nothing on this site depends on Squarespace anymore, so it's
safe to cancel that subscription once you're ready.

## Deploying with GitHub + Vercel

1. **Create a GitHub repo**
   - github.com → New repository → name it (e.g. `foodtechgroup-website`) → Create
2. **Push this folder to it**
   ```
   cd site
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/foodtechgroup-website.git
   git push -u origin main
   ```
   (Or use GitHub Desktop / GitHub's web "upload files" if you'd rather avoid the command line.)
3. **Connect Vercel**
   - vercel.com → Add New → Project → Import the GitHub repo
   - Framework preset: **Other** (it's a static site, no build command needed)
   - Click Deploy
4. **Add your domain**
   - In the Vercel project → Settings → Domains → add `foodtechgroup.co.nz`
   - Vercel will show you DNS records to add at your domain registrar (wherever
     the domain itself is registered — this is separate from Squarespace hosting,
     so check where you actually bought the domain name)
   - Once DNS propagates (can take a few hours), the domain points at Vercel instead

From then on, any time you push a change to the `main` branch on GitHub,
Vercel automatically redeploys the live site — no manual re-upload needed.

## Contact form

The form on the site posts to Formspree (`https://formspree.io/f/xppazooe`).
This works identically regardless of where the site is hosted — no changes
needed for the move to Vercel.
