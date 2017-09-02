# Markdown generation using bibtex

The first step is to [install pandoc](http://pandoc.org/installing.html).

To generate the markdown of the citations using the template `citation_template.md`:

    pandoc -s -S --bibliography gonzalez-fierro_complete_publications.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
    pandoc --from html --to markdown_github publications.html -o publications.md
