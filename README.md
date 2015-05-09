# LaTeX-fussycite

The purpose of this package is for eliminating redundant information from repeatedly cited sources according to my own, finnicky conventions!

## What are these fussy conventions you speak of?
The two major rules are

1] Don't repeat yourself, and
2] always display enough citation information given the context.

Repeated citation of the same source doesn't require that *all* information always be rendered. However, it is still very useful to have the same citation information included in the content, because while writing, content will frequently be moving around and citations frequently added and removed. Doing this manually is a pain, and  there is an important additional requirement. In short, if you are citing the same source in a row, there is no reason to repeatedly include the author (and/or year) of the source, so the included functions include an intelligent way to automate decisions of when you just need to render the page for a citation.

Additionally, a new page is a new context in which you might not know who was last cited. In LaTeX especially, you can't (from the content alone) determine where on a page any given citation will land. As a result, these functions reset on a new page and provide the full information desired. The functions included provide as much information as you would like if they are the first entry on a new page, and this choice is reflected in the three functions \citeau{} (Includes the author in the first citation on a new page), \citeyr{} (Includes the year in the first citation on a new page), and \citeauyr{} (Includes the author and year...).

The choice between these is best left up to the author, as appropriateness depends on context, especially the degree to which you are jumping between different sources.

NB: In my thesis, I ended up primarily using \citeyr{} and \citeauyr{}. I have left \citeau{} in this package in case anyone else has a use for this.

## How do I install this?

### On Linux, Windows or Mac
Place fussycite.sty in your "texmf-local/tex" directory

### On Mac (a better option)
Place fussycite.sty in ~/Library/texmf/tex/

## How do I use this?
This package includes four citation functions:
* \citedewey{work, page} (I cite the Collected Works of John Dewey *a lot*)
* \citeau{author, year, page}
* \citeyr{author, year, page}
* \citeauyr{author, year, page}

NB: This system includes a hack into the indexing system in order to detect whether a given citation is on a different page than the previous one. As a result, you'll have to compile the document twice for all of these numbers to be properly determined. (You're probably already doing this if you have a table of contents.)

## Known issues
This code might not work with a document that also uses an index. If you want to use this AND an index, and are having trouble, let me know and we can try to sort this out.

## Other conventions
These functions (with the exception of \citedewey{}) integrate with BibTex databases by generating \nocite entries. However, the system is opinionated. The convention of label references in BibTeX is {AUTHOR}-{YEAR}{optional letter}

## Licence
This program can be redistributed and/or modified under the terms of the LaTeX Project Public License Distributed from CTAN archives in directory macros/latex/base/lppl.txt.
