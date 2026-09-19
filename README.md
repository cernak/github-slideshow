# Slideshow

A [reveal.js](https://revealjs.com) presentation deck. Slides are written in
Markdown; the deck is plain static HTML with no build step.

**Live:** https://cernak.github.io/github-slideshow/

## Writing a talk

Edit [`slides/talk.md`](slides/talk.md). Three separators do the work:

| Syntax  | Meaning                                    |
| ------- | ------------------------------------------ |
| `---`   | Start a new slide                          |
| `--`    | Nest a slide below the current one         |
| `Note:` | Everything after this becomes speaker notes |

Images go in `images/` and are referenced as `![Alt text](images/name.png)`.

To change the look, swap the theme stylesheet in [`index.html`](index.html).
Dark rooms suit `black`, `league`, or `moon`; bright rooms and washed-out
projectors suit `white` or `beige`. There are `black-contrast` and
`white-contrast` variants when legibility matters most.

## Previewing locally

```sh
npm start
```

Then open <http://localhost:8000>. Any Python 3 install will do — there's no
Ruby, no bundler, and no Node runtime needed just to preview.

A local server is required because the browser fetches `slides/talk.md` over
HTTP; opening `index.html` directly from the filesystem will show an empty
deck.

## Presenting

| Key                | Does                               |
| ------------------ | ---------------------------------- |
| `S`                | Speaker view — notes, timer, next slide |
| `F`                | Full screen                        |
| `O`                | Overview of every slide            |
| `B`                | Black out the screen               |
| `Ctrl`/`Cmd` + click | Zoom into a region               |

For a PDF handout, open the deck with `?print-pdf` appended to the URL and
print to PDF from the browser.

## Updating reveal.js

The `reveal/` directory is a committed copy of the library, so that GitHub
Pages can serve it without a build step. To pull in a new version:

```sh
npm install reveal.js@latest
npm run vendor
```

Commit the resulting changes to `reveal/`, `package.json`, and
`package-lock.json`. Dependabot watches `package.json` and will open a pull
request when a new release or security fix appears — run `npm run vendor`
on that branch before merging, so the served copy matches the lockfile.

## Deployment

GitHub Pages serves this repository directly from the default branch. The
`.nojekyll` file tells Pages to publish the files as-is rather than running
them through Jekyll. Pushing to `main` is the whole deploy process.

## License

[MIT](LICENSE)
