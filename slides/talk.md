# Your Talk Title

### A subtitle, if you want one

Nick Cernak

Note:
This is a speaker note. Press **S** during the talk to open the
speaker view — notes, a timer, and the upcoming slide, all in a
separate window you keep on your laptop.

---

## Writing slides

Every slide is plain Markdown in `slides/talk.md`.

Three separators are all you need:

- `---` starts a new slide
- `--` nests a slide *below* the current one
- `Note:` begins speaker notes

---

## Building a point

Reveal items one at a time with `fragment`:

- First this <!-- .element: class="fragment" -->
- then this <!-- .element: class="fragment" -->
- and finally this <!-- .element: class="fragment" -->

Note:
Fragments advance with the same arrow key as slides, so you don't
have to think about it while presenting.

---

## Showing code

```js
Reveal.initialize({
  hash: true,
  slideNumber: 'c/t',
  plugins: [RevealMarkdown, RevealHighlight]
});
```

Syntax highlighting is automatic — just name the language.

---

## Vertical slides

Press **↓** to go deeper, **→** to skip ahead.

Useful for optional detail you can drop if you're running short.

--

### Backup detail

Nested slides are the escape hatch for the question you *might*
get asked. Keep them here rather than cutting them.

--

### More backup

Press **→** to rejoin the main thread.

---

## Images

Drop files in `images/` and reference them normally:

```markdown
![Alt text](images/diagram.png)
```

Alt text matters — some conferences publish decks for screen readers.

---

## Presenting

| Key | Does |
|-----|------|
| `S` | Speaker view, with notes and timer |
| `F` | Full screen |
| `O` | Overview of every slide |
| `B` | Black out the screen |
| `Ctrl/Cmd` + click | Zoom into a region |

---

## Handing out the deck

Append `?print-pdf` to the URL and print to PDF from the browser.

That gives you one page per slide, ready to email to organizers.

---

# Thank you

Questions?

Note:
Leave this slide up during Q&A — it keeps your name and contact
on screen while people are deciding whether to ask.
