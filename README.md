# sORFboost

`A program called sORFboost was created specifically to forecast the coding skills of sORFs.

The associated study is about "sORFboost" model that made by  using of machine learning algorithm xgboost.

Short open reading frames, or sORFs or smORFs, are 303 base pairs or less in length (including the stop codon) and, when translated, create micropeptides of approximately 100 amino acids. 

Due to evidence demonstrating their key roles in numerous essential biological functions, micropeptides are now receiving more attention than in the past due to their small size.


### What does sORFboost do?
When given a fasta file containing DNA fasta sequences, "sORFboost" will find all the sORFs (length = 303 bp) present in each of the sequence's three translation frames and return the predicted class label (coding or noncoding) as well as the probability of being in that class for each sORF. An output.csv file will contain all of the results.  



### Dependencies: 

Language dependency:
**`Python 3`** (Please do *not* use Python 2 to run the code.)

Library dependency:
* `Numpy`
* `pandas`
* `Bio` (the Biopython package: https://biopython.org)


### How to use:
```sh
cd sORFboost
python3 ./src/sORFboost.py input_fasta_file_path output_fasta_file_path
```

Note:
  *Your input fasta file's path is shown by the 'input_fasta_file_path' field. Please confirm that the fasta file contains just DNA sequences and not RNA or protein sequences. 
  * Due to the fact that the IDs will be used to name the discovered ORFs, please make sure that every entry in your fasta file has a *unique* ID. Additionally, please make sure that your sequences *only* contain the following four letters: 'A', 'T', 'C', and 'G'. Currently, *not* supported DNA letters include 'N', 'R', 'Y', etc.
  * The output '.csv' file's path is specified by the 'output_fasta_file_path' parameter. It is not required. 
  * It is advised that you give this output file a.csv extension if you decide to specify it. 
  * If you don't specify the output file, a'sORFboost_results.csv' file with the same name will be produced automatically under the same './sORFboost' directory as the output file. 

The output `.csv` file contains the following columns:
* `sORF_ID`: the ID of an sORF. 
* `sORF_seq`: the DNA sequence of the sORF (containing the stop codon with the start codon as `ATG`).
* `transcript_DNA_sequence_ID`: the ID of the original DNA sequence in your input fasta file where this sORF is extracted.
* `start_at`: the 1-based starting position of this sORF on the original DNA sequence. 
* `end_at`: the 1-based ending position of this sORF on the original DNA sequence. 
* `classification`: the predicted class of the sORF, either `coding` or `noncoding`. 
* `probability`: the probability that this sORF is in the assigned class.

### How to run a demo
There is a sample DNA sequence file `sample_seqs.fasta` under the directory `./demo_files/`. You can try to run `sORFboost` on this file:

```sh
cd sORFboost
python3 ./src/sORFboost.py ./demo_files/sample_seqs.fasta ./demo_files/sORFboost_results_on_sample_seqs.csv
```

This will output a file `sORFboost_results_on_sample_seqs.csv` under the same directory (`./demo_files/`).

