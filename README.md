# Annotated bibliography template in LaTeX for specific writing projects

These files support the automated generation of the an annotated bibliography in LaTeX.
The AnnoBib.tex file is the master file.
It uses the annote field in the bibtex entry in cited.bib and the plain-annote.bst file.
To write out the cited bib entries from global.bib, use the command line program **bibtool** with the main.tex file's corresponding main.aux file:

```bash
bibtool -x main.aux -o cited.bib
```
Bibtool is distributed with LaTeX.

Manually add annote fields to the cited.bib file and enter your annotations there if you have not done so already.
Or, if you are more disciplined, you can add the annote fields in global.bib and repeat the extraction of the cited entries when you are finished.
All of the entries in cited.bib will be used to make the annotated bibliography regardless of the presence or absence of the annote field.

I store these files in a \url{annotatedBibliography} subfolder in my writing projects folder.
These file work fine on Overleaf.
