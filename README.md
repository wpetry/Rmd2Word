# Rmd2Word

## This repo contains:
1. a template for knitting Rmarkdown manuscript drafts to Microsoft Word to share with collaborators (`ms_style_template.docx`)
2. an Rmarkdown template for customizing your own document template (`ms_template.Rmd`)
3. supporting files to make #2 realistically display a bibliography (`example.bibtex`) and citation formatting (`journal-of-ecology.csl`)

## To use this template
1. Clone `ms_style_template.docx` into the working directory where your RMarkdown will be rendered.
2. Export the bibliography from your reference manager as choice. Here I've used BibTex, but other formats are supported (http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html).
3. Download the citation style for your journal of choice. Follow RStudio's advice for working with these:
>A primer on creating and modifying CSL styles can be found at http://citationstyles.org/downloads/primer.html.
>A repository of CSL styles can be found at https://github.com/citation-style-language/styles.
>See also http://zotero.org/styles for easy browsing.
4. Specify the output template, the bibliography, and the citation style files in the Rmarkdown YAML header
```
---
title: "My awesome discovery"
output:
  word_document:
    reference_docx: ms_style_template.docx
bibliography: example.bibtex
csl: journal-of-ecology.csl
---
```

## Resources
- RStudio's Rmarkdown [Bibliographies and Citations reference manual]( http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
- Richard Layton's ["Rmd to docx collaboration superpowers!"](http://www.graphdoctor.com/archives/867)

## License note
`journal-of-ecology.csl` was retrieved from Zotero as an example citation style. This work is licensed under a Creative Commons Attribution-ShareAlike 3.0 License (http://creativecommons.org/licenses/by-sa/3.0/).
