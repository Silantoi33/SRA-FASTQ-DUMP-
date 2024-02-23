# SRA-FASTQ-DUMP-
How to install sra in ubuntu and run fastq-dump
1. Activate conda environment
2. Create a new environment for SRA
3. Activate the environment
4. use this command with this link to install SRA `https://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-ubuntu64.tar.gz`
5. Extract the content of the file using this command `tar -vxzf sratoolkit.tar.gz`
6. For convenience (and to show you where the binaries are) append the path to the binaries to your PATH environment variable using this command `export PATH=$PATH:$PWD/sratoolkit.3.0.10-ubuntu64/bin`  "check version"
7. Verify that the binaries will be found by the shell using this comand `which fastq-dump`
8. Run fastq-dump to download and split the file using this command `fastq-dump --gzip --skip-technical --readids --read-filter pass --dumpbase --split-3 --clip SRR8933535`
9. You can use this command to first download the SRA file first `prefetch SRR8933535'
10. Now split it using fastq-dump using this command `fastq-dump SRR8933535'
11. 
