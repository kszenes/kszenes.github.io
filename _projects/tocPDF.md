---
layout: page
title: tocPDF
description: Automatic CLI tool for generating an outline of PDFs based on the table of contents. 
img:
importance: 4
category: fun
---

# Problem statement
Imagine this: you just became fascinated by some new topic in mathematics, say for instance, algebraic topology and you found that the reference textbook that everyone recommends can be downloaded as a PDF from the internet for free. Excited to start you journey in this field you open the PDF and find a nicely structured table of contents (TOC) with all the relevant subjects having there own section. Having found from where you want to start reading, you are eager to jump to that section. But wait! For some reason, the outline that comes with the PDF is empty and therefore you need to manually navigate to the sections of interest and back. Even worse, since the PDF contains a Preface chapter which means that the page numbering only starts on the PDF page 42, you cannot simply use the PDF page to jump to the section. Instead, you need to add an offset to the PDF page which makes this setup even less convenient.

# The solution
Not to worry, the `tocPDF` Python tool extracts the table of contents and populates the outline of the PDF with it. In order to achieve this it requires the page corresponding to the start and end of the TOC as well as the offset to the first page numbered with an Arabic numeral. 
```sh
tocPDF --start 3 --end 6 --offset 9 example.pdf
tocPDF -s 3 -e 6 -o 9 example.pdf
```
For certain PDFs, this offset is not constant due to pages missing (particularly between different parts of the book). `tocPDF` can verify that the offset is still accurate by verifying the expected page number matches the one parsed from the PDF. This can be enabled by passing the `-m/--missing_pages` flag:
```sh
tocPDF -s 3 -e 6 -o 9 -m example.pdf
```
Note that this additional verification will slow down the generation of the outline.
## TOC Extraction
`tocPDF` relies on a number of external tools for performing the extraction of the TOC from the PDF:
- [pdfplumber](https://github.com/jsvine/pdfplumber) (default)
- [pypdf](https://github.com/py-pdf/pypdf)
- [tika](https://github.com/chrismattmann/tika-python) (requires Java)

These can be selected using the `-p/--parser` flag:
```sh
tocPDF -s 3 -e 6 -o 9 -m -p pypdf example.pdf
```
Certain parsers might perform better on certain PDFs. Therefore, if you are not happy with the results, make sure to try running `tocPDF` with a different parser. 
