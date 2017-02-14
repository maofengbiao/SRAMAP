# SRAtools
Convert SRA data to mapped BAM/SAM/Bigwig/Bed by one step in parallel computation
#:::dependents:::

#1. please install trim_galore and bowtie2 !!!!!!!
$ wget https://repo.continuum.io/miniconda/Miniconda2-latest-Linux-x86_64.sh
$ bash Miniconda3-latest-Linux-x86_64.sh
$ conda install -c bioconda trim-galore=0.4.1
$ conda install bowtie2

#2. please install bedtools, samtools and deeptools !!!!!!!!
$ conda install -c bioconda bedtools=2.26.0
$ conda install -c bioconda samtools=1.3.1
$ conda install -c bioconda deeptools=2.4.2

#3. please install GNU Parallel and fastq-dump (in sratoolkit) !!!!!!!
$ conda install -c bioconda parallel=20160622
$ wget http://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-centos_linux64.tar.gz
$ tar zxvf sratoolkit.current-centos_linux64.tar.gz

#4. basic shell knowlege !!!!!!!
$ export PATH=$PATH:/path/to/sratoolkit.x.x.x-centos_linux64/bin:/path/to/SRAtools

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
