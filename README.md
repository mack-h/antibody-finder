# antibody-finder
Program to flexibly and comprehensively assess commercial/custom antibody products and corresponding protocol modifications for use in IHC across species. In active development.

PROGRAM OUTLINE:

BIG FUNCTIONS
- Make log file

- Run NCBI blast
	- Multiple species
	- Specified sequence range
	- Multiple sequences
	- Convert any protein ID into FASTA sequence
	- present the command to run the exact sequence in the terminal and note this in a log file with the date

In console:
In output file:

- Pull relevant NCBI BLAST data
	- percent similarity by species
		- option to specify a minimum cutoff
	- percent similarity by protein (include species)
		- option to specify a maximum cutoff
	- note species excluded
	- Amend entirety of downloadable BLAST data to a tab with the protein identifier in an excel file (this should perhaps be included as input with the other protein identification information. If none provided, default to protein name and range as the name of the tab)
	- option to do separate tabs (recommended), separate files


In console:
In output file: Sorted by: Protein ID, Sequence, % Similarity, Species by default (can specify in GUI or with option)

- Pull relevant ExPasy & other data by inputting FASTA sequence for the range specified
	- note to the user that this does not consider endcaps
	- extract sequence from FASTA
	- clip FASTA sequence to specified range
	- amend to BLAST data, include link to ExPasy page and recommended protocol parameters
	- amend links to log file

- Get immunogen sequence from product pages **have hard-coded option, and offer flex option attempt if not hard-coded. Recommended submitting as issue if doesn't work**
	- Use product page links or vendor name/protein ID --> search function
		- identify product page links
		- identify vendor name/protein ID combo
			- Google search 'vendor name antibodies'
				- click first link
					- find search bar
						- search terms
	- 'look for searchbar' function
		- common search elements
		- ignore common conflicting elements that include phrase 'search'
		- filter by elements of at least a certain length to start
		- if not bar, search for button; if button found, then search for bar; then input in bar
		- maybe have an option to show a screenshot, and user clicks on left upper corner of search bar (or wherever the element would map to); this maps to coordinates which help try again (find_element) function

	- directly use search tool to pull relevant products
		- option to include other keywords
		- include product page links in file
	- specify how many search results to include in console; specify how many to include in results

	- print all product spec headers, and specify which was used to retrieve the immunogen
		- offer to specify another header
			- code needs to use regex to attempt to pull from the input header instead
		
	
