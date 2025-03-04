![Version](https://img.shields.io/github/v/release/DCMLab/mendelssohn_quartets?display_name=tag)
[![DOI](https://zenodo.org/badge/{{ zenodo_badge_id }}.svg)](https://zenodo.org/badge/latestdoi/{{ zenodo_badge_id }})
![GitHub repo size](https://img.shields.io/github/repo-size/DCMLab/mendelssohn_quartets)
![License](https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-9cf)


This is a README file for a data repository originating from the [DCML corpus initiative](https://github.com/DCMLab/dcml_corpora)
and serves as welcome page for both 

* the GitHub repo [https://github.com/DCMLab/mendelssohn_quartets](https://github.com/DCMLab/mendelssohn_quartets) and the corresponding
* documentation page [https://dcmlab.github.io/mendelssohn_quartets](https://dcmlab.github.io/mendelssohn_quartets)

For information on how to obtain and use the dataset, please refer to [this documentation page](https://dcmlab.github.io/mendelssohn_quartets/introduction).

# Felix Mendelssohn – String Quartets

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


## Cite as

## Version history

See the [GitHub releases](https://github.com/DCMLab/mendelssohn_quartets/releases).

## Questions, Suggestions, Corrections, Bug Reports

Please [create an issue](https://github.com/DCMLab/mendelssohn_quartets/issues) and/or feel free to fork and submit pull requests.

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
|03op44,1a|     374|   751|2.1.0   |Uli Kneisel |Adrian Nagel|
|03op44,1b|     225|   393|2.1.0   |Uli Kneisel |Adrian Nagel|
|03op44,1c|     155|   438|2.1.0   |Uli Kneisel |Adrian Nagel|
|03op44,1d|     316|   819|2.1.0   |Uli Kneisel |Adrian Nagel|
|04op44,2a|     277|   839|2.1.0   |Adrian Nagel|            |
|04op44,2b|     244|   829|2.1.0   |Adrian Nagel|            |
|04op44,2c|      83|   328|2.1.0   |Adrian Nagel|            |
|04op44,2d|     515|   794|2.1.0   |Adrian Nagel|            |
|05op44,3a|     369|  1044|2.1.0   |Adrian Nagel|            |
|05op44,3b|     301|   635|2.1.0   |Adrian Nagel|            |
|05op44,3c|     131|   385|2.1.0   |Adrian Nagel|            |
|05op44,3d|     323|  1000|2.1.0   |Adrian Nagel|            |
|06op80a  |     324|   729|2.1.0   |Adrian Nagel|            |
|06op80b  |     301|   338|2.1.0   |Adrian Nagel|            |
|06op80c  |     120|   388|2.1.0   |Adrian Nagel|            |
|06op80d  |     461|   493|2.1.0   |Adrian Nagel|            |


*Overview table automatically updated using [ms3](https://ms3.readthedocs.io/).*
