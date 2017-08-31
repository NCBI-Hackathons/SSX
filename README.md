# Test1

##Workflow for Excel to python code to find somatic mutation SNPs in genes using NCBI's SNP FASTA and FLAT files along with NCBI's Nucleotide FASTA REFSEQ File for Humans
    
   # *parameters:
      - Will aid in the design of primers to construct internal standards (IS) for target gene variants in NGS variant fraction mix. These IS will control for multiple sources of analytical variance in NGS.  Controlling for this variation will allow for more reproducible NGS analysis results along with improved confidence limits of data analysis.
      - mTOR will be the first gene tested
      - only use SNPs w/ 0.01 <= MAF <= 0.5
      - part one of code should print 6 columns
      - parts 2 & 3: each step results in printing one more column
      - text coordinates are coordinates gotten from string, not genomic coordinates
      - preferably use python for this program because of its elegance and potential wide range of use
      
 # Part 1    
 ##Step1. download SNP fasta and flat files from NCBI. get Nucleotide refseq FASTA file from NCBI
 
 ##Step2. extract following information from FASTA and FLAT files:  SNP name, SNP genomic coordinate, MAF, 10 nucleotides to the left of SNP (L(10) nucleotides), SNP symbol, 10 nucleotides to the right of SNP (R(10) nucleotides)
 
 ##Step3. create a table with these six data columns as headers in the order listed in step 2.
 
 # Part 2
 ##Step1. Find L & R nucleotides in Nucleotide FASTA file, print out coordinates where they begin.
 
 ##Step2. Perform QC to make sure that L & R (10) are in the right places (they don't catch a repeat by mistake on left or right)
 
 ##Step3. Filter only L & R (10) sequences that pass QC, print the final QC text coordinates
 
 ##Step4. Convert the text coordinates to genomic coordinates
 
 # Part 3
 ##Step1. Search for QC L&R (10) sequences using QC text coordinates.  Print L and R results in 2 separate columns
 
 ##Step2. For Final column of 1st row, concatenate L(10), SNP symbol, and R(10)
 
 ##Step3. For second row, search in final column of previous row's output for L(10) and R(10) each, print resulting sequences in their respective cells below previous entry. Repeat this process for every row until last QC approved entry runs through.
 
 ##Step4. When Concatenating the final column for 2nd row, concatenate L(10), SNP symbol, R(10), and output of final previous column.Repeat this process for every row until last QC approved entry runs through.
 
 ##Step5. When final QC row is reached, take the output and put it into a text file.  This text file should have all the QC approved SNPs and L & R primers.
 
 
 
      
