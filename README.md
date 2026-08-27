# Acreedo — GitHub Pages demo

This folder is a static, public-demo version of the Acreedo website. It keeps the real photography, responsive layouts, custom font, scroll reveals, mobile navigation, tattoo gallery, artist Facebook portfolio links, piercing prices, FAQ, newsletter demo and contact demo.

It works on GitHub Pages without Node.js, a database or a server.

## Edit the wording and links

Open `assets/content.js` in GitHub or any text editor. That one file contains:

- business details and opening hours;
- the email, phone number, Facebook page, Google reviews and map links;
- homepage text;
- artist names, biographies, availability and Facebook album links;
- tattoo portfolio entries;
- piercing prices;
- FAQ answers.

Search for `EDIT-ME` and replace every result before sharing the demo.

To replace a photo, put the new JPG in `assets/photos/` and change its filename in `assets/content.js`. Use lowercase filenames without spaces for the least trouble.

## Put it on GitHub Pages

1. Create a new GitHub repository.
2. Upload the *contents* of this folder to the repository root. `index.html` must be at the top level.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. GitHub will show the public demo URL after the first deployment finishes.

All navigation uses hash routes such as `#/tattoos`, so the pages work even when the demo is hosted below a repository name.

## Add your own domain

GitHub recommends using `www.yourdomain.co.uk` and also configuring the root domain.

1. In your GitHub profile, open **Settings → Pages → Add a domain** and follow GitHub's TXT-record instructions to verify ownership.
2. In the website repository, open **Settings → Pages**. Enter `www.yourdomain.co.uk` under **Custom domain** and save.
3. At the company where you bought the domain, add a `CNAME` record:
   - Name/host: `www`
   - Value/target: `YOUR-GITHUB-USERNAME.github.io`
4. To make the root `yourdomain.co.uk` work too, add four `A` records with the name/host `@`:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
5. Wait for DNS to update, then return to **Settings → Pages** and enable **Enforce HTTPS** when the option becomes available.

Do not add wildcard DNS records such as `*.yourdomain.co.uk`. Keep GitHub's verification TXT record in place.

## Forms

The contact and newsletter forms deliberately show demo confirmations and do not send personal data anywhere. Before a real launch, connect them to a service such as Formspree/Basin and Mailchimp/Buttondown, or use the production Acreedo website instead.

## Why the manager is not included

GitHub Pages only serves public static files. It cannot securely keep a manager password, process private logins or accept permanent image uploads. Putting the production manager password into this repository would expose it to everyone.

Edit `assets/content.js` for the GitHub demo. Keep the real manager portal on the hosted production version.

## Local preview

You can double-click `index.html` to preview it. For the closest match to GitHub Pages, serve the folder with any small local web server.
