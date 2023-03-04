# Markdown generation using BibTeX

This guide explains how to transform a BibTeX file into markdown using a style file.

## Requirements

We are going to need pandoc to transform between formats, a BibTeX file with the information of the publications and [citation style language file](http://citationstyles.org/). 

The first step is to [install pandoc](http://pandoc.org/installing.html). The version I used is 1.19.2.1. The installation files for Linux, Mac and Windows can be found [here](https://github.com/jgm/pandoc/releases/tag/1.19.2.1).

You need your citations in BibTeX format. [Here](gonzalez-fierro2014thesis.bib) you have an example.

Finally, you need a csl file. In [this repo](https://github.com/citation-style-language/styles) you will find a huge number of formats. In my case, I used a modification of the IEEE style: `ieee-with-url-mod.csl`.

## File generation

To generate the markdown of the citations I use the template `citation_template.md` and a csl file. To generate the citation for the conferences:

```bash
pandoc -s -S --bibliography gonzalez-fierro_conferences.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
pandoc --from html --to markdown_github publications.html -o publications.md
```

To generate the citation for the journals:

```bash
pandoc -s -S --bibliography gonzalez-fierro_journals.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
pandoc --from html --to markdown_github publications.html -o publications.md
```

To generate the citation for the thesis:

```bash
pandoc -s -S --bibliography gonzalez-fierro_thesis.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
pandoc --from html --to markdown_github publications.html -o publications.md
```

To generate the citation for the patents:

```bash
pandoc -s -S --bibliography gonzalez-fierro_patents.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
pandoc --from html --to markdown_github publications.html -o publications.md
```

To generate the citation for the books:

```bash
pandoc -s -S --bibliography gonzalez-fierro_books.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
pandoc --from html --to markdown_github publications.html -o publications.md
```

To generate the citation for the blog posts:

```bash
pandoc -s -S --bibliography gonzalez-fierro_posts.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
pandoc --from html --to markdown_github publications.html -o publications.md
```

To generate the citation for the interviews:

```bash
pandoc -s -S --bibliography gonzalez-fierro_interviews.bib --filter pandoc-citeproc citation_template.md --csl ieee-with-url-mod.csl -o publications.html
pandoc --from html --to markdown_github publications.html -o publications.md
```
