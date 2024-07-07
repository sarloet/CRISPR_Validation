# CRISPR_Validation

Code for CompBio coding Challenge.
Code is in .ipynb format for visualization purposes.


Workflow:

- Read in sequence from Fastq file
- Compute the reverse complement of the read
- Get Barcode and identify replicate number for the read
- Trimm off sequence barcodes and sequencing primers
- Align trimmed sequence to reference sequence using Needleman-Wunsch from Biopython ignoring sequences with bad alignement score
- Get index of target sequence in aligned sequence by pattern-matching the reference sequence
- Identify target nucleotide and PAM sequence ignoring target sequences where inserts/deletions and N in PAM
- Create and add to count matrices
- Calculate frequency matrices and plot the results

Features:

- Barcodes of replicates, target sequences and target nucleotide index can be specified and more barcodes added.
- Accounts for frameshifts in barcode sequences.
- Avoids reading the entire FASTQ file into memory.
