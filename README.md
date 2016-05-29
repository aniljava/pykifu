# pykifu
Python Script to convert SGF games with commentary to PDF/Postscript 


# About
An ad-hoc script to convert the sgf game into multipage pdfs. Was created with kindle ebook reader in mind. But can be used for printing and other usage.

Raw postscript is generated (Basically lines, stones and texts at appropriate coordinates). The generated postscript needs to be converted to pdf using `ps2pdf`

# Usage
`./pykifu <input-sgf-file.sgf> | ps2pdf - <output-pdf-file.pdf>`

# Samples
- Sample pdf [Lee Sedol vs AlphaGo https://github.com/aniljava/pykifu/releases/download/1.0/sample-lee-sedol-vs-alphago-game-1.pdf]
- https://github.com/aniljava/pykifu/releases has all other pdfs and sgfs from www.gogameguru.com untill 05-28-2016

# FEATURES
- Currently Splits moves based on the comments.
- If comments are not found, splits moves by next stone distance (upto 10 moves) or every 5 moves
- Tested against all the game records at gogameguru.com. Works goods with the comment convention used.
- Recognizes Alfa, Numeric, TR labels
- Captured stones are removed on normal page, and shown in last page with index.


# TODO / LIMITATIONS
- Allow command line options to change configurations like splitting, comments
- Add support for variations
- Split if comments does not properly splits the game
- Support other markers like square


# Dependencies
- gomill 
  - https://github.com/mattheww/gomill/
  - `pip install gomill`
- mako
  - http://www.makotemplates.org/
  - `pip install mako`


License
-------

All games records (pdf, sgf) with commentries are copyrighted work of YOUNGGIL AN at www.gogameguru.com, licensed under Creative Commons CC BY-NC-SA 4.0.

The script is licensed under Apache License. Please check the official page of License for details.


