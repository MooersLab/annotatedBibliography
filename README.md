![Version](https://img.shields.io/static/v1?label=annotatedBibliography&message=0.4&color=brightcolor)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

# Annotated bibliography template in LaTeX for specific writing projects

## Purpose
Generate lists of cited papers with annotations following each citation. This document is useful when writing review articles.

## How it works

These files support the automated generation of an annotated bibliography in LaTeX using bibliographic information in a BibTeX file (NOT BibLaTeX).
The *AnnoBib.tex* file is the master file.
It uses the *annote* field in the BibTeX entry in *cited.bib*.
Its style is set by *apacannx.bst*, which must be present unless this file is stored in your library of files for LaTeX on your local computer.


## Generate a bib file with only cited references

To write out the cited bib entries in a manuscript from *global.bib*, use the command line program **bibtool** with the main.tex file's corresponding main.aux file:
 
Run the following code to generate a bib file of the papers cited in a manuscript. 
Note that main.tex is the manuscript file. 
The *main.aux* file is hidden on Overleaf. 
Find it under the "Logs and outputs" pulldown menu. 

The following command will preserve the letter case in the cite key. 
The default behavior is to lower the case.

```bash
bibtool --preserve.key.case=on -x main.aux > cited.bib
```

Bibtool is distributed with LaTeX.

## Writing the annotations

Manually add *annote* fields to the *AnnoBibMyBDA.bib* file and enter your annotations.
Or, if you are more disciplined, you can add the *annote* fields in a *global.bib* file and repeat the extraction of the cited entries when you are finished.
All entries in `cited.bib` will be used to create the annotated bibliography regardless of whether the *annote* field is present.

The annote field does not have to be limited to a single paragraph summary like in the one you made in the sixth grade.
The annotation field can contain figures, tables, coding listings, and equations.

I store these files in an *annotatedBibliography* subfolder in my writing project's folder.
These files work on Overleaf, too.

## Alternative bibliographic styles

Alternatively, you can use the *IEEEannot.bst* bibliography style file that returns numbered entries in alphabetic order.

## Annote fields with multiple paragraphs

I have found no support for blank lines between paragraphs in the annotation.
I wrap each paragraph in `\par{\noindent   .... }` to have the paragraphs printed in block format.
I insert `\vspace{10pt}` between paragraphs to generate a blank line between paragraphs.
The result is visually pleasing to me.
Surprisingly, space will flank display math, figures, code listings, and tables.

### Annote fields with multiple paragraphs in BibLaTeX
You may be using BibLaTeX if you use typist because typist does not support BibTeX.
BibLaTeX uses different tools then BibTeX to generate the bibliography.
Its tool `biber` converts blank lines into whitespace early in the processing of the bib file.
You can start new paragraphs separated by blank lines in an [imported tex file](https://tex.stackexchange.com/questions/488913/how-to-embed-a-review-in-biblatex) that stores a single annotation.
However, the blank line will be lost in the exported PDF.

You can use the biblatex-chicago package, which has added support for [annotated bibliographies](https://tex.stackexchange.com/questions/183743/why-cant-i-get-annotations-in-the-bibliography-here/183917#183917).
You can add `\par` after each paragraph to break the text into paragraphs, but there will be no spacing between paragraphs.
The result is visually displeasing to me.
<img width="965" alt="par" src="https://github.com/user-attachments/assets/50e3c510-408a-4eac-89f8-fd8d158ce474">

A work around is to replace the `\par` with display `$$ $$`. 
This will give a wider than desired paragraph spacing, but it is better than no blank lines.

<img width="970" alt="emptyDisplayMath" src="https://github.com/user-attachments/assets/68fef0c3-7691-4978-bea8-e07f8a145ab4">



## Colored annotations

You can color the annotation blue.

- Load the *color* or *xcolor* package with the `\usepackage{xcolor}` macro in the preamble of the *main.tex* file.
- Add the macro `\color{blue}` to the line in the `*.bst` file that describes the format of the *annote* field.

You could also print the annotation in bold or italics.

## Support beyond text

Your annotated bibliography can be spiced up:
You can include lists, display math, computer code blocks, figures, and tables in the *annote* fields.


## Related projects of possible interest

- [LaTeX manuscript template](https://github.com/MooersLab/manuscriptInLaTeX/edit/main/README.md)
- [Writing log template](https://github.com/MooersLab/writingLogTemplate)
- [Slideshow Template](https://github.com/MooersLab/slideshowTemplateLaTeX)
- [Diary for 2022 in LaTeX](https://github.com/MooersLab/diary2022inLaTeX)
- [Diary for 2023 in LaTeX](https://github.com/MooersLab/diary2023inLaTeX)
- [latex-emacs profile](https://github.com/MooersLab/latex-emacs)
- [snippets for latex-mode in Emacs](https://github.com/MooersLab/snippet-latex-mode)
- [Quizzes about Emacs to improve recall of keybindings](https://github.com/MooersLab/qemacs)
- [Slides from talk about LaTeX in Emacs at the Berlin Emacs Meetup Aug 31, 2022](https://github.com/MooersLab/BerlinEmacsAugust2022)
- [Slides from talk about GhostText, Data Science Workshop, July 2022](https://github.com/MooersLab/DSW22ghosttext)
- [Video link to talk about GhostText, Data Science Workshop, July 2022](https://mediasite.ouhsc.edu/Mediasite/Channel/python/watch/4da0872f028c4255ae12935655e911321d)
- [The writer's law](https://github.com/MooersLab/thewriterslaw)

## Version History

|Version      | Changes                                               | Date            |
|:------------|:------------------------------------------------------|:----------------|
| Version 0.2 | Added Update table to README.md                       | 2024 April 7    |
| Version 0.3 | Edit the README.md heavily.                           | 2024 April 17   |
| Version 0.4 | Edit the README.md heavily.                           | 2024 October 8   |
| Version 0.5 | Edit the README.md heavily.                           | 2024 October 16   |

## Sources of Funding

- NIH: R01 CA242845
- NIH: R01 AI088011
- NIH: P30 CA225520 (PI: R. Mannel)
- NIH P20GM103640 and P30GM145423 (PI: A. West)


