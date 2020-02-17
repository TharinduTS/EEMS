# EEMS
## Changing VCF file to be accessible by bed2diffs#
First chromosome names were changed to numbers to make it accessible by plinkio using
''bash
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
sed 's/Chr9_10S/18/' 17 > 18(18 gave the file with all chromosomes renamed).
''
Copied the file to compute canada server.

