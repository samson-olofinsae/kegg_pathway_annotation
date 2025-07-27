# KEGG Pathway Annotation Tool


## Author

**Samson Olofinsae**  

This Python script allows you to annotate a list of human genes with their associated functional pathways from the KEGG database.

## Overview

- Converts NCBI Gene IDs to KEGG gene identifiers.
- Uses the KEGG REST API to retrieve pathway associations.
- Outputs a table showing gene-pathway mappings along with functional descriptions.

## Input

A tab-separated file named `genes.tsv` containing:
```
GeneID	GeneName
NCBI_GENE_ID1	Name1
NCBI_GENE_ID2	Name2
...
```

## Output

A file `pathways.csv` with the following columns:

- `GeneID`
- `GeneName`
- `KEGGID`
- `KEGGPathwayID`
- `PathwayDescription`

## Dependencies

- Python 3.x
- pandas
- requests
- biopython

Install dependencies:
```bash
pip install pandas requests biopython
```

## Usage

Place your `genes.tsv` file in the same directory and run:
```bash
python annotate_genes_with_kegg_pathways.py
```

## Example Use Case

This tool was originally developed for investigating genes involved in Gorlin Syndrome by linking NCBI gene IDs to functional pathways via KEGG and OMIM.

## License

MIT License


## Ethical Statement
This tool is strictly educational and publicly reproducible. It does not use or replicate any private data, code, or intellectual property from NHS or affiliated institutions. All KEGG queries are made using public API endpoints under standard academic fair use. The tool is independently developed by the author and released under the MIT license.
