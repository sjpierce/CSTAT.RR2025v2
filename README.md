# README
Steven J. Pierce

<!-- README.md is generated from README.Rmd. Please edit that file -->

# CSTAT.RR2025v2: Materials For CSTAT Webinar on Reproducible Research

<!-- badges: start -->

[![](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
[![Project Status: WIP - Initial development is in progress, but there
has not yet been a stable, usable release suitable for the
public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)
<!-- badges: end -->

This repository holds materials for one of my professional presentations
(Pierce, 2025, October 2). Its primary purpose is for me to use version
control tools while developing my slides, but its secondary purposes
include distributing the slides to my audience and demonstrating how to
use Quarto to create slides.

There are two different types of users of this repository: myself and my
audience. I assume most of my audience just wants copies of my slides,
but some may want to see exactly how they were created by examining
other parts of the repository (especially the Quarto scripts).

Since there are no other contributors, I am omitting details that may
otherwise be useful to collaborators. However, here is a link to my web
page on [software for reproducible research with
R](https://sjpierce.github.io/rr_software.html). This presentation uses
the Quarto extension called `reveal-header`
(https://github.com/shafayetShafee/reveal-header). Installing that
created the `_extensions/` subfolder here.

## Obtaining the Slides & Example Files

For each of the links below, you will land on a GitHub page that has a
*Download raw file* button in the upper right corner of the screen. Its
icon looks like an arrow pointing down into a tray. It is just to the
left of the pencil icon. Use that to download each file to your
computer.

The `*.qmd` files are Quarto scripts, while the corresponding `*.html`
files are the resulting rendered output. The output should work in
common web browsers like Chrome, Edge, and Firefox.

- [`Slides.qmd`](https://github.com/sjpierce/CSTAT.RR2025v2/blob/main/Slides.qmd)
  *This is the code that creates the slides.*
- [`Slides.html`](https://github.com/sjpierce/CSTAT.RR2025v2/blob/main/output/Slides.html)
  *These are final final slides.*

## Usage Tips

- After you open the `Slides.html` file on your computer, press the `s`
  key on your keyboard to see the speaker view that contains my speaker
  notes.
- There are also other [slide navigation keyboard
  shortcuts](https://quarto.org/docs/presentations/revealjs/presenting.html).
- Try opening both a Quarto script and the output it generates and look
  at them side-by-side. For more intensive examination of how things
  work, see the Rendering the Scripts section below.

## Repository Structure and Contents

The structure for the repository is shown in the outline below, where
folder names and file names are `highlighted like this` and comments are
in normal text. The repository is set up as an [RStudio
project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-RStudio-Projects).

- `CSTAT.RR2025/`: This is the root folder for the repository.
  - `.git/`: This hidden folder is used by Git. Leave it alone!
  - `.quarto/`: This hidden folder may be created by Quarto to hold
    temporary files. Do not edit or delete any of these files unless you
    know what you are doing! This folder is not tracked by Git.
  - `.Rproj.user/`: This hidden folder is used by Rstudio. Leave it
    alone!
  - `_extensions/`: This folder contains files for Quarto extensions
    used by my presentation slides.
  - `graphics/`: This folder stores `.jpg` and `.png` graphics files
    used in my slides and example files.
  - `output/`: This folder holds rendered output from scripts in this
    Quarto project.
    - `graphics/`: This subfolder is created when you render the slides
      or other scripts. It holds temporary copies of graphics files used
      to create the HTML output files. You can ignore or delete it.
    - `site_libs/`: This folder holds shared files for a website that
      get created when I render the scripts. They include things like
      CSS, JavaScript, and HTML widget libraries, which help to avoid
      duplicating files across multiple output documents.
    - `Slides.html`: These are the slides used during the presentation.
  - `.gitignore`: This file tells Git what files to ignore and omit from
    synchronizing with the main repository on GitHub.
  - `_brand.yml`: This Quarto metdata file contains color palette, font,
    and logo settings for CSTAT branding that get applied across slides
    and other outputs.  
  - `_quarto.yml`: This is a Quarto metadata file containing
    project-level YAML code that will be inherited by Quarto scripts in
    this folder or its subfolders.  
  - `apa.csl`: This is a citation style language file for the
    Publication Manual of the American Psychological Association, 7th
    edition. It is used by Quarto to format references.
  - `apa-numeric-superscript-brackets.csl`: This is a citation style
    language file for the Publication Manual of the American
    Psychological Association, 7th ed. that has been adapted to use
    numeric superscripts in square brackets for in-text citations and
    put the reference list in the order the citations were used. It is
    used by Quarto to format reference sections.
  - `CSTAT_style.css`: This custom style sheet provides logo and title
    banner formatting settings and classes for my HTML outputs. It
    supplements `_brand.yml` and `CSTAT_theme.scss`.
  - `CSTAT_theme.scss`: This is a Sassy custom style sheet file to
    provide formatting settings and classes for my slides and other HTML
    outputs. It supplements `_brand.yml` and `CSTAT_style.css`.
  - `CSTAT.RR2025.Rproj`: This is an RStudio project file. It contains
    some settings for working with the project in that software.
  - `README.md`: This file is obtained by knitting the `README.qmd` file
    and is used by GitHub to display information about the repository.
    Do not edit it manually: just re-knit `README.qmd` to update it. In
    R Studio, you can read the formatted version by opening the file and
    clicking the Preview button.
  - `README.qmd`: This file gives an introduction to the repository.
    Rendering it produces the `README.md` file and opens the preview
    automatically.
  - `references.bib`: This is a BibTeX file containing citation data for
    papers, software, etc. that we want to cite anywhere in our Quarto
    scripts throughout the package.
  - `Slides.qmd`: This is the Quarto script that creates the slides.
    Rendering it creates my final HTML slides in the file
    `output/Slides.html`.

## Rendering The Scripts

This section is for users who want to do more than just casually examine
the slides and example files side by side. The best way to learn is to
actually install all the software and then try rendering some files
yourself. To render either my presentation slides or my other example
Quarto scripts from the source code:

- Install the necessary [software for reproducible research with
  R](https://sjpierce.github.io/rr_software.html).
- Download or clone the repository to your computer (preferably using
  Git).
- Double-click the `CSTAT.RR2025v2.Rproj` file from Windows Explorer to
  open the RStudio project.
- Use RStudio to open the relevant Quarto script file (e.g.,
  `Slides.qmd`).
- Click the *Render* button in RStudio source editor pane.

That will generate the output file (e.g., `output/Slides.html`) and
overwrite any prior version of it that exists in your local copy of the
repository.

## References

<div id="refs" class="references csl-bib-body hanging-indent"
entry-spacing="0" line-spacing="2">

<div id="ref-Pierce-RN8764" class="csl-entry">

Pierce, S. J. (2025, October 2). *Reproducible research: Principles,
practices, and tools for generating reproducible statistical analyses
and reports* \[Online seminar\]. Center for Statistical Training and
Consulting webinar series on Responsible and Ethical Conduct of
Research, East Lansing, MI, United States.
<https://github.com/sjpierce/CSTAT.RR2025v2>

</div>

</div>

## Citing This Repository

Please cite my actual presentation (Pierce, 2025, October 2).

## License

This work is licensed under [CC BY-NC-SA
4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/?ref=chooser-v1).
To view a copy of this license, visit
<https://creativecommons.org/licenses/by-nc-sa/4.0/>

The following exceptions apply:

- Graphics files for the Michigan State University (MSU) wordmark and
  the logos for the Center for Statistical Training and Consulting
  (CSTAT) do not fall under the CC BY-NC-SA license. They are
  intellectual property owned by Michigan State University. I use them
  for branding purposes because I am an MSU employee.
- Similarly, I assume that graphics files for the logos of National
  Institutes of Health (NIH), the National Science Foundation (NSF), and
  the Institute of Education Sciences (IES) are the intellectual
  property of their respective organizations and also do not fall under
  the CC BY-NC-SA license. Their use in this repository should fall
  under fair use provisions of trademark law.
