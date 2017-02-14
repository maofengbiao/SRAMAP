# SRAtools
Convert SRA data to mapped BAM/SAM/Bigwig/Bed by one step in parallel computation
#:::dependencies:::

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

#:::SRAtools Usage:::

$ ./SRAtools -h

-i input SRR list file

-o output directory

-w SRR web site

-g genome reference indexed by bowtie2

-a adapter 1 [GATCGGAAGAGCACACGTCT]

-b adapter 2 [AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGT]

-q quality of trimming [20]

-p phred system value [33]

-t process number [10]

-m mapQ required [30]

-s size of bin for generating wig [50]

-e extend bases for reads for bam2bigwig [200]

-h the helpinformation

