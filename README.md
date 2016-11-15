# SRA_Pipe
Convert SRA data to BAM/Bigwig/bed by one step in parallel computation
#:::dependents:::

#1. pleas install samtools and deeptools !!!!!!!!
#2. pleas install trim_galore and bowtie2 !!!!!!!
#3. basic shell knowlege !!!!!!!

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
adp1=GATCGGAAGAGCACACGTCT
adp2=AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGT
# min quality of seq
quality=20 
#phred value (33/64)
phred=33 
#parallel number
parallel=10 
#mapping quality
mapQ=30
#for bam2bigwig
binSize=50
extend=200
