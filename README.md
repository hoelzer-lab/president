![](https://img.shields.io/github/v/release/hoelzer-lab/president)
![](https://img.shields.io/badge/licence-MIT-lightgrey.svg)
![](https://img.shields.io/badge/python-3.8-orange)
[![](https://img.shields.io/badge/ANI-definition-violet.svg)](https://pubmed.ncbi.nlm.nih.gov/17220447/)

# PRESIDENT: PaiRwisE Sequence IDENtiTy
Calculate pairwise nucleotide identity with respect to a reference sequence.

Given a reference and a query sequence (which can be fragmented), calculate
pairwise nucleotide identity with respect to the reference sequence.

#### Usage:
```
python pairwise_nucleotide_identity.py --query tiny_test.masked_consensus.fasta --reference NC_045512.2.fasta -x 3000 -p 8
```

#### Notes:
- nextstrain uses a quality threshold of < 3000 non-canonical nucleotides
- `N`s in the query are treated as mismatches, uncomment the corresponding line
(below) to ignore `N`s

#### Requirements:
- conda install -y -c bioconda python=3.8 mafft screed

#### ANI definition:
- https://pubmed.ncbi.nlm.nih.gov/17220447/

#### Spec:
> Sequence identity to a reference genome sequence (e.g. NC_045512.2) should be calculated at the nucleotide level relative to the entire length of the reference. Only informative nucleotides (A,T,G,C) are considered identical to each other.
