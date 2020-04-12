# Avaamo Tutorial

Tutorial on building agents on the Avaamo conversational AI platform

## Description

This respository uses [Pandoc](http://pandoc.org/) for the books creation. 
Pandoc is a suite of tools to compile markdown files into readable files (PDF, EPUB, HTML...).

## Usage

### Installing

Please, check [this page](http://pandoc.org/installing.html) for more information. On ubuntu, it
can be installed as the *pandoc* package:

```sh
sudo apt-get install pandoc
```

This template uses [make](https://www.gnu.org/software/make/) to build the output files, so don't
forget to install it too:

```sh
sudo apt-get install make
```

To export to PDF files, make sure to install the following packages:

```sh
sudo apt-get install texlive-fonts-recommended texlive-xetex
```

### Folder structure

Here's a folder structure for a Pandoc book:

```
my-book/         # Root directory.
|- build/        # Folder used to store builded (output) files.
|- chapters/     # Markdowns files; one for each chapter.
|- images/       # Images folder.
|  |- cover.png  # Cover page for epub.
|- metadata.yml  # Metadata content (title, author...).
|- Makefile      # Makefile used for building our books.
```

### Setup generic data

Edit the *metadata.yml* file to set configuration data (note that it must start and end with `---`):

```yml
---
title: My book title
author: Daniel Herzog
rights: MIT License
lang: en-US
tags: [pandoc, book, my-book, etc]
abstract: |
  Your summary.
mainfont: DejaVu Sans

# Filter preferences:
# - pandoc-crossref
linkReferences: true
---
```

You can find the list of all available keys on
[this page](http://pandoc.org/MANUAL.html#extension-yaml_metadata_block).

### Creating chapters

Creating a new chapter is as simple as creating a new markdown file in the *chapters/* folder;
you'll end up with something like this:

```
chapters/01-introduction.md
chapters/02-installation.md
chapters/03-usage.md
chapters/04-references.md
```

Pandoc and Make will join them automatically ordered by name; that's why the numeric prefixes are
being used.

All you need to specify for each chapter at least one title:

```md
# Introduction

This is the first paragraph of the introduction chapter.

## First

This is the first subsection.

## Second

This is the second subsection.
```

Each title (*#*) will represent a chapter, while each subtitle (*##*) will represent a chapter's
section. You can use as many levels of sections as markdown supports.

#### Manual control over page ordering

You may prefer to have manual control over page ordering instead of using numeric prefixes.

To do so, replace `CHAPTERS = chapters/*.md` in the Makefile with your own order. For example:

```
CHAPTERS += $(addprefix ./chapters/,\
 01-introduction.md\
 02-installation.md\
 03-usage.md\
 04-references.md\
)
```

#### Links between chapters

Anchor links can be used to link chapters within the book:

```md
// chapters/01-introduction.md
# Introduction

For more information, check the [Usage] chapter.

// chapters/02-installation.md
# Usage

...
```

If you want to rename the reference, use this syntax:

```md
For more information, check [this](#usage) chapter.
```

Anchor names should be downcased, and spaces, colons, semicolons... should be replaced with hyphens.
Instead of `Chapter title: A new era`, you have: `#chapter-title-a-new-era`.

#### Links between sections

It's the same as anchor links:

```md
# Introduction

## First

For more information, check the [Second] section.

## Second

...
```

Or, with al alternative name:

```md
For more information, check [this](#second) section.
```

### Inserting objects

Text. That's cool. What about images and tables?

#### Insert an image

Use Markdown syntax to insert an image with a caption:

```md
![A cool seagull.](images/seagull.png)
```

Pandoc will automatically convert the image into a figure, using the title (the text between the
brackets) as a caption.

If you want to resize the image, you may use this syntax, available since Pandoc 1.16:

```md
![A cool seagull.](images/seagull.png){ width=50% height=50% }
```

#### Insert a table

Use markdown table, and use the `Table: <Your table description>` syntax to add a caption:

```md
| Index | Name |
| ----- | ---- |
| 0     | AAA  |
| 1     | BBB  |
| ...   | ...  |

Table: This is an example table.
```

#### Insert an equation

Wrap a LaTeX math equation between `$` delimiters for inline (tiny) formulas:

```md
This, $\mu = \sum_{i=0}^{N} \frac{x_i}{N}$, the mean equation, ...
```

Pandoc will transform them automatically into images using online services.

If you want to center the equation instead of inlining it, use double `$$` delimiters:

```md
$$\mu = \sum_{i=0}^{N} \frac{x_i}{N}$$
```

[Here](https://www.codecogs.com/latex/eqneditor.php)'s an online equation editor.

#### Cross references

Originally, this template used LaTeX labels for auto numbering on images, tables, equations or
sections, like this:

```md
Please, admire the gloriousnes of Figure \ref{seagull_image}.

![A cool seagull.\label{seagull_image}](images/seagull.png)
```

**However, these references only works when exporting to a LaTeX-based format (i.e. PDF, LaTeX).**

In case you need cross references support on other formats, this template now support cross
references using [Pandoc filters](https://pandoc.org/filters.html). If you want to use them, use a
valid plugin and with its own syntax.

Using [pandoc-crossref](https://github.com/lierdakil/pandoc-crossref) is highly recommended, but
there are other alternatives which use a similar syntax, like
[pandoc-xnos](https://github.com/tomduck/pandoc-xnos).

First, enable the filter on the *Makefile* by updating the `FILTER_ARGS` variable with your new
filter(s):

```make
FILTER_ARGS = --filter pandoc-crossref
```

Then, you may use the filter cross references. For example, *pandoc-crossref*  uses
`{#<type>:<id>}` for definitions and `@<type>:id` for referencing. Some examples:

```md
List of references:

- Check @fig:seagull.
- Check @tbl:table.
- Check @eq:equation.

List of elements to reference:

![A cool seagull](images/seagull.png){#fig:seagull}

$$ y = mx + b $$ {#eq:equation}

| Index | Name |
| ----- | ---- |
| 0     | AAA  |
| 1     | BBB  |
| ...   | ...  |

Table: This is an example table. {#tbl:table}
```

Check the desired filter settings and usage for more information
([pandoc-crossref usage](http://lierdakil.github.io/pandoc-crossref/)).

### Output

This template uses *Makefile* to automatize the building process. Instead of using the *pandoc cli
util*, we're going to use some *make* commands.

#### Export to PDF

Please note that PDF file generation requires some extra dependencies (~ 800 MB):

```sh
sudo apt-get install texlive-xetex ttf-dejavu
```

After installing the dependencies, use this command:

```sh
make pdf
```

The generated file will be placed in *build/pdf*.

#### Export to EPUB

Use this command:

```sh
make epub
```

The generated file will be placed in *build/epub*.

#### Export to HTML

Use this command:

```sh
make html
```

The generated file(s) will be placed in *build/html*.

#### Export to DOCX

Use this command:

```sh
make docx
```

The generated file(s) will be placed in *build/docx*.

#### Extra configuration

If you want to configure the output, you'll probably have to look the
[Pandoc Manual](http://pandoc.org/MANUAL.html) for further information about pdf (LaTeX) generation,
custom styles, etc, and modify the Makefile file accordingly.

## References

- [Pandoc](http://pandoc.org/)
- [Pandoc Manual](http://pandoc.org/MANUAL.html)
- [Wikipedia: Markdown](http://wikipedia.org/wiki/Markdown)

## Contributors

This project has been developed by:

| Avatar | Name | Nickname | Email |
| ------ | ---- | -------- | ----- |
| ![](http://www.gravatar.com/avatar/2ae6d81e0605177ba9e17b19f54e6b6c.jpg?s=64)  | Daniel Herzog | Wikiti | [info@danielherzog.es](mailto:info@danielherzog.es)
