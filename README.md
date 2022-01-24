# Some write-up with Links

## Raven
Raven is a C++ based De Novo Genome assembler based on heuristics and statistics (no machine learning involved). You can read more details in this paper: https://www.biorxiv.org/content/10.1101/2020.08.07.242461v2.full.pdf And Robert Vaser's PhD Thesis: https://www.bib.irb.hr/1052813/download/1052813.Robert_Vaser_doktorat.pdf

You can find Raven here: https://github.com/lbcb-sci/raven
To install and run Raven we recommend Ubuntu or WSL on Windows. 

For the AI projects we use Raven only for the overlap phase, the first step of the OLC De Novo Genome Assembly paradigm. Instead of creating the full assembly we only want raven to do the overlap phase and output a nice graph. We usually use this Raven fork for this task: https://github.com/lvrcek/raven/tree/filter

Currently we use 2 different types of data: 1) perfect synthetical reads and 2) real reads. Both are Human genome chromosomes and are based on the references from here: https://github.com/marbl/CHM13

To analyze the Raven Graphs we use usually Graphia (it should be pre-installed on the laptops). Another tool called Bandage can also be used (for directly seeing some properties of the .gfa files).

The goal is to adjust Raven so, that it is able to create well connected graph for at least the perfect-reads data sets.
