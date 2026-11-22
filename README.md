# yelbandrawy.github.io

My personal site. It's plain HTML and CSS, with no build step and no JavaScript.

- `index.html`: all the content
- `styles.css`: styles (follows the system's light or dark setting)
- `assets/`: photo, CV, favicon
- `.nojekyll`: tells GitHub Pages to serve the files as they are

## Run locally

    python3 -m http.server 8080

## Deploy (GitHub Pages)

1. Create a public repo named `YElbandrawy.github.io`.
2. Push this folder to its `master` branch (the repo's default).
3. In the repo, open Settings → Pages and set Source to "Deploy from a branch", with `master` and `/ (root)`.
4. The site goes live at https://yelbandrawy.github.io/ a minute or two later.

If you use a different repo name (for example `portfolio`), the site lives at
`https://yelbandrawy.github.io/portfolio/`. All links are relative, so it still works,
but update the `og:url` and `og:image` tags in `index.html` to match.

## Public CV

`assets/Youssef-Eid-Elbandrawy-Resume.pdf` is a public version of the CV. Its source is `cv/source.html`.
Compared with the full CV in `~/archive/CVs`, it leaves out the phone number and the internal and
implementation details of employer projects. After editing the source, regenerate the PDF with:

    google-chrome --headless=new --no-pdf-header-footer \
      --print-to-pdf=assets/Youssef-Eid-Elbandrawy-Resume.pdf cv/source.html

Note: every file in this repo is public on GitHub Pages, so don't put the full CV here.
