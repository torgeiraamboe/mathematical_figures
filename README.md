
# Mathematical figures

Mathematical figures I have made, mostly in InkScape. 
Feel free to use anything you want as you please. 

Some of the files are meant to use with LaTeX, in particular they contain mathematical writing. 
You will see these by being encompassed by dollar signs, $...$.
These are used to let LaTeX compile the mathematical writing, in order to have it in the same style as the rest of the document.

### How to use the files containing TeX
 - Open the filename.svg file in Inkscape
 - In the "save as" document type menu, you will find an option to "save as pdf"
 - Choose this option and press save
 - A new popup will appear with some options
 - Make sure "Omit text in PDF and create LaTeX file" is checked off in the "Text output options" menu
 - You can play around with the other options as you like, but I would recommend to check off "Use exported object's size" in the "Output page size" menu

This procedure will create two files, filename.pdf file and filename.pdf_tex. These are now ready to be included in you TeX document. To do this, do the following
 - Make sure you have added the graphicx package to your preamble
 - Put both files in a folder in the root directory, called "inkscape_figures" or another name of you choice
 - Add this folder as a graphics path to your document by using the following code in your preamble: \graphicspath{{./inkscape_figures/}}
 - Include the files into you document, for example using the following code 

```
\begin{figure}
\centering
\def\svgwidth{0.5\textwidth}
\input{filename.pdf_tex}
\end{figure}
```
