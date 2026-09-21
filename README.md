# Tyler Franke: academic website

A one-page academic site built with Jekyll, which GitHub Pages runs for you.
You never need to touch HTML to update your papers, talks, conferences,
visits or teaching: each list lives in its own small text file in `_data/`.

## Put it online

1. Create a public GitHub repository named **`<username>.github.io`**
   (use your own GitHub username).
2. Upload all files in this folder to the repository (keep the folder structure,
   including the folders that start with `_`).
3. In the repository, open **Settings > Pages**, set *Source* to
   "Deploy from a branch", branch `main`, folder `/ (root)`.
4. In `_config.yml`, replace `USERNAME` in the `url` line with your username.
5. After a minute or two the site is live at `https://<username>.github.io`.

## Everyday edits

| To change | Edit |
| --- | --- |
| Papers and preprints | `_data/papers.yml` |
| Talks | `_data/talks.yml` |
| Conferences attended | `_data/conferences.yml` |
| Research visits | `_data/visits.yml` |
| Teaching | `_data/teaching.yml` |
| Name, position, email, profile links | `_config.yml` |
| About and research text | `index.html` (the lorem ipsum paragraphs) |
| CV | replace `assets/cv.pdf` (keep the file name) |
| Photo | add e.g. `assets/img/photo.jpg`, then set `photo:` in `_config.yml` |
| Colours | the variables at the top of `assets/css/style.css` |

You can edit any of these directly on github.com (click the file, then the
pencil icon). Each data file starts with a commented template to copy.

Things to keep in mind:
- Write dates as `YYYY-MM-DD`. Lists are sorted automatically, newest first,
  and only month and year are displayed.
- Indentation matters in `.yml` files: use spaces, not tabs, and line fields
  up under each other as in the examples.
- If a data file has no entries, its section and menu link disappear.
- Put quotes around text containing a colon, e.g. `title: "Skeins: a survey"`.
- If the site stops updating, open the **Actions** tab on GitHub; a failed
  build there shows which file and line caused the problem.

## Being found by search engines

The page already includes a descriptive title and summary, structured data
identifying you as a person at Universität Hamburg, a sitemap and robots.txt.
To get it indexed quickly:

1. Add the site in [Google Search Console](https://search.google.com/search-console)
   (choose "URL prefix", verify with the HTML-tag method by pasting the tag into
   `_includes/head.html`), then submit `sitemap.xml`. Bing Webmaster Tools can
   import the same setup.
2. Link to the site from places search engines already trust: your university
   or CRC 1624 profile page, arXiv, ORCID, Google Scholar and GitHub profiles.
3. Fill in the `links:` in `_config.yml`, which tells search engines those
   profiles belong to the same person.

New sites typically take from a few days to a few weeks to appear for a name
search.

## Preview on your own computer (optional)

With Ruby installed: `bundle install`, then `bundle exec jekyll serve`,
and open http://localhost:4000.
