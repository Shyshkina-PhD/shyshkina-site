# shyshkina.eu

Independent static website for Tetiana Shyshkina.

## Preview locally

Open `index.html` in a browser, or run:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a public GitHub repository, for example `shyshkina-site`.
2. Upload all files from this folder to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then save.
6. GitHub will publish the site at `https://YOUR-USERNAME.github.io/shyshkina-site/`.

## Connect shyshkina.eu later

Do this only after the GitHub Pages preview is ready.

1. In **Settings → Pages → Custom domain**, enter `shyshkina.eu`.
2. Add a file called `CNAME` to the repository root containing only:

```
shyshkina.eu
```

3. At the domain provider, change only the website records required by GitHub Pages.
4. Do **not** delete or change Zoho MX, SPF, DKIM, or DMARC records. They control email.
5. After DNS is verified, enable **Enforce HTTPS** in GitHub Pages.

## Replace images

Put optimised images in `assets/images/` and replace a placeholder such as:

```html
<div class="media-placeholder photo-a"><span>Photograph 01</span></div>
```

with:

```html
<figure class="photo-a real-image">
  <img src="assets/images/photo-01.jpg" alt="Brief factual description">
</figure>
```

Add this CSS:

```css
.real-image { margin: 0; overflow: hidden; }
.real-image img { width: 100%; height: 100%; object-fit: cover; display: block; }
```

Recommended export: JPEG/WebP, 1600–2200 px on the long edge, usually below 500 KB.

## CV

Place the PDF at:

`assets/files/tetiana-shyshkina-cv.pdf`

The existing Download CV link will then work.
