# Academic website

A personal academic homepage based on the supplied CV and photograph. The white background, restrained typography, photo sidebar, About me introduction, and text-led publication list take inspiration from [Maxime Bouscary](https://mbscry.github.io/) and [Wes Gurnee](https://wesg.me/). The owner's name appears once in the profile, with the original author lists preserved for publications.

## Preview

Open `index.html` in a browser, keeping the `assets` folder beside it. No build step or dependencies are required. You can also serve this folder locally:

```bash
python3 -m http.server 8000
```

Open `http://localhost:8000`.

## GitHub Pages

For a new static site:

1. Create or select a repository named `YOUR-USERNAME.github.io`.
2. Upload this folder's contents, including `index.html`, `assets`, and `.nojekyll`, to the root of the publishing branch.
3. In **Settings → Pages**, select **Deploy from a branch**, choose your publishing branch and **/ (root)**, then **Save**.
4. Open the address shown in Pages settings after deployment completes.

All asset links are relative, so this also works as a project site under a repository path.

The existing `afriatg/afriatg.github.io` repository uses Jekyll and AcademicPages. This package is a standalone static version. To retain that repository's current Jekyll setup and other pages, integrate the content into `_pages/about.md`, update the author fields in `_config.yml`, and add the photograph and CV to the repository's image and file directories. Do not add `.nojekyll` to a deployment that should continue to build Jekyll pages.

Official reference: [Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

## Edit

- **Biography:** edit the `about` section of `index.html`. It describes the owner as a fifth-year PhD student in Operations Research at MIT.
- **Publications:** copy a `<li class="paper">` into the appropriate conference/journal or workshop list and edit the title, author list, venue, year, and paper links.
- **Experience, education, and teaching:** edit the corresponding named sections in `index.html`.
- **Photo:** replace `assets/profile.jpg`. The supplied photo is unchanged; CSS provides the circular framing and zoom. Adjust `.portrait img` to change `object-position` or `transform: scale(...)`.
- **CV:** replace `assets/CV_Gabriel_Afriat.pdf`, keeping the filename.
- **Links:** the sidebar contains email, Google Scholar, LinkedIn, and the CV download.
- **Style:** edit the embedded CSS. The site uses system fonts and no network-loaded assets.

The content and navigation links remain available without JavaScript. JavaScript adds a compact mobile navigation menu. Keyboard focus, a skip link, reduced-motion support, and print styles are included.

## Files

- `index.html` — complete page, styles, and navigation script.
- `assets/profile.jpg` — supplied photograph.
- `assets/CV_Gabriel_Afriat.pdf` — PDF converted from the supplied CV.
- `.nojekyll` — for standalone static deployments.
- `README.md` — preview, editing, and publishing instructions.
