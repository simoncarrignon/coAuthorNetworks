# Co-authorship analysis tool

This software is made to help analyse the literature of research
projects. Which papers share authors, which authors publish together?
Wjat are the timelines? etc.


Robustness goes over precision. The analysis should work with any
given bibtex-file that has minimal information.  The cleaner
the bibtex-file (duplicates, name spellings, ...) the better the
output, i.e. more precise. It is not intended for scientific
analysis of text corpora.

It's a fork from  Simon Carrignon's original lines of code that can be
found [here](https://framagit.org/sc/pybibnet). Simon is also [on Github](https://github.com/simoncarrignon).

## Prerequisites

The software is developed and used with `python3`. It makes use of the
package
[`bibtexparser`](https://github.com/sciunto-org/python-bibtexparser),
which can be installed typing:

    pip install bibtexparser

## Usage

```bash
./main.py BIBTEXFILENAME
```

It expects a bibtex-file at `FILENAME`. The output consists of four
files:

  * `FILENAME.authorlist.csv`
  * `FILENAME.authorNetwork.csv` - network of authors who share a publication
  * `FILENAME.paperlist.csv`
  * `FILENAME.paperNetwork.csv` - network of publications which share an author

Visualization of the networks is not (yet)
implemented. [Gephi](https://gephi.org/) does a pretty good job doing
that.


A bibtex example is available in `example/`. The two graphs were done with [Gephi](https://gephi.org/).

![Co-author network of phd.bib](example/phdAuthorNET.png)
![Co-paper network of phd.bib](example/phdPaperNET.png)


## Warranty

There is none. The software might or might not work for you or even
have unexpected effects like data loss or much worse. I don't know,
but did used it and would say it's rather safe to run. Always have a
backup!

## Authors

  * Niko Komin ([on Laikaundfreunde](http://www.laikaundfreunde.de/niko-komin))
  * Simon Carrignon ([on Framagit](https://framagit.org/sc), [on Github](https://github.com/simoncarrignon), [on Twitter](https://twitter.com/SimonCarrignon/).


## License


<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
