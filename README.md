# SOC HYP Final Report Boilerplate

This repository is meant as a quickstart guide for NUS SOC students doing their Honors Year Project (HYP, _aka FYP_) final report in LaTeX.

It handles all the necessary styling and formatting of the final report so you can focus on your content.

\*If you aren't going to use LaTeX _(which is really awesome)_ for your final report, then you should ignore this entire repository. There is nothing here for you. _(Except maybe how the final report should look like.)_

## Pre-requisites
You need to install __LaTeX__ in order to build the final report.

This document should explain how to do it for you particular machine: [http://latex-project.org/ftp.html](http://latex-project.org/ftp.html)

## Usage
0. Install LaTeX.
0. Fork this repository.
0. Edit content.
0. Build report.
0. Repeat as necessary.

Once you have LaTex installed, you simply run the following command in the root folder of project to __build your report__:

```
# Optional, if you want to do a "clean" build.
$ make clean

$ make report
```

This generates a __`report.pdf`__ file in the folder. Don't worry if you notice many other files being created. These are basically files created during the various intermediate steps of the build process.

## Project Structure

This project is structured as follows:
```
.
|-- Makefile
|-- README.md
|-- contents
|   |-- conclusion.tex
|   |-- intro.tex
|   `-- results.tex
|-- images
|   |-- giraffe.jpg
|   `-- squirrel.jpg
|-- report.bib
|-- report.tex
|-- socreport.bst
|-- socreport.cls
`-- tables
    `-- example.tex
```

- `report.tex`:
    - This is the main file. It contains the meta information, abstracts, acknoledgements and all other includes.
    - Edit this file with information about your project.
- `./contents/`:
    - This folder contains the text of the report. I included three example `.tex` files which are included in the `report.tex`.
    - Remove/Add files in this folder and update `report.tex` as necessary.
- `./images/`:
    - This folder is used to contain all images.
    - LaTex is also told to look for images here in `report.tex`
- `./tables/`:
    - This folder contains the tables used in the report.
    - Take a look at the example table included.
- `report.bib`:
    - This file contains the information for references in the report.
    - Copy paste the BibTex citations and used them in the report using `\cite{}`.
    - An example in included in the introduction.

## Text Formatting

Not specific to this repository, but just some LaTeX stuff to help with writing and formatting your report. These should cover 90% of all your usage.

### Basic Text Formating

- __Bold__ text: `\textbf{Bold} text`
- _italics_: `\textit{italics}`
- `monospace` text: `\texttt{monospace} text`

### Citations

To cite something, use `\cite{CITATION_REF}` where `CITATION_REF` is the citation reference.

To cite something from Google Scholar:

0. Find the paper
0. Click `cite -> BibTex`
0. Copy the text shown and paste into `report.bib`

This should look something like:
```
@book{lamport1986document,
  title={Document Preparation System},
  author={Lamport, Leslie and LaTEX, A},
  year={1986},
  publisher={Addison-Wesley Reading, MA}
}
```

0. This first argument is the citation reference.

### Math and Equations

ShareLaTeX has a good intro guide here: [https://www.sharelatex.com/learn/Mathematical_expressions](https://www.sharelatex.com/learn/Mathematical_expressions).

For simple inlined symbols, wrap then in `$`: eg. $x^2$

### Tables and Figures
A intro guide for tables is: [https://www.sharelatex.com/learn/Tables](https://www.sharelatex.com/learn/Tables) and for graphs is [https://www.sharelatex.com/learn/Pgfplots_package](https://www.sharelatex.com/learn/Pgfplots_package).

I also recommend using a web editor to visually create any tables you want and using them to generate tex. Eg. [http://www.tablesgenerator.com/](http://www.tablesgenerator.com/)), there are many others.


## Credits
0. This project uses the awesome `Makefile` courtesy of Chris Monson. You can read more about it here: [http://www.bouncingchairs.net/oss/latex.html](http://www.bouncingchairs.net/oss/latex.html) or find its source here: [https://github.com/shiblon/latex-makefile](https://github.com/shiblon/latex-makefile).
0. The `socreport.bst` and `socreport.cls` files are courtesy of Prof Lee Wee Sun. It basically does all the magic in making the report look like it should.
0. The format of this repository is heavily inspired by @shawntan who graciously shared it, saving me hours of my life.
0. `gitignore` taken from [https://github.com/github/gitignore](https://github.com/github/gitignore)
0. Giraffe Image taken from [here](https://www.flickr.com/photos/badjonni/15080255893/in/photolist-oYAfFX-onsqXy-o4CBiR-nMrrz8-nMrH3b-oncEgX-34V2Vg-89B8vb-nCDGGk-7t5JJh-k9fxhg-7DoLjP-9Vy7gm-o4PBp1-7t5K4U-nMstXk-fNd8kE-asGFjd-ciYqas-95sxFD-5us7yz-g2iZgE-6gYn1H-e1Rp8P-bUWqhD-oQaAHa-7t5JWN-4qLVpd-6WuKKv-cea3K-29vTaP-bVyB6p-4pbafF-bW1Ckn-ehSbUo-6AvK1j-bVPGzc-e1Rps4-etgap5-6VXn2n-7QoFUj-83zVeR-7EjVWt-4uwwPQ-of4Vwg-49ZGtp-bu9dVW-cXAU4W-8HNMSn-aAujKA)
0. Squirrel Image taken from [here](https://www.flickr.com/photos/genista/127048347/in/photolist-ciYqas-95sxFD-5us7yz-g2iZgE-6gYn1H-e1Rp8P-bUWqhD-oQaAHa-7t5JWN-4qLVpd-6WuKKv-cea3K-29vTaP-bVyB6p-4pbafF-bW1Ckn-ehSbUo-6AvK1j-bVPGzc-e1Rps4-etgap5-6VXn2n-7QoFUj-83zVeR-7EjVWt-4uwwPQ-of4Vwg-49ZGtp-bu9dVW-cXAU4W-8HNMSn-aAujKA-64WtLN-4vRtCy-fPxuFz-72hsLr-gbh18h-k9fz8v-ffdVcQ-f77UyT-p9b2tG-6cnoSG-89AWNJ-qSSwFP-p8tHw3-p37F3C-dhwwUe-nicLJs-qUaLPt-pnftZH)
