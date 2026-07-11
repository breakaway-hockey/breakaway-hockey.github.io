# Breakaway — site source

A Jekyll site for women's & girls' hockey gear guides and coaching content,
built to host free on GitHub Pages.

## What's in here

- `_config.yml` — site title, description, plugins
- `index.html` — homepage (hero + auto-updating post grids)
- `about.md`, `affiliate-disclosure.md` — static pages
- `_posts/` — every blog post lives here as one Markdown file
- `_layouts/`, `_includes/` — the templates and header/footer (you shouldn't need to touch these often)
- `assets/css/style.css` — all site styling in one file

## 1. Put this on GitHub

1. Create a **free GitHub account** at github.com if you don't have one.
2. Create a **new repository**. If you want the site at `yourname.github.io`,
   name the repo exactly `yourname.github.io` (replace `yourname` with your
   GitHub username). This gets you the cleanest free URL.
   - If you'd rather use a different repo name, that's fine too — your site
     will just live at `yourname.github.io/repo-name` instead, and you'll
     need to set `baseurl: "/repo-name"` in `_config.yml`.
3. Upload all the files in this folder to that repository (drag-and-drop
   works fine on GitHub's web interface — you don't need to use the command
   line if you don't want to).

## 2. Turn on GitHub Pages

1. In your repo, go to **Settings → Pages**.
2. Under "Build and deployment," set **Source** to "Deploy from a branch."
3. Set **Branch** to `main` (or `master`) and folder to `/ (root)`.
4. Save. Give it 1–2 minutes, then your site will be live at
   `https://yourname.github.io` (or the project URL if you used a different
   repo name).

No hosting bill, no server to manage. It rebuilds automatically every time
you update a file in the repo.

## 3. Publishing a new post (the part you'll do most often)

1. Go to the `_posts` folder in your repo.
2. Duplicate an existing post file as a starting point.
3. Name the new file `YYYY-MM-DD-your-post-title.md` — the date at the front
   of the filename is required by Jekyll and controls where it sorts.
4. Edit the front matter at the top of the file:

```yaml
---
title: "Your Post Title Here"
category: "Gear Guide"   # or "Behind the Bench"
affiliate: true           # set to false if the post has no affiliate links
read_time: 6
excerpt: "One sentence describing the post — shows up on the homepage card."
---
```

5. Write the post body in Markdown below the `---`.
6. Commit the change on GitHub. The live site updates automatically within
   a couple of minutes.

## 4. Adding affiliate links

Once you're approved for a program (Amazon Associates, REI, etc.), just
drop the link in as normal Markdown:

```markdown
[Shop this skate on Amazon →](https://your-actual-affiliate-link-here)
```

Any post with `affiliate: true` in its front matter will automatically show
the disclosure box at the top — you don't need to add that by hand.

## 5. Custom domain (optional, later)

If you eventually buy a domain (e.g. `breakawayhockey.com`), GitHub Pages
supports it for free — you just add a `CNAME` file and update your DNS.
Not needed to launch; the free `github.io` URL works fine for Pinterest
links from day one.

## Local preview (optional)

If you want to preview changes on your own computer before publishing,
you'll need Ruby and Jekyll installed. Not required — editing directly on
GitHub and letting Pages rebuild is enough to run this site.

```bash
bundle install
bundle exec jekyll serve
# visit http://localhost:4000
```
