# GSOligos-Database
The database of Oligonucleotide specific to Mycobacterium Avium complex (MAC)



![Figure](https://user-images.githubusercontent.com/108401291/181876744-709e98f0-cc93-43f4-8597-4473dd909e71.jpg)


Pre-Requisite:

. NCBI-BLAST (standalone)


COMMANDS:

Fastq to fasta conversion

cat read.R1.fa read.R2.fa >database (pair-end reads)

makeblastdb -dbtype nucl -in database (Database generation)

blastn -query probe.file -db database -evalue 10 -word_size 18 -out 0.01x.out -qcov_hsp_perc 100 -outfmt 6
