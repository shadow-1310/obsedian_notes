### Training Material
#### Mutations
##### Types
- Point Mutation
	- change in one base
- Substitution
	- one or more base is replaced by same number of bases
- Inversion
	- segment of chromosome is reversed end to end.
- Insertion
	- new base is added to sequence
- Deletion
	- base is deleted from sequence
##### Results
- Neutral
##### Variants Nomenclature
HGVS - Human Genomic Variation Society
- Genomic HGVS
	- g.5A>T and g.10C>T
- Coding HGVS
- Protein HGVS
	- p.His2Pro

##### Variant Lebels
- pathogenic
- likely pathogenic
- VUS- Variant of Unknown Significance
- Likely Benign
- Benign

### WGS process
1. DNA Extraction
2. DNA shearing
3. DNA library preparation
4. DNA library sequencing
5. DNA sequence assembly ( Reconstructing)

Human reference genome
- hg19 - 2009
- hg38 - 2013


#### Variant Database
dbSNP, ClinVar, gnomAD
- SNPs
	- Single Nucleotide Polymorphism
- Indels
	- Insertions and Deletions
- CNVs 
	- Copy Number Variations
	- alteration in number of copies of specific DNA segment
- Structural Variants

#### Common File Types
- FASTQ
	- raw sequence data of short DNA segment along with quality scores
- BAM
	- it is generated after sequence read from FASTQ has been aligned to reference genome
- VCFs

Primary Analysis
- Initial process of reading sequence data to obtain DNA sequence
- Along with quality scores
Secondary Analysis
- aligning reads to reference genome identifying variants through variant calling
Tertiary Analysis
- interpretation and annotation of genetic variants to understand their biological significance and impact on health

### StrandNGS
- Does Primary and Secondary Analysis
#### StrandOmics
- Does Tertiary Analysis

Pre-mRNA --> Splicing --> final mRNA

Why splicing is required
- Reusability ->Alternative Splicing
- instead of having separate gene for each protein
- cell leverage intro-exon mechanism to create multiple protein from same gene