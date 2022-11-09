# Computational Publishing for Archives

## Quarto - How To: Install, getting started, guide

### Install and getting started

<https://quarto.org/docs/get-started/>

They miss out that you need Python installed and Jupyter Lab and a working
terminal to install them

<https://www.python.org/downloads/>

<https://jupyter.org/install>

As well as knowing what the Python prompt and escape looks like:
<https://stackoverflow.com/questions/41524734/how-to-exit-python-script-in-command-prompt>

## Create a book

<https://quarto.org/docs/books/>

1. I've used the book section with Terminal Win 10
<https://quarto.org/docs/books>

1.  Published book to GitHub pages using the Docs route
    <https://quarto.org/docs/publishing/github-pages.html#render-to-docs>

2.  YAML \_quarto.yml was modified to outpt-dir: docs

3.  GitHub pages render from /docs

4.  Download locally and in the terminal at top level of repo run *quarto
    preview* to locally view at localhost:7104 and to output run *quarto render*

5.  **Haven't figured out yet how to add a notebook to a book and have it render
    mult-format to the book? First I was just getting the book to run.**
