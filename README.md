# THE User Manual

Roland Tritsch's presentations about his background, values, and working together:

- [THE User Manual][manual]
- [Meet and Greet][meet-and-greet]

## Build and preview

Install [Emacs][] with [org-re-reveal][] configured and [Node.js][] with
[Puppeteer][] installed globally (`npm install -g puppeteer`). Then run:

```sh
make publish
```

Open `public/roland-slides.html` or `public/roland-mng-slides.html` in a browser.
Each deck also has a PDF and a `_with-notes.pdf` version in `public/`.
The build also creates `roland.html` and `roland-mng.html` to preserve existing
presentation URLs.

## Publish

The GitHub Actions workflow builds and deploys `public/` on pushes to `trunk`
or a manual workflow run. The repository's Pages build source is configured as
**GitHub Actions**, replacing the previous deployment from `trunk`'s `docs/`
directory.

See [AGENTS.md][] for the repository layout and verification steps.

[manual]: https://tedn.life/reveal-roland/roland.html
[meet-and-greet]: https://tedn.life/reveal-roland/roland-mng.html
[Emacs]: https://www.gnu.org/software/emacs/
[org-re-reveal]: https://gitlab.com/oer/org-re-reveal
[Node.js]: https://nodejs.org/
[Puppeteer]: https://pptr.dev/
[AGENTS.md]: AGENTS.md

