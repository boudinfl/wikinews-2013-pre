# Preprocessed Wikinews Keyphrase benchmark dataset

* **update 2025/02/09** the dataset is available on huggingface: [https://huggingface.co/datasets/taln-ls2n/wikinews-fr-100](https://huggingface.co/datasets/taln-ls2n/wikinews-fr-100)

This dataset was introduced in:

 - **TopicRank: Graph-Based Topic Ranking for Keyphrase Extraction.**
   Adrien Bougouin, Florian Boudin, Béatrice Daille.
   *In Proceedings of the International Joint Conference on Natural Language
   Processing (IJCNLP), 2013.*

The dataset is split into three directories:

  * `references`: reference keyphrases for evaluation
  * `test`: test set
  * `src`: scripts and archive from which the dataset is built

Each input file is processed using the Stanford CoreNLP suite v3.6.0.
We use the default parameters and perform tokenization, sentence splitting and
Part-Of-Speech (POS) tagging. Files are in XML format.

Original raw text dataset can be retreived from this [link](bougouin-2013).

Reference keyphrases are in json format and named according to the following
rules:

    test.reader.[stem]?.json

reader-provided (stemmed or not) reference keyphrases for test.

Stemming (if applied), is performed with nltk Porter algorithm (French).

This corpus has been made for the evaluation of automatic keyphrase extraction
systems. It contains 100 French documents published on WikiNews between May 2012
and December 2012.

[witten-1999]: https://github.com/adrien-bougouin/WikinewsKeyphraseCorpus
