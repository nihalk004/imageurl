# ImageURL

A small browser-based image uploader for this repository. Upload an image, get a direct URL that opens as the image itself, and export the uploaded links to an Excel workbook.

## Run it

Open `index.html` in a browser, or enable GitHub Pages for this repository (deploy from the `main` branch and `/` folder) to host it as a website.

## Uploading images

1. Create a **fine-grained personal access token** for `nihalk004/imageurl` with **Contents: Read and write** repository permission. The token must have access to the target branch.
2. Open the app and enter the token and target branch (`main` by default).
3. Choose or drag in PNG, JPG/JPEG, GIF, or WebP images (up to 10 MB each), then select **Upload images**.
4. Copy a direct URL from the results list, or select **Download Excel** to save `image-urls.xlsx` with the image names, URLs, and upload times.

Images are committed under `images/`. Since this is a public repository, uploaded files and their raw image links are public. The token is held only in the open page and is sent only to GitHub's API; it is not saved in browser storage or included in the repository. Close or reload the page to clear the token and current upload list.

The Excel export uses SheetJS from jsDelivr, so an internet connection is needed for that library to load.
