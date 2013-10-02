# Dominatrix for Pandoc

An implemention of @kenlimmj's dominatrix latex sty for pandoc aka. I really liked what he was doing, so I hacked this abominable frankenstein out of his David.

## Quick Start

Throw `dominatrix_pandoc.latex` into the templates folder of pandoc. It should be located at 

`/usr/local/share/pandoc-1.11.1/data/templates`

Then, run pandoc using these arguments

`pandoc --standalone --latex-engine=xelatex --template dominatrix_pandoc.latex <input file probably markdown> -o <output file of whatever format you want. probably pdf or tex>`

If you're using SmartMarkdown for Sublime, then use these user-settings

```
{
    /* Please specify the PATH of pdflatex if you wanna generate PDF */
    "tex_path": ["/usr/local/texlive/2012/bin/x86_64-darwin"],
    /* Provide your arguments here as a list e.g.: ["--latex-engine=xelatex", "--toc"]
    arguments that are separated by space must be in separate slots. e.g. ["-H", "template.tex"] */
    "pandoc_args": ["--standalone"],
    "pandoc_args_pdf": ["--latex-engine=xelatex", "--template", "dominatrix_pandoc.latex"],
    "pandoc_args_html": [""],
    "pandoc_args_docx": []
}
```