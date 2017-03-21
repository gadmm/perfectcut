## Synopsis

I wrote the LaTeX package **perfectcut** to make commands of
abstract-machine-like calculi more readable when nested. It defines
(among others) the command `\perfectcut` with two arguments, which
displays a bracket whose size is determined by the number of nested
`\cutprimitive` (regardless of the contents). Here's an example of
usage:

```latex
\usepackage{perfectcut}
\let\cut\cutprimitive
\newcommand{\mt}{\tilde\mu}
\[
  \cut{t}{\mt x.\cut{u}{\mt y.\cut ve}}
  =
  \cut{u}{\mt y.\cut{t}{\mt x.\cut ve}}
\]
```

![Screenshot.](perfectcut.svg)

`perfectcut.sty` also offers a reimplementation of `\big`, `\bigg`,
etc. into robust and arbitrarily-size variants.

The manual has more examples and instructions.

The package is [hosted and updated on CTAN](https://www.ctan.org/pkg/perfectcut)
and can be obtained via your favorite LaTeX distribution.

## Use

See `perfectcut.pdf`.

## License

LPPL Version 1.3c. See `LICENSE`.

