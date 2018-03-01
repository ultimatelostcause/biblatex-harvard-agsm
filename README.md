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

# Known Issues

## Major

* Citations do not include contribution type.
* Pseudo-dates "forthcoming" and "in press" not supported.
* A separate entry needs to be created in the bibliography file to generate stub references for short author names.
* Citation-only format for newspaper articles not support.
* Special sources not supported.
* Order of details in related entry incorrect.


## Minor

* Name suffix appears after family name rather than after given initials in reference list.
* "vol." used instead of "vols" for volume range in reference list.
* Special characters in page number not supported in bibliography file entries without also specifying "p.".
* Extended date components displayed in wrong order in reference when URL specified. (The AGSM states on p. 230 that "A document within a web site can usefully be considered in the same way as a published document or a book".  However, the media release example contradicts this by moving the day and month before the publisher and location, which differs from the usual ordering described for media releases at p. 207, and there is no explicit mention of the need to re-order these components.)
* Title of mail list displayed in italics rather than quoted in normal font.
* Email address of mail list user wrapped in parentheses.

## Trivial

* A comma is used instead of a semi-colon to separate multiple citations of works by the same author when page numbers are given.
* Year range is not shown in compact format.