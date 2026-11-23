# Repository guidance

## Layout

- `slides/roland-slides.org`: THE User Manual.
- `slides/roland-mng-slides.org`: Meet and Greet.
- `images/`: shared assets, accessible through the `slides/images` symlink.
- `scripts/`: Org export and browser-based PDF rendering from `reveal-template`.
- `Makefile`: discovers `slides/*-slides.org` and optional `docs/*-doc.org`.
- `public/`: ignored generated HTML and PDFs, including compatibility copies at
  `roland.html` and `roland-mng.html` for existing links.
- `.github/workflows/deploy.yml`: builds and deploys `public/` to GitHub Pages.

## Making changes

Edit the Org sources and shared images. Keep both decks' 1280 × 720 layout
consistent with `reveal-template`. Keep generated files out of source control.
See [README.md][] for prerequisites and publishing setup.

## Verification

Run `make publish` for deck edits. Run `make -B publish` after changing images,
shared includes, or build scripts because these dependencies are not tracked by
Make. Inspect both HTML decks in a browser, check local image loading and speaker
notes, and verify the PDFs with `pdfinfo` and `pdftotext`. Run
`git diff --check` before committing.

`make clean` removes generated outputs from `public/`. `make clean-full` also
removes HTML, PDF, and TeX files elsewhere in the repository; avoid it if reference
documents have been added.

[README.md]: README.md
