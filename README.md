# Doctoral Thesis LaTeX Template
KU Leuven Faculty of Psychology and Educational Sciences doctoral thesis LaTeX template

## LaTeX installation (Windows)
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
   
## Using the template

## Changing the chapter style
Chapter style can be changed in several ways (e.g. https://texblog.org/2012/07/03/fancy-latex-chapter-styles/). Below you can find an straight forward example. Adding following code to the preamble will replace the standard chapter style with the ChapterNumber | LongTitle format. 

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
 * Glossaries (acronyms): remove numbering by adding the nonumberlist option \usepackage[toc,acronym,nomain,nonumberlist]{glossaries} in the main_book.tex or main_A4.tex file. 

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


