![Version](https://img.shields.io/github/v/release/DCMLab/mendelssohn_quartets?display_name=tag)
[![DOI](https://zenodo.org/badge/388173249.svg)](https://doi.org/10.5281/zenodo.14996150)
![GitHub repo size](https://img.shields.io/github/repo-size/DCMLab/mendelssohn_quartets)
![License](https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-9cf)


This is a README file for a data repository originating from the [DCML corpus initiative](https://github.com/DCMLab/dcml_corpora)
and serves as welcome page for both 

* the GitHub repo [https://github.com/DCMLab/mendelssohn_quartets](https://github.com/DCMLab/mendelssohn_quartets) and the corresponding
* documentation page [https://dcmlab.github.io/mendelssohn_quartets](https://dcmlab.github.io/mendelssohn_quartets)

For information on how to obtain and use the dataset, please refer to [this documentation page](https://dcmlab.github.io/mendelssohn_quartets/introduction).

When you use (parts of) this dataset in your work, please read and cite the accompanying data report:

_Hentschel, J., Rammos, Y., Neuwirth, M., & Rohrmeier, M. (2025). A corpus and a modular infrastructure for the 
empirical study of (an)notated music. Scientific Data, 12(1), 685. https://doi.org/10.1038/s41597-025-04976-z_

# Felix Mendelssohn – String Quartets (A corpus of annotated scores)

This corpus of annotated [MuseScore](https://musescore.org) files has been created within
the [DCML corpus initiative](https://github.com/DCMLab/dcml_corpora) and employs
the [DCML harmony annotation standard](https://github.com/DCMLab/standards). 
It represents the five string quartets published during Felix Mendelssohn's lifetime, plus the posthumous Op. 80. 
These works span the prodigious composer's entire adult career from age 18 until his untimely death at age 38. 
These are among the composer's most intensely personal works, and particularly so the memorials to Beethoven (op. 13) 
and to Mendelssohn's sister Fanny Hensel (op. 80). The three string quartets of Op. 44 were dedicated to the 
Crown Prince of Sweden and constitute an expansive centrepiece for this group of works. 
Our annotations, though reflecting an older version of the DCML standard, 
nonetheless provide an intriguing summary of the vertical logic serving Mendelssohn's elegant contrapuntal technique.

## Getting the data

* download repository as a [ZIP file](https://github.com/DCMLab/mendelssohn_quartets/archive/main.zip)
* download a [Frictionless Datapackage](https://specs.frictionlessdata.io/data-package/) that includes concatenations
  of the TSV files in the four folders (`measures`, `notes`, `chords`, and `harmonies`) and a JSON descriptor:
  * [mendelssohn_quartets.zip](https://github.com/DCMLab/mendelssohn_quartets/releases/latest/download/mendelssohn_quartets.zip)
  * [mendelssohn_quartets.datapackage.json](https://github.com/DCMLab/mendelssohn_quartets/releases/latest/download/mendelssohn_quartets.datapackage.json)
* clone the repo: `git clone https://github.com/DCMLab/mendelssohn_quartets.git` 


## Data Formats

Each piece in this corpus is represented by five files with identical name prefixes, each in its own folder. 
For example, the first movement of the first quartet, op. 12 has the following files:

* `MS3/01op12a.mscx`: Uncompressed MuseScore 3.6.2 file including the music and annotation labels.
* `notes/01op12a.notes.tsv`: A table of all note heads contained in the score and their relevant features (not each of them represents an onset, some are tied together)
* `measures/01op12a.measures.tsv`: A table with relevant information about the measures in the score.
* `chords/01op12a.chords.tsv`: A table containing layer-wise unique onset positions with the musical markup (such as dynamics, articulation, lyrics, figured bass, etc.).
* `harmonies/01op12a.harmonies.tsv`: A table of the included harmony labels (including cadences and phrases) with their positions in the score.

Each TSV file comes with its own JSON descriptor that describes the meanings and datatypes of the columns ("fields") it contains,
follows the [Frictionless specification](https://specs.frictionlessdata.io/tabular-data-resource/),
and can be used to validate and correctly load the described file. 

### Opening Scores

After navigating to your local copy, you can open the scores in the folder `MS3` with the free and open source score
editor [MuseScore](https://musescore.org). Please note that the scores have been edited, annotated and tested with
[MuseScore 3.6.2](https://github.com/musescore/MuseScore/releases/tag/v3.6.2). 
MuseScore 4 has since been released which renders them correctly but cannot store them back in the same format.

### Opening TSV files in a spreadsheet

Tab-separated value (TSV) files are like Comma-separated value (CSV) files and can be opened with most modern text
editors. However, for correctly displaying the columns, you might want to use a spreadsheet or an addon for your
favourite text editor. When you use a spreadsheet such as Excel, it might annoy you by interpreting fractions as
dates. This can be circumvented by using `Data --> From Text/CSV` or the free alternative
[LibreOffice Calc](https://www.libreoffice.org/download/download/). Other than that, TSV data can be loaded with
every modern programming language.

### Loading TSV files in Python

Since the TSV files contain null values, lists, fractions, and numbers that are to be treated as strings, you may want
to use this code to load any TSV files related to this repository (provided you're doing it in Python). After a quick
`pip install -U ms3` (requires Python 3.10 or later) you'll be able to load any TSV like this:

```python
import ms3

labels = ms3.load_tsv("harmonies/01op12a.harmonies.tsv")
notes = ms3.load_tsv("notes/01op12a.notes.tsv")
```


## Version history

See the [GitHub releases](https://github.com/DCMLab/mendelssohn_quartets/releases).

## Questions, Suggestions, Corrections, Bug Reports

Please [create an issue](https://github.com/DCMLab/mendelssohn_quartets/issues) and/or feel free to fork and submit pull requests.

## Cite as

> Hentschel, J., Rammos, Y., Neuwirth, M., & Rohrmeier, M. (2025). A corpus and a modular infrastructure for the empirical study of (an)notated music. Scientific Data, 12(1), 685. https://doi.org/10.1038/s41597-025-04976-z

## License

Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)).

![cc-by-nc-sa-image](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)

## Scores

Quartets nos. 1, 2, 4, 5, as well as no. 3 mvts. 2 & 3, were specially typeset for this project by Tom Schreyer. The remainder of Quartet no. 3 was typeset by MuseScore Pro contributor Nicolas Froment and Quartet no. 6 was typeset by MuseScore contributor Quasi Cantando. The scores correspond to volume 12 of the 1874-1882 Breitkopf und Härtel critical edition, though from that volume they exclude the *Four Pieces for String Quartet*, a collection of separate movements included in the volume as Op. 81.

## File naming convention

```regex
(?<quartet>\d{2})
op(?<op>\d{2})(?:,(?<no>\d))?
(?<movement>a|b|c|d)
```

## Overview
|file_name|measures|labels|standard| annotators | reviewers  |
|---------|-------:|-----:|--------|------------|------------|
|01op12a  |     292|   673|2.1.0   |Adrian Nagel|            |
|01op12b  |     128|   349|2.1.0   |Adrian Nagel|            |
|01op12c  |      65|   212|2.1.0   |Adrian Nagel|            |
|01op12d  |     313|   771|2.1.0   |Adrian Nagel|            |
|02op13a  |     251|   793|2.1.0   |Adrian Nagel|            |
|02op13b  |     125|   544|2.1.0   |Adrian Nagel|            |
|02op13c  |     163|   415|2.1.0   |Adrian Nagel|            |
|02op13d  |     397|   805|2.1.0   |Adrian Nagel|            |
|03op44,1a|     374|   748|2.1.0   |Uli Kneisel |Adrian Nagel|
|03op44,1b|     225|   393|2.1.0   |Uli Kneisel |Adrian Nagel|
|03op44,1c|     155|   437|2.1.0   |Uli Kneisel |Adrian Nagel|
|03op44,1d|     316|   819|2.1.0   |Uli Kneisel |Adrian Nagel|
|04op44,2a|     277|   837|2.1.0   |Adrian Nagel|            |
|04op44,2b|     244|   829|2.1.0   |Adrian Nagel|            |
|04op44,2c|      83|   328|2.1.0   |Adrian Nagel|            |
|04op44,2d|     515|   793|2.1.0   |Adrian Nagel|            |
|05op44,3a|     369|  1044|2.1.0   |Adrian Nagel|            |
|05op44,3b|     301|   635|2.1.0   |Adrian Nagel|            |
|05op44,3c|     131|   385|2.1.0   |Adrian Nagel|            |
|05op44,3d|     323|  1000|2.1.0   |Adrian Nagel|            |
|06op80a  |     324|   729|2.1.0   |Adrian Nagel|            |
|06op80b  |     301|   338|2.1.0   |Adrian Nagel|            |
|06op80c  |     120|   388|2.1.0   |Adrian Nagel|            |
|06op80d  |     461|   493|2.1.0   |Adrian Nagel|            |


*Overview table automatically updated using [ms3](https://ms3.readthedocs.io/).*
