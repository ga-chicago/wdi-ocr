## Sass Refresher

- `touch index.html`
- `mkdir styles scripts`
- `touch styles/main.scss scripts/app.js`

```bash
$ tree
.
├── index.html
├── scripts
│   └── app.js
└── styles
    └── main.scss

2 directories, 3 files
```

- `sass --watch styles/main.scss:styles/main.css`

```bash
>>> Sass is watching for changes. Press Ctrl-C to stop.
      write styles/main.css
      write styles/main.css.map
[Listen warning]:
  Listen will be polling for changes. Learn more at https://github.com/guard/listen#polling-fallback.
```

**Result**:

```bash
$ tree
.
├── index.html
├── scripts
│   └── app.js
└── styles
    ├── main.css
    ├── main.css.map
    └── main.scss

2 directories, 5 files
```
