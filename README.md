# GSOligos-Database
The database of Oligonucleotide specific to Mycobacterium Avium complex (MAC)



![Untitled (2)](https://user-images.githubusercontent.com/43175313/181879632-a28e6498-5f14-4761-9732-40dd0c4b52f2.jpg)



Pre-Requisite:

. NCBI-BLAST (standalone)


COMMANDS:

Fastq to fasta conversion

cat read.R1.fa read.R2.fa >database (pair-end reads)

makeblastdb -dbtype nucl -in database (Database generation)

blastn -query probe.file -db database -evalue 10 -word_size 18 -out 0.01x.out -qcov_hsp_perc 100 -outfmt 6
