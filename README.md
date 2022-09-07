# Annotated bibliography template in LaTeX for specific writing projects

These files support the automated generation of the an annotated bibliography in LaTeX.
The AnnoBib.tex file is the master file.
It uses the annote field in the bibtex entry in cited.bib and the plain-annote.bst file.
To write out the cited bib entries from global.bib, use the command line program **bibtool** with the main.tex file's corresponding main.aux file:

```bash
bibtool -x main.aux -o AnnoBibMyBDA.bib
```
Bibtool is distributed with LaTeX.

Manually add annote fields to the AnnoBibMyBDA.bib file and enter your annotations there if you have not done so already.
Or, if you are more disciplined, you can add the annote fields in global.bib and repeat the extraction of the cited entries when you are finished.
All of the entries in cited.bib will be used to make the annotated bibliography regardless of the presence or absence of the annote field.

I store these files in a *annotatedBibliography* subfolder in my writing projects folder.
These file work fine on Overleaf.

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
