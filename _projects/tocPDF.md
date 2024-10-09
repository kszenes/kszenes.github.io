---
layout: page
title: tocPDF
description: Automatic CLI tool for generating an outline of PDFs based on the its table of contents. 
img:
importance: 4
category: Fun
---

# Introduction
Imagine this: you just became fascinated by some new topic in quantum physics, say, for instance, perturbation theory, and you found that the reference textbook that everyone recommends can be luckily downloaded as a free PDF from the internet. Excited to start your journey in this field, you open the PDF and find a nicely structured table of contents (TOC) with all the relevant subjects having their own dedicated section. Having found the section that you want to start reading with, you are eager to jump to it. But wait! For some reason, the outline that comes with the PDF is empty and, therefore, you need to manually navigate to page using the page number from the TOC. Even worse, since the PDF contains a Preface chapter, the page numbering of the book only starts on the PDF page 27 and, therefore, you cannot simply use the PDF page to jump the desired section. Instead, you need to add an offset to the PDF page which makes navigating the PDF even less convenient.

# Solution
Not to worry, I wrote a Python command line tool `tocPDF` to solve precisely this issue. It extracts the TOC found in the PDF and populates the outline of the PDF with it.

{% include video.liquid path="assets/video/projects/tocPDF-example-video.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true muted=true loop=true %}

## Installation
The project is hosted on [GitHub](github.com/kszenes/tocPDF) and can be installed using `pip`:
```sh
pip install tocPDF
```
## Usage
`tocPDF` requires the PDF page number corresponding to the start and end of the TOC as well as the offset to the first page of the book (the first one numbered with an Arabic numeral). 
```sh
tocPDF --start 3 --end 6 --offset 9 example.pdf
tocPDF -s 3 -e 6 -o 9 example.pdf
```
For certain PDFs, this offset is not constant for the entire document due to additional unnumbered or missing pages. This is particularly common between different parts of a textbook where a blank unnumbered page is often added. In these cases, using naively the original offset without taking into account this additional shift would lead to a mismatch between the page number in the outline and the true page number of the section. `tocPDF` addresses this issue by verifying that the offset for each section is still accurate. This is done by ensuring that the expected page number of a section matches the one parsed from the PDF. This feature can be enabled by passing the `-m/--missing_pages` flag:
```sh
tocPDF -s 3 -e 6 -o 9 -m example.pdf
```
Note that this additional verification will slow down the generation of the outline.
## TOC Extraction
`tocPDF` works with a number of backends for extraction of the TOC from the PDF:
- [pdfplumber](https://github.com/jsvine/pdfplumber) (default)
- [pypdf](https://github.com/py-pdf/pypdf)
- [tika](https://github.com/chrismattmann/tika-python) (requires Java)

These can be selected using the `-p/--parser` flag:
```sh
tocPDF -s 3 -e 6 -o 9 -m -p pypdf example.pdf
```
Certain parsers might perform better on certain PDF TOC formats. Therefore, if you are not happy with the results, make sure to experiment with the different parsers.
