# Minimalistic doctoral thesis LaTeX template
KU Leuven Faculty of Psychology and Educational Sciences doctoral thesis LaTeX template

## LaTeX installation 
### Windows 10
1. Install MiKTeX (or any other TeX/LaTeX typesetting system)
    * Download the latest version here: https://miktex.org/download
    * Install and check for updates (open MiKTeX console and navigate to Updates)
    * Go to Settings (in MikTeX console) and select the "Always install missing packages on-the-fly" option
2. Install TeXstudio (or any other writing environment)
   * Download the latest version here: https://www.texstudio.org/
3. Install Active Perl (required by glossaries package)
   * Download the latest version here: https://www.activestate.com/activeperl/downloads
   * After installation, navigate to your MiKTeX installation folder (e.g. C:\Program Files\MiKTeX 2.9\miktex\bin\x64) and run perltex.exe
4. Change TeXstudio settings
   * Go to Options > Configure TeXstudio > Build
   * Click "Advanced"
   * Change Default compiler to: txs:///pdflatex | txs:///makeglossaries | txs:///biber --output-safechars | txs:///pdflatex | txs:///pdflatex
5. Optional: add an extra CWL file for autocompletion (to avoid red highlighting of unrecognized commands)
   * Download the CWL file here: https://raw.githubusercontent.com/Thonnard/Doctoral-Thesis-LaTeX-Template/master/CWL/mylist.cwl
   * Copy CWL file to  C:\Users\your_username\AppData\Roaming\texstudio\completion\user
   * Go to Options > Configure TeXstudio > Completion 
   * Check the mylist.cwl box
   
### Linux (Ubuntu/Mint)
1. Install TeX Live (or any other TeX/LaTeX typesetting system)
   * ```sudo apt-get install texlive-full```
2. Install TeXstudio
   * ```sudo apt-get install texstudio```
4. Change TeXstudio settings
   * Go to Options > Configure TeXstudio > Build
   * Click "Advanced"
   * Change Default compiler to: txs:///pdflatex | txs:///makeglossaries | txs:///biber --output-safechars | txs:///pdflatex | txs:///pdflatex
5. Optional: add an extra CWL file for autocompletion (to avoid red highlighting of unrecognized commands)
   * Download the CWL file here: https://raw.githubusercontent.com/Thonnard/Doctoral-Thesis-LaTeX-Template/master/CWL/mylist.cwl
   * Copy CWL file to texstudio config folder ```cp mylist.cwl ~/.config/texstudio/completion/user/```
   * Go to Options > Configure TeXstudio > Completion 
   * Check the mylist.cwl box
   

## Using the template
   * Open "main_book.tex" or "main_A4.tex" in TeXstudio
   * Adjust variables in the preamble (e.g. margins ("left", "right", ...), bindingoffset; cf. Warnings below) if necessary.
   * Font size can be set by changing \documentclass[a4paper,twoside,11pt]{book} in the preamble.
   * Line spacing (interline) can be set with the \setstretch{} command.
   * The title page can be adjusted by changing the "TitlePageBook.tex" or "TitlePageA4.tex" file.
   * Add/remove chapters in the mainmatter section (e.g. \include{./TeX_files/chapter33}.
   * Add/remove bibliography bib files in the bibliography section (e.g. \addbibresource{./Bibliography/chap33.bib}.
   * Add content to the chapter tex files (e.g. chapter01.tex) to write your chapters (cf. examples in the template).
   * Compile your document by clicking "Build and View" in the "Tools" menu (or press F5).

Additional information is written as comments in the main_book or main_A4 tex file. 
Examples for using acronyms, references, tables and figures are provided in the template.

## Changing the chapter style
The chapter style can be changed in several ways (e.g. https://texblog.org/2012/07/03/fancy-latex-chapter-styles/). Below you can find a straightforward example. Adding following code to the preamble will replace the standard chapter style with the ChapterNumber | LongTitle format. 

```
% change chapter style
\usepackage[T1]{fontenc}
\usepackage{titlesec, blindtext, color}
\definecolor{gray75}{gray}{0.75}
\newcommand{\hsp}{\hspace{20pt}}
\titleformat{\chapter}[hang]{\Huge\bfseries}{\thechapter\hsp\textcolor{gray75}{|}\hsp}{0pt}{\Huge\bfseries}
```

## Features
 * Citations need to be in bibtex format and can be imported from Mendeley, Zotero,...
 * Citations from a Word document can be converted to bibtex with this macro: http://git.macropus.org/citation-finder/.
 * Reference lists are created automatically per chapter.
 * Glossary (acronyms) is created autmatically: you can remove numbering by adding the nonumberlist option in the main_book.tex or main_A4.tex file. 
 ```\usepackage[toc,acronym,nomain,nonumberlist]{glossaries}```
 * Table of content, list of figures and list of tables are created automatically.

## Warnings
 * The size of graphics and figures can be set dynamically (e.g. \includegraphics[width=\textwidth]{einstein}) instead of static (e.g. \includegraphics[width=4cm]{einstein}) but final results should be double-checked when switching between A4 and book format.
 * Binding offset is set to 0.5cm for book documents. Check with your publisher for optimal settings! This can be changed in the preamble of main_book.tex with the option bindingoffset.
 * Binding offset is set to 0cm for A4 documents. This can be changed in the preamble of main_A4.tex with the option bindingoffset.

## LaTeX documentation
 * https://www.latex-project.org/help/documentation/
 * https://www.overleaf.com/learn
 * https://en.wikibooks.org/wiki/LaTeX
 * https://ctan.org/
 * https://www.latex-tutorial.com/quick-start/

## Examples
### Title page
<img src=/Output/main_bookjpg_Page1.jpg width="300" title="Github Logo"></img>
### Table of content
<img src=/Output/main_book_Page15.jpg width="300" title="Github Logo"></img>
### Chapter styles
<img src=/Output/main_book_Page19.jpg width="300" title="Github Logo"></img>
<img src=/Output/main_book_style2jpg_Page19.jpg width="300" title="Github Logo"></img>

