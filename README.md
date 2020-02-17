# EEMS
## Changing VCF file to be accessible by bed2diffs#
First chromosome names were changed to numbers to make it accessible by plinkio using
```bash
sed 's/Chr1L/1/' 0 > 1
sed 's/Chr1S/2/' 1 > 2
sed 's/Chr2L/3/' 2 > 3
sed 's/Chr2S/4/' 3 > 4
sed 's/Chr3L/5/' 4 > 5
sed 's/Chr3S/6/' 5 > 6
sed 's/Chr4L/7/' 6 > 7
sed 's/Chr4S/8/' 7 > 8
sed 's/Chr5L/9/' 8 > 9
sed 's/Chr5S/10/' 9 > 10
sed 's/Chr6L/11/' 10 > 11
sed 's/Chr6S/12/' 11 > 12
sed 's/Chr7L/13/' 12 > 13
sed 's/Chr7S/14/' 13 > 14
sed 's/Chr8L/15/' 14 > 15
sed 's/Chr8S/16/' 15 > 16
sed 's/Chr9_10L/17/' 16 > 17
sed 's/Chr9_10S/18/' 17 > 18
```
(18 gave the file with all chromosomes renamed).
#Copied the file to compute canada server.
#Load vcftools
```
module load vcftools
```
Filter only chromosomes
```
--vcf borealis.vcf --chr 1 --chr 2 --chr 3 --chr 4 --chr 5 --chr 6 --chr 7 --chr 8 --chr 9 --chr 10 --chr 11 --chr 12 --chr 13 --chr 14 --chr 15 --chr 16 --chr 17 --chr 18 --recode --out borealis_subset_chr1-18
```
#removed Sca in header using
```
sed 's/Sca*//' in > out
```
#removed underscores using
```
sed 's/_//g' borealis_header_removed_ch_only.vcf>final
```

##converting VCF to PLINK
Search plink and load/cheack loadedmodules
```
module spider plink
module load plink/1.9b_4.1-x86_64
module list
```
#convert VCF to PLINK
```
plink --vcf final.vcf


