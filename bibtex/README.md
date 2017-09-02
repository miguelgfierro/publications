# Markdown generation using bibtex

The first step is to [install pandoc](http://pandoc.org/installing.html).

To generate the markdown of the citations I use the template `citation_template.md` and a csl file. To generate the citation for the conferences:

    pandoc -s -S --bibliography gonzalez-fierro_conferences.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
    pandoc --from html --to markdown_github publications.html -o publications.md

To generate the citation for the journals:

    pandoc -s -S --bibliography gonzalez-fierro_journals.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
    pandoc --from html --to markdown_github publications.html -o publications.md

To generate the citation for the thesis:

    pandoc -s -S --bibliography gonzalez-fierro2014thesis.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
    pandoc --from html --to markdown_github publications.html -o publications.md


