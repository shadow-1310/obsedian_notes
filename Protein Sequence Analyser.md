A webapp which can take a directory containing FASTA files an then parse the amino acid sequence, later which can be used for further analysis.
## Work done till now

[[2023-08-05]]

- made a class whose constructor will take the path of the directory containing the .fasta files as input and will create the dataframe containing the columns -  name of species, PDB_ID, chain_number, AA_sequence
- one more method is added which will calculate the percentages of the given amino acids within that sequence
	- it will take the list of amino acids as an input argument
- another method is also added which can remove speciific rows from the dataframe based on the user input of pdb_id.

### Next
- implement proper directory structure taking help from the Krish Naik mlflow video
- implement logger and exception handler

## to do
- download FASTA file through ncbi API 
	- https://www.rcsb.org/docs/programmatic-access/file-download-services
	- https://www.rcsb.org/docs/programmatic-access/file-download-services
