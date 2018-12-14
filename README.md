# Alignment-Free phylogenetic tree construction

Constructs a phylogenetic tree in [Newick tree format](https://en.wikipedia.org/wiki/Newick_format) using *.fasta* or *.paml* nucleotide sequence files as input.

## Instructions

### Compiling
To compile using gcc under Linux (tested using version 7.3.1)
```
make AFP
```
```
g++ AFP.cpp -o AFP
```

### Running with sequence files as input
```
./AFP filename.fasta
```
```
./AFP filename.paml
```
### Generating random trees

To generate a random phylogenetic tree with N nodes:
```
./AFP -random N
```

### Additional arguments
Running './AFP' without arguments or with a flag '-h' will display the help dialog with additional
information.

#### k-mer length (default 8)
To change the k-mer length used for constructing the distance matrix add flag *-k N*, e.g.:
```
./AFP filename.fasta -k 5
```

#### Distance measures
1. Cosine distance (flag *-c*)
2. Mahalanobis distance (flag *-m*)
3. Fractional k-mer count (default)

### Output
The output of the functions will be stored in 'Newick_real.txt', 'Newick_synthetic.txt', or 'Newick_random.txt'.

