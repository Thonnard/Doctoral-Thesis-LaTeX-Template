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
4. Change TeXStudio settings
   * Go to Options > Configure TeXstudio > Build
   * Click "Advanced"
   * Change Default compiler to: txs:///pdflatex | txs:///makeglossaries | txs:///biber --output-safechars | txs:///pdflatex | txs:///pdflatex
5. Optional: Add an extra CWL file for autocompletion (to avoid red highlighting of unrecognized commands)
   * Download the CWL file here: https://raw.githubusercontent.com/Thonnard/Doctoral-Thesis-LaTeX-Template/master/CWL/mylist.cwl
   * Copy CWL file to  C:\Users\your_username\AppData\Roaming\texstudio\completion\user
   * Go to Options > Configure TeXstudio > Completion 
   * Check the mylist.cwl box
   
## Using the template

## Features

## LaTeX documentation

## Examples


