# AtisAligned

## Introduction
Atis-Aligned is a semantic parsing dataset that was obtained by augmenting the popular [ATIS dataset](https://dl.acm.org/doi/10.3115/1075812.1075823) with word alignments. 

## Format
The dataset can be found in the `data` folder and it comes in `.csv` format. There are five columns:
1. ID : contains the id of the example
2. NL : contains the natural language queries
3. MR : contains the meaning representation
4. ALIGNMENT : contains the word alignments
5. MONOTONIC : contains 0-1 labels indicating whether the alignment is monotonic

There are two versions of the dataset:
- `EN.csv` contains the dataset with manually annotated word alignments
- `EN_giza.csv` contains the dataset with automatically annotated word alignments using the [GIZA++ tool](https://github.com/moses-smt/giza-pp)

The `splits` folder contains lists of IDs for three different test splits: 
- a question split, which ensures that the NL questions at test time have not been observed at training time
- a query split, which ensures that the MR queries at test time have not been observed at training time
- a length split, which ensures that the MR queries at test time are longer than those observed at training time

The test set IDs are found in the `test.txt` files. Moreover, we provide three development sets `dev1.txt`, `dev2.txt` and `dev3.txt`, which can be used for validation.
