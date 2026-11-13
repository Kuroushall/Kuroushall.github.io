# Kuroush Allameh: personal website

A minimal academic homepage in plain HTML and CSS. There is no build step, no framework and no JavaScript, so GitHub Pages serves these files exactly as they are, and you can preview the site by opening `index.html` in a browser.

## Publish on GitHub Pages

1. On GitHub, create a new **public** repository named exactly **`USERNAME.github.io`**, where `USERNAME` is your GitHub username.
2. Put the contents of this folder in it, either by dragging the files onto the repository page ("uploading an existing file") or from a terminal:

   ```sh
   cd homepage
   git init -b main
   git add .
   git commit -m "Personal website"
   git remote add origin https://github.com/USERNAME/USERNAME.github.io.git
   git push -u origin main
   ```

3. In the repository, open **Settings → Pages** and check that **Source** is *Deploy from a branch*, with branch **`main`** and folder **`/ (root)`**.
4. About a minute later the site is live at `https://USERNAME.github.io`. Every later push updates it.

## Editing

| To change | Edit |
| --- | --- |
| Bio, email, news | `index.html` |
| Papers | `publications.html` |
| Menu at the top | the `<nav>` block, which appears in both `index.html` and `publications.html` |
| Colours, font, spacing | the variables at the top of `style.css` |

- **News item:** copy one `<li>` line in the News list, put it at the top and edit it.
- **New paper:** copy one `<li> … </li>` block in `publications.html` to the top of the list. The list is numbered newest first and renumbers itself.
- **CV:** add `cv.pdf` to the repository, then remove the comment marks `<!--` and `-->` around the CV line in the menu of both pages.
- **Notation:** AdS<sub>3</sub> is written `AdS<sub>3</sub>`, and T T̄ is written `T<span class="bar">T</span>`.

## Files

```
index.html          home page: bio, email, news
publications.html   list of papers
404.html            page shown for broken links
style.css           all styling, including a dark mode
favicon.svg         browser-tab icon
fonts/              EB Garamond, served from the site itself (SIL Open Font License, see fonts/OFL.txt)
.nojekyll           tells GitHub Pages to serve the files as they are, without running Jekyll
```
