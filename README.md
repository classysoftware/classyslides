# ABOUT

This package provides the **classyslides** beamer theme and extensions.

## USAGE

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
   ln -s classyslides/source/beamerthemeclassyslidesbase.sty
   ln -s classyslides/source/beamerthemeclassyslidesfonts.sty
   ln -s classyslides/source/beamerthemeclassyslidesdark.sty
   ln -s classyslides/source/beamerthemeclassyslideslight.sty
   ```
4. Edit your presentation and compile

```bash
# Compile twice to see references etc.
pdflatex quickstart.tex
pdflatex quickstart.tex
```

Alternatively, you can add the source folder `$path/source` as a local style file. The correct way of doing this depends on your plattform and LaTeX distribution. A thorough instruction for multiple platforms/distributions can be found [here][1].

## FEATURES

**Classyslides** is a minimalistic beamer theme with focus on clear layout and efficient use of space.

Main features:

- Dark and light theme (extensions `beamerthemeclassyslideslight.sty` and `beamerthemeclassyslidesdark.sty`)
- Preconfigured block, theorem and code environments:
  - `Block`
  - `Definition`
  - `Example`
  - `Theorem`
  - `Proof`
  - `Code` (uses the `listings` package via `tcolorbox`)

# EXAMPLES

The PDF files in `$path/examples` are compiled from the example presentation `$path/examples/euclid.tex` (adopted from the beamer manual). They illustrate the output using the `beamerthemeclassyslidesfonts.sty` extension for each theme extension.

[1]: http://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te
