# SRA_Pipe
Convert SRA data to BAM/Bigwig/bed by one step in parallel computation
#:::dependents:::

#1. pleas install samtools and deeptools !!!!!!!!
#2. pleas install trim_galore and bowtie2 !!!!!!!
#3. basic shell knowlege !!!!!!!

#:::parameters setting:::

rootdir= #srrlist deposit directory
srrlist=$rootdir/srr.1.list #SRR name list
sraftpdir= # SRR deposit ftp site
samplist=$srrlist #sample list
specie=mouse #spacies
dbver=mm10 #db version
refindex=/data/fmao/db/$specie/$dbver/Bowtie2Index/genome #db ref index by bowtie2

outdir= #output dir
sra_out=$outdir/sra #sra output dir
fq_out=$outdir/fq #fq output dir
clean_out=$outdir/clean #clean output dir
bowtie2_out=$outdir/bowtie2 #bowtie2 output dir
adp1=GATCGGAAGAGCACACGTCT
adp2=AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGT
quality=20 # min quality of seq
phred=33 #phred value (33/64)
parallel=10 #parallel number
mapQ=30 #mapping quality
#for bam2bigwig
binSize=50
extend=200
