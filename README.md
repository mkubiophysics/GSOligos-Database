# GSOligos-Database
The database of Oligonucleotide specific to Mycobacterium Avium complex (MAC)


![Untitled](https://user-images.githubusercontent.com/43175313/182015217-b624b342-2b52-47ed-8087-93066f1e0895.jpg)



Pre-Requisite:

. NCBI-BLAST (standalone)


COMMANDS:

Fastq to fasta conversion

cat read.R1.fa read.R2.fa >database (pair-end reads)

makeblastdb -dbtype nucl -in database (Database generation)

blastn -query probe.file -db database -evalue 10 -word_size 18 -out 0.01x.out -qcov_hsp_perc 100 -outfmt 6
