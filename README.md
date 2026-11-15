# Kevin Tollison — Portfolio Site

A static portfolio (plain HTML and CSS, no build step, no JavaScript required) ready to host for free on GitHub Pages.

The site files are already in this folder. `index.html` should stay at the root of the repository.

## Add your resume

Drop your resume PDF into this same folder and name it `resume.pdf`. The Resume links on the site already point there (`href="resume.pdf"`). Until you add the file, those links will 404.

## Publish on GitHub Pages (free)

1. Create a free GitHub account if you don’t have one, at [github.com](https://github.com).
2. Create a new repository. A simple name like `kwtgames` or `portfolio` is fine. Leave it empty (no README, no .gitignore).
   - Public repos can use GitHub Pages on the free plan.
3. Upload the **contents of this folder** (not a parent folder) so that `index.html` is at the repo root.
   - In the browser: open the new repo, choose **Add file → Upload files**, select everything in this folder, and commit.
   - Or with git, from this folder:

     ```
     git init
     git add .
     git commit -m "Add portfolio site"
     git branch -M main
     git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
     git push -u origin main
     ```

4. In the repo, go to **Settings → Pages**.
5. Under **Build and deployment**, set **Source** to “Deploy from a branch”, branch `main`, folder `/ (root)`, and save.
6. After a minute or two, the site will be live at:

   `https://YOUR_USERNAME.github.io/YOUR_REPO/`

If the pages look unstyled, the files may have been uploaded inside an extra folder. `index.html`, `projects/`, and `assets/` need to sit at the repo root.

### Optional: use a user-site URL instead

If you name the repository `YOUR_USERNAME.github.io`, GitHub will serve it at `https://YOUR_USERNAME.github.io/` with no extra path. The relative links in this site work either way.

## Optional: point kwtgames.com at the site

If you still own kwtgames.com (or another domain):

1. In this folder, create a file named `CNAME` (no extension) with a single line:

   ```
   kwtgames.com
   ```

   Commit and push it.
2. In GitHub: **Settings → Pages → Custom domain**, enter `kwtgames.com`, and save. Enable “Enforce HTTPS” once the certificate is ready.
3. At your domain registrar, add the DNS records GitHub documents for Pages custom domains. Typically:

   - An `A` record (or `ALIAS`/`ANAME`) for the apex `kwtgames.com` pointing at GitHub’s Pages IP addresses, and/or
   - A `CNAME` record for `www` pointing at `YOUR_USERNAME.github.io`.

   Use the current IPs from [GitHub’s Pages custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site), since they can change.

DNS can take a little while to update. Keep the `CNAME` file in the repo so GitHub remembers the domain.

A `CNAME` file is **not** included here on purpose, so the site can be previewed or hosted on a github.io URL first. Add it when you are ready to attach the domain.

## What’s in this folder

- `index.html` — home page
- `projects/` — one page per project
- `assets/css/style.css` — styles (system fonts only; no external font or tracking requests)
- `assets/img/` — compressed images and short looping clips
- `assets/img/favicon.svg` — site icon

There is no build step. Edit the HTML or CSS and push again to update the live site.

Images were resized (max 1600px wide; a few extra-wide Maple level layouts were kept at 2400px so the layouts stay readable) and compressed to WebP. Old WordPress GIFs were converted to small looping MP4s. YouTube videos are embedded with `youtube-nocookie.com` iframes.

## itch.io for playable builds

GitHub Pages is a good home for the writeups. If you later want people to play desktop or WebGL builds, [itch.io](https://itch.io) is also free and is a better place to host the actual games.
