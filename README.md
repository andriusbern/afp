# Alignment-Free phylogenetic tree construction from .fasta sequence files

# Distance measures used:
1. Cosine distance
2. Mahalanobis distance
3. Fractional k-mer count (best performing)

# Instructions
To compile using gcc under Linux (tested using version 7.3.1)
```
make AFP  [OR]   g++ AFP.cpp -o AFP
```
To run:
```
./AFP
```

Running './AFP' without arguments or with a flag '-h' will display the help dialog with additional
information.

Testing:
To test on [.paml or .fasta] files add the filename as the first argument, E.G:
    ./AFP sequences.fasta [OR] ./AFP sequences.paml

The output of the functions will be stored in:
    'Newick_real.txt' [OR] 'Newick_synthetic.txt' respectively for each format.

Additional arguments can be passed that are described in the help dialog.
