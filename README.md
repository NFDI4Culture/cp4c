# Computational Publishing for Archives

## Quarto - How To: Install, getting started, guide

### Install and getting started

<https://quarto.org/docs/get-started/>

They miss out that you need Python installed and Jupyter Lab and a working
terminal to install them

<https://www.python.org/downloads/>

<https://jupyter.org/install>

Also install Panda: py -m pip install panda

As well as knowing what the Python prompt and escape looks like:
<https://stackoverflow.com/questions/41524734/how-to-exit-python-script-in-command-prompt>

#### Docker Compose

This repository also contains Docker Compose and Dockerfiles for running the various applications in Docker containers.

Run `docker-compose up -d --build` to start the containers and `docker-compose down` to stop the containers.

The jupyterlab container runs a stand-alone version of JupyterLab on http://localhost:8888. This can be used to edit any Jupyter Notebook files in the repository. The JupyterLab instance runs with the password 'jupyterlab'.

The nginx container runs Nginx webserver and displays the static site that Quarto renders. This runs at http://localhost:1337.

The quarto container starts a Ubuntu 22.04 container, installs various things like Python, downloads Quarto and installs it, and then adds Python modules like jupyter, matplotlib, and panda. It then runs in the background so Quarto can be called on to render the qmd and ipynb files into the site/book like so:

`docker exec -it quarto quarto render` 

(There's an open issue with how this Docker setup works in a MacOS environment. The Docker setup works in Ubuntu but Quarto doesn't run properly when Docker is run in MacOS. Unclear why but there's an open discussion with the Quarto team at https://github.com/quarto-dev/quarto-cli/discussions/3308)

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
