# Sequence Analysis Workflow

## Objective
To verify and characterize the canonical human TDP-43 protein sequence prior to dwonstream structural and computational analyses. 

## Data Source
Protein sequence downloaded from [UniProt](https://www.uniprot.org/uniprotkb/Q13148/entry#sequences)
Accession:
Q13148

Species:
Homo sapiens
---
## Software
Software used was SeqKit v2.13.0

Downloaded from [SeqKit - Ultrafast FASTA/Q kit](https://bioinf.shenwei.me/seqkit/). 

Why Seqkit? I used it to rapidly validate the integrity of the downloaded FASTA sequence before downstream structural analysis in pyMOL and sequence analysis in Python. 

## Commands used
### Sequence Statistics

```bash
seqkit stats TDP43_HUMAN.fasta
```

Purpose:
- Verify FASTA format
- Confirm sequence type
- Determine sequence length

---

### Convert FASTA to tabular format

```bash
seqkit fx2tab -l TDP43_HUMAN.fasta
```

Purpose:

- Extract sequence identifier
- Display amino acid sequence
- Calculate sequence length

### Output
```text
file               format  type     num_seqs  sum_len  min_len  avg_len  max_len
TDP43_HUMAN.fasta  FASTA   Protein         1      414      414      414      414
```

```text
sp|Q13148|TADBP_HUMAN TAR DNA-binding protein 43 OS=Homo sapiens OX=9606 GN=TARDBP PE=1 SV=1    MSEYIRVTEDENDEPIEIPSEDDGTVLLSTVTAQFPGACGLRYRNPVSQCMRGVRLVEGILHAPDAGWGNLVYVVNYPKDNKRKMDETDASSAVKVKRAVQKTSDLIVLGLPWKTTEQDLKEYFSTFGEVLMVQVKKDLKTGHSKGFGFVRFTEYETQVKVMSQRHMIDGRWCDCKLPNSKQSQDEPLRSRKVFVGRCTEDMTEDELREFFSQYGDVMDVFIPKPFRAFAFVTFADDQIAQSLCGEDLIIKGISVHISNAEPKHNSNRQLERSGRFGGNPGGFGNQGGFGNSRGGGAGLGNNQGSNMGGGMNFGAFSINPAMMAAAQAALQSSWGMMGMLASQQNQSGPSGNNQNQGNMQREPNQAFGSGNNSYSGSNSGAAIGWGSASNAGSGSGFNGGFGSSMDSKSSGWGM          414
```
