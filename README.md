# Description

A biblatex implementation of the author-year (aka Harvard) citation and referencing style per the Australian Government Style Manual (6th ed). 

# Prerequisites

* The standard biblatex `author-year` style (version 3.7).
* The `xpatch` package.

# Installation

Either:
* Copy the `.bbx` and `.cbx` files to the `bbx` and `cbx` directories respectively of your biblatex installation.
* Clone the repository locally, and configure the repository directory as a LaTeX root directory.

# Usage

Add the following to your LaTeX document:
```latex
\usepackage[style=harvard-agsm,backend=biber,defaultpkgs]{biblatex}
```

The `defaultpkgs` option is optional.  If enabled, the `babel` package will be loaded with the Australian locale, and the `csquotes` package will be loaded with the British English format.

The `xpatch` package will always be loaded.