# GSOligos-Database
The database of Oligonucleotide specific to Mycobacterium Avium complex (MAC)

![Untitled-2](https://user-images.githubusercontent.com/43175313/182015289-dfc7fa6f-5650-4f5f-bf7a-4cfda9f16ce5.jpg)




Pre-Requisite:

. NCBI-BLAST (standalone)


COMMANDS:

Fastq to fasta conversion

cat read.R1.fa read.R2.fa >database (pair-end reads)

makeblastdb -dbtype nucl -in database (Database generation)

blastn -query probe.file -db database -evalue 10 -word_size 18 -out 0.01x.out -qcov_hsp_perc 100 -outfmt 6
