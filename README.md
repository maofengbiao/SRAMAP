# SRA_Tools
Convert SRA data to BAM/SAM/Bigwig/Bed by one step in parallel computation
#:::dependents:::

#1. please install samtools and deeptools !!!!!!!!
#2. please install trim_galore and bowtie2 !!!!!!!
#3. please install fastq-dump and GNU Parallel !!!!!!!
#4. basic shell knowlege !!!!!!!


#:::parameters setting:::
#srrlist deposit directory
rootdir= 
#SRR name list
srrlist=$rootdir/srr.list 
# SRR deposit ftp site
sraftpdir= 
#spacies
specie=mouse #spacies
#db version
dbver=mm10
#db ref index by bowtie2
refindex=/data/fmao/db/$specie/$dbver/Bowtie2Index/genome 
#output dir
outdir= 
#sra output dir
sra_out=$outdir/sra 
#fq output dir
fq_out=$outdir/fq 
#clean output dir
clean_out=$outdir/clean
#bowtie2 output dir
bowtie2_out=$outdir/bowtie2
#adapter_forward
adp1=GATCGGAAGAGCACACGTCT
#adapter_reverse
adp2=AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGT
# min quality of seq
quality=20 
#phred value (33/64)
phred=33 
#parallel number
parallel=10 
#mapping quality
mapQ=30
##Parameters for bam2bigwig
#binSize
binSize=50
#extend base
extend=200
