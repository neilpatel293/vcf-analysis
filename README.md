# vcf-analysis
Compares two or vcf files containing variants and reports variants duplicated between different vcf files with user-specified rules. 

Options

-R : Rules for comparing the vcf files. -R can be used multiple times in the same command. 
Possible values: genes, chromosome, startPos, endPos 

-M : Necessary is vcf-analysis is given a merged vcf file containing variant calls from different samples. 

-O : The output directory.

-I : The input vcf files. Multiple vcf files can be specified by leaving a space between the file locations/names. 

-F : The filters that are applied once duplicates between samples have been found. The format is : column heading:value. 
For numerical values, the value can be a number or a range using the <>= characters (ie. >=0.5). Multiple filters can be
specified by using -F multiple times in the same command. 

-V : Verbose. Use if you wish to get instantaneous updates on what vcf-analysis is doing. 

Dependencies: 
1.) VCFtools (v0.1.14) is used for parsing the vcf files (ie. converting vcf files into a format readable by vcf-analysis) and to merge 
    the vcf files into a single vcf file for processing if multiple vcf files are provided. 
