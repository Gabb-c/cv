# cv

My modular LaTeX CV. Compiled with LuaLaTeX, published as a PDF release on every push to `main`.

## Structure

```
src/
├── main.tex            # document root — packages, fonts, section includes
├── config.tex          # page setup, accent color, custom commands
└── sections/           # one file per CV section
    ├── heading.tex
    ├── summary.tex
    ├── skills.tex
    ├── experience.tex
    ├── projects.tex
    ├── education.tex
    └── languages.tex
```

## Build locally

Requires a LuaLaTeX-capable TeX distribution (e.g. TeX Live) with `latexmk`.

```sh
cd src
latexmk -lualatex main.tex
```

Output: `src/main.pdf`.

## Release

The [`Publish CV`](.github/workflows/publish-cv.yml) workflow compiles `src/main.tex`
and attaches `Gabriel_Da_Cunha_CV.pdf` to a dated GitHub Release on every push to
`main` that touches `src/**`.
