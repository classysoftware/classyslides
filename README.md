# classyslides

This package provides the **classyslides** beamer theme and extensions.

## USAGE

### BASIC USAGE

1. Set up **classyslides** as a local style file

   Comprehensive instructions for multiple platforms/distributions can be found in this [StackOverflow answer][1].

2. Create a Beamer presentation and import the **classyslides** theme using `\usetheme{classyslides}`

   ```latex
   \documentclass{beamer}

   % Select the classyslides theme
   \usetheme{classyslides}
   \mode<presentation>

   % Settings
   \title{My classy presentation}

   %
   % Document
   %
   \begin{document}

   \begin{frame}
   \titlepage
   \end{frame}

   \contentpagetrue
   \begin{frame}
     \frametitle{First slide}
     Stay classy!
   \end{frame}

   \end{document}
   ```

### USING THE QUICKSTART FILE

#### About the `quickstart.tex` file

The `quickstart.tex` file bootstraps a presentation with the following properties:

- Default font theme extension
- Header and footer extensions
- Light color theme
- Table of contents and references

#### Instructions

1. Create a folder for your presentation (under path `$path`)

   ```bash
   mkdir $path
   ```

2. Change to the presentation directory and pull this repository

   ```bash
   cd $path
   git clone https://github.com/classysoftware/classyslides.git
   ```

3. Copy the quickstart file in `./quickstart/quickstart.tex` and link the source files

   ```bash
   cp ./classyslides/quickstart/quickstart.tex .
   ln -s classyslides/source/* .
   ```

4. Edit your presentation and compile

   ```bash
   # Compile twice for correct page numbers, progress bar rendering, references etc.
   pdflatex quickstart.tex
   pdflatex quickstart.tex
   ```

## ABOUT

**Classyslides** is a minimalistic beamer theme with focus on clear layout and efficient use of space.

### FEATURES

- Default **font** theme (extension `beamerfontthemeclassyslides.sty`)
- Optional **header** and **footer** (extensions `beamerinnerthemeheader.sty` and `beamerinnerthemefooter.sty`)
- Optional **dark** and **light themes** (extensions `beamercolorthemeclassyslideslight.sty` and `beamercolorthemeclassyslidesdark.sty`)
- Preconfigured **block**, **theorem** and **code environments**:
  - `Block`
  - `Definition`
  - `Example`
  - `Theorem`
  - `Proof`
  - `Code` (uses the `listings` package via `tcolorbox`)

# EXAMPLES

Sample PDF outputs are provided in `./examples`. These files illustrate outputs for the example presentation `./examples/euclid.tex`---which was adopted from the beamer manual---for the following extension options:

- `euclid.pdf`
  - Only default fonts theme extension
  - Produced with `\usetheme[fonts]{classylides}`
- `euclid-light.pdf`
  - Default fonts theme and light color theme extensions
  - Produced with `\usetheme[fonts, colors=light]{classylides}`
- `euclid-dark.pdf`
  - Default fonts theme and dark color theme extensions
  - Produced with `\usetheme[fonts, colors=dark]{classylides}`
- `euclid-dark-light-header-footer.pdf`
  - Default fonts theme, light color theme, header and footer extensions
  - Produced with `\usetheme[fonts, header, footer, colors=dark]{classylides}`

[1]: http://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te
