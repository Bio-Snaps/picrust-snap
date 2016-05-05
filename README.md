# Picrust-Snap
---
Picrust-Snap is the first Bio-snap! Pronounced *very* sassy-like "Bi-O-Snap!"

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

### Requirements
* Ubuntu 16.04 LTS 64-bit
* snapd
    * `sudo apt-get install snapd`
* snapcraft
    * `sudo apt-get install snapcraft`

### Building the snap
Copy the `python2numpy.py` to the snapcraft plugins directory
`sudo cp ./python2numpy /usr/lib/python3/dist-packages/snapcraft/plugins/`
Numpy 1.5.1 was a pain to build, it required certain env flags, python2numpy is just an extension of the existing python2 plugin that can compile numpy.

Data directory must contain the additional picrust data from here:
[16S copy number normalization](ftp://ftp.microbio.me/pub/picrust-references/picrust-1.0.0/16S_13_5_precalculated.tab.gz)
[KEGG Ortholog predictions](ftp://ftp.microbio.me/pub/picrust-references/picrust-1.0.0/ko_13_5_precalculated.tab.gz)

Then `snapcraft snap` should result in a file called `picrust_1_amd64.snap`. Install this with `sudo snap install picrust_1_amd64.snap`

We then need to connect it to our homespace, which is not done by default for security with:
`sudo snap connect picrust:home ubuntu-core:home`

Now it's all installed!

## Commands

A list of all the picrust commands:
```
picrust.ancestral-state-reconstruction  
picrust.metagenome-contributions        
picrust.print-picrust-config          
picrust.categorize-by-function          
picrust.normalize-by-copy-number        
picrust.run-genome-evaluations        
picrust.compare-biom                    
picrust.parallel-predict-traits         
picrust.scale-metagenome              
picrust.evaluate-test-datasets          
picrust.pool-test-datasets              
picrust.start-parallel-jobs           
picrust.format-tree-and-trait-table     
picrust.predict-metagenomes             
picrust.start-parallel-jobs-sge       
picrust.make-test-datasets              
picrust.predict-traits                  
picrust.start-parallel-jobs-torque    
```

