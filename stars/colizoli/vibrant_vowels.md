---
project: vibrant_vowels
stars: 1
description: Change single letters (vowels) to specific colors in Word documents
url: https://github.com/colizoli/vibrant_vowels
---

vibrant\_vowels
===============

Change single letters (vowels) to specific colors in Microsoft Word documents (DOCX).
-------------------------------------------------------------------------------------

This script will loop through individual letters and reformat each occurrence of a letter with a specific color (RGB);  
If 'change\_font' is True, the script will replace the entire document's font typeface and font size. The reformatted document is saved as a new document. Fonts need to be already installed on the computer.

Books are found in the directory: os.path.join(os.getcwd(), 'books'). The name of book input at the prompt should exclude the 'docx' file extension: "books/{}.docx".format(book\_name). The new colored version will be saved as: "books/{}\_vibrant\_vowels.docx".format(book\_name).

Letters and colors to be changed are imported from a CSV file in the directory: os.path.join(os.getcwd(), 'colors'). The CSV file with colors needs to have the following columns: 'letter', 'r', 'g', 'b'. Letters are case-sensitive.

The following packages need to be installed: python-docx, pandas, numpy

> > pip install python-docx pandas numpy

To run:

> > python color\_text\_vibrant\_vowels.py

You will be prompted with the book name and whether you want to change the font type and size.

Character formatting is applied at the docx.text.run.Run level. The script can be adjusted to change the font typeface, size, bold, italic, and underline of single letters or the whole document. A Run object has a read-only font property providing access to a Font object. A run's Font object (docx.text.run.Run.font) provides properties for getting and setting the character formatting for that run. E.g. current\_run.font.color.rgb = RGBColor(r, g, b)

The function for isolating individual letters as runs, isolate\_run(), was taken from here: See: python-openxml/python-docx#980

Debugged on Python 3.9. Not optimized for efficiency or speed, but it works.