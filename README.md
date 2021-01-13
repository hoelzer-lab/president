![](https://img.shields.io/github/v/release/hoelzer-lab/president)
![](https://img.shields.io/badge/licence-MIT-lightgrey.svg)
![](https://img.shields.io/badge/python-3.8-orange)
[![](https://img.shields.io/badge/ANI-definition-violet.svg)](https://pubmed.ncbi.nlm.nih.gov/17220447/)

# PRESIDENT: PaiRwisE Sequence IDENtiTy
Calculate pairwise nucleotide identity with respect to a reference sequence.

Given a reference and a query sequence (which can be fragmented), calculate
pairwise nucleotide identity with respect to the reference sequence relative 
to the entire length of the reference. Only informative nucleotides (A,T,G,C) 
are considered identical to each other.

#### Requirements:
```
conda create -y -n president -c bioconda python=3.8 mafft screed && conda activate president
```

#### Usage:
```
python pairwise_nucleotide_identity.py --query NC_045512.2.20mis.fasta --reference NC_045512.2.fasta -x 3000 -p 8
```

#### Notes:
- nextstrain uses a quality threshold of < 3000 non-canonical nucleotides
- Ns in the query are treated as mismatches, uncomment the corresponding line directly in the code to ignore Ns

#### ANI definition:
- https://pubmed.ncbi.nlm.nih.gov/17220447/

