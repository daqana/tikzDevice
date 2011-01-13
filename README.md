#**This is an active integration branch for version 0.6**

This means wild things may happen at any moment.  History may get re-written.
Upstream rebases may occur.  **Pull at your own peril.**


# tikzDevice

---

## Description

The tikzDevice package new graphics device for R which enables direct
output of graphics in a LaTeX-friendly way.  Plotting commands issued
by R functions are transformed into LaTeX code blocks.  These blocks
are interpreted with the help of TikZ-- a graphics library for TeX and
friends written by Till Tantau.

The tikzDevice supports three main modes of output:

  - Figure chunks: placed in .tex files and suitable for inclusion in
    LaTeX documents via the \input{} command.

  - Stand alone figures: Complete LaTeX documents containing figure
    code that can be compiled into stand-alone images.  Pages are
    cropped to the size of the figure using the LaTeX preview package.

  - Console output: TikZ code is returned directly to the R console
    as a character vector for further manipulation.


## Beta Notice

The tikzDevice is currently flagged as a beta work.  The package is
reasonably stable and has been used by the authors to produce graphics
for academic publications for over a year.  The reason for beta status
is that there are several open design issues- two of which are:

  - Providing support for UTF8 text.

  - Supporting TeX variants other than LaTeX.

Resolving these issues may require changes to the tikzDevice that break
backwards compatibility with previous versions.  The beta flag is a reminder
that such changes may occur- although we will strive to avoid them if possible.

The beta flag will be removed upon release of version 1.0. At this time the
tikzDevice will switch to [semantic versioning][1] and changes that
break backwards compatibility will happen rarely and will incur a major release.

  [1]: http://www.semver.org


## Obtaining the Package

Stable versions of the tikzDevice may be downloaded from CRAN:

    install.packages( 'tikzDevice' )

Development versions may be obtained from R-Forge:

    install.packages( 'tikzDevice', 
      repos='http://r-forge.r-project.net' )


## Reporting Bugs and Getting Help

The tikzDevice has a dedicated mailing list courtesy of R-Forge.  The
mailing list is the easiest way to get answers for questions related
to usage:

  tikzdevice-bugs @at@ lists.r-forge.r-project.org 

Primary development takes place on GitHub.  Bugs and feature requests
may be made by opening issues at the primary repository:

  http://github.com/Sharpie/RTikZDevice/issues

Adventurous users are encouraged to fork the repository and contribute
to the development of the device!


## Latest Changes
*See the CHANGELOG for changes that occurred in previous releases*

---

### Version: 0.5.4
*Under development, will most likely become 0.6.0*

#### Behind the Scenes

- New Makefile for executing common development tasks.

- Package documentation now handled by `roxygen`.  Thanks to Hadley Wickham and
  Yihui Xie for the `Rd2roxygen` package which facilitated this switch.

- Package test suite completely overhauled and now based on Hadley Wickham's
  `test_that` package.

---
