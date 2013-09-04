Full-Circle-Magazine-Series
===========================

* Author: Laszlo Szathmary (jabba.laci@gmail.com)
* Last update: 2013-09-04 (yyyy-mm-dd)
* Home page: <https://ubuntuincident.wordpress.com/2011/02/21/python-tutorials-of-full-circle-magazine-in-a-single-pdf/>
* GitHub: <https://github.com/jabbalaci/Full-Circle-Magazine-Series>

Full Circle Magazine (FCM) started a Python tutorial series in issue #27. 
It would be nice to extract these tutorials from the issues and put them 
together in a single PDF. Thus, we would have all the tutorials together 
in one document.

Usage:
------

`./01-get-issues.sh`

Download the necessary FCM issues. Issue #28 has a different name,
the script will rename it.
    
`./01b-get-latest-issue.sh`

It'll only download the latest issue.

`./02-extract.py python.csv`

The file `python.csv` specifies which pages to extract from the issues.
You can write your own `series.csv` file (ex.: `gimp.csv`) to extract
a different series.

`./03-combine-pieces.py python.csv`

Combine the pieces together in a single PDF. Location of the result:
`python/result/all.pdf`. If you combine the pieces with Adobe Acrobat Pro, 
the size of the resulting file will be very small. `Pdftk` produces a much 
larger file.

`ebook_edition/fetch.py`

Fetch e-book edition issues in `.epub` format.
