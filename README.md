# Snappy-Picrust
---
Snappy-Picrust is the first Bio-snap! Pronounced *very* sassy-like "Bi-O-Snap!"

## Whats a snap?
Snaps are a new type of packaging system introduced for Ubuntu 16.04 LTS. Snaps are
container-like packages that I believe can alleviate the dependency hell that many
bioinformaticist experience. For more information check out [Ubuntu's Snap page](https://developer.ubuntu.com/en/desktop/).

## Whats a PICRUSt?
It's the Phylogenetic Investigation of Communities by Reconstruction of Unobserved States

According to the PICRUSt [site](https://picrust.github.io/picrust/) it's:
PICRUSt (pronounced “pie crust”) is a bioinformatics software package designed to predict metagenome functional content from marker gene (e.g., 16S rRNA) surveys and full genomes.

You should check out the [publication](http://www.nature.com/nbt/journal/vaop/ncurrent/abs/nbt.2676.html)
>Predictive functional profiling of microbial communities using 16S rRNA marker gene sequences. Langille, M. G.I.\*; Zaneveld, J.\*; Caporaso, J. G.; McDonald, D.; Knights, D.; a Reyes, J.; Clemente, J. C.; Burkepile, D. E.; Vega Thurber, R. L.; Knight, R.; Beiko, R. G.; and Huttenhower, C. Nature Biotechnology, 1-10. 8 2013.

## OK so what is a Snappy-Picrust?
Snappy-Picrust is the picrust package wrapped up in it's own little snappy container! I like to call it the first Bio-snap. My goal is to make using bioinformatics packages friendly to install.

## Installation
To install the snap just `sudo snap install picrust_1_amd64.snap`
Then connect the snap to your home folder `sudo snap connect picrust:home ubuntu-core:home`
