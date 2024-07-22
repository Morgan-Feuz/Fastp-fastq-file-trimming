# FastQ File Trimming with Fastp

### Background
Fastp is a tool designed for FastQ file preprocessing, such as trimming adapters or polyX in the 3' ends (e.g., polyG artifacts). 
For more detailed information on Fastp usages, the main GitHub page is [here](https://github.com/OpenGene/fastp) and the accompanying paper is [here](https://academic.oup.com/bioinformatics/article/34/17/i884/5093234).

<ins>Note:</ins> Fastp is only supported for Linux of macOS, but is also available on Galaxy as well if necessary. 

----------------------------------------------------------------------------------------------------

### Linux Installation

<ins>Bioconda installation:</ins>
```
# Note: the Fastp version in Bioconda may not be the lastest
$ conda install -c bioconda fastp
$ fastp --version

$ conda update fastp
$ fastp --version
# 0.23.4 (latest)

```
More information on Conda and Bioconda is available [here](https://github.com/Morgan-Feuz/conda-virual-envs). 


<ins>Download the latest prebuilt binary:</ins>
```
$ wget http://opengene.org/fastp/fastp
$ chmod a+x ./fastp
```
------------------------------------------------------------------------------------------------------

### Basic Usage
```
# For single-end Illumina FastQ reads with PolyX trimming enabled
$ fastp -i /path/to/file/fastq.gz -o /path/for/results/fastp_trimmed -x --report_title "Fastp Trimmed Title" --json=fastp.json --html=fastp.html
```







