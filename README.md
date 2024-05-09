# Quarto Book PDF template for university thesis

This is a template for a university thesis created with [Quarto Book](https://quarto.org/docs/books/), designed for output in PDF format.

## Installation

Before using the template, you should install Quarto. You can find the instructions [here](https://docs.posit.co/resources/install-quarto/).
You also need to have LaTeX installed on your machine.

## Layout

The font of the document is Times New Roman, size 12 and with 1.5 of spacing between lines.
The document starts with a custom LaTeX cover, followed by the abstract. Then, there are the table of contents, the list of figures, and list of tables. The next elements of the document are the introduction and all the chapters. The document ends with the references. Page numbering is in roman numerals until the end of the introduction, and switches to arabic numerals from the first chapter, starting from 1.

## Usage

After the installation, you can use the template and modify what you need.
The main file is `_quarto.yml`, from here, you can edit your preferences. By changing the following variables, they will also be reflected on the output front page:

```yaml
book:
  title: "Thesis title"
  subtitle: "Thesis subtitle"
  author:
    - name: "Name Surname"
      id: "010101"
      affiliations:
        - name: "University of ..."
          department: "Department of ..."
  date: "2024-01-01"
  output-file: "output_thesis"
```

This section contains all the files that compose the book. You can add or change files, but do not remove the `index.qmd` file, as it is necessary to generate the PDF. In this case, it is used as the introduction section of the thesis:

```yaml
  chapters:
    - index.qmd
    - chapter_1.qmd
    - chapter_2.qmd
    - chapter_3.qmd
    - references.qmd
```

These are the settings for the page margins:

```yaml
    geometry:
      - inner=3cm
      - outer=3cm
      - top=2.5cm
      - bottom=2.5cm
```

While these set the font, the size and the spacing:

```yaml
    linestretch: 1.5
    fontsize: 12pt
    mainfont: "Times New Roman"
```

You can write the abstract of the thesis directly here, and it will appear in the second page of the PDF:

```yaml
abstract: |
  Abstract here.
```

In the folder `_cover` you should replace the `logo.jpg` with the actual logo of your university.
The cover of the thesis is in the `before-body.tex` file. In this file you need to choose the type of degree, for example:

```latex
    \Large{MSc/BSc program\\
    in\\
    Economics\\}
```

Change the supervisor's name:

```latex
            \textbf{Supervisor} \\
            Ch. Prof. ...\\[.3cm]
```

Finally, change the academic year:

```latex
            \textbf{Academic Year}\\
            2023-2024
```

In these files, you will find other settings that can be changed based on your preferences and needs.

## License

[MIT](https://choosealicense.com/licenses/mit/)