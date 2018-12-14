# Alignment-Free phylogenetic tree construction

Constructs a phylogenetic tree in [Newick tree format](https://en.wikipedia.org/wiki/Newick_format) using *.fasta* or *.paml* nucleotide sequence files as input.

# Distance measures used:
1. Cosine distance
2. Mahalanobis distance
3. Fractional k-mer count

# Instructions
To compile using gcc under Linux (tested using version 7.3.1)
```
make AFP    g++ AFP.cpp -o AFP
```
or 
```
g++ AFP.cpp -o AFP
```

To run:
```
./AFP filename.fasta
```
or 
```
./AFP filename.paml
```

Running './AFP' without arguments or with a flag '-h' will display the help dialog with additional
information.

To generate random phylogenetic trees with N nodes:
```
./AFP -random N
```

Testing:
To test on [.paml or .fasta] files add the filename as the first argument, E.G:
    ./AFP sequences.fasta [OR] ./AFP sequences.paml

The output of the functions will be stored in:
    'Newick_real.txt' [OR] 'Newick_synthetic.txt' respectively for each format.

Additional arguments can be passed that are described in the help dialog.
