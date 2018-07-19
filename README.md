# PubMed PICO Element Detection Dataset
This dataset is introduced by *[Jin, Di, and Peter Szolovits. "PICO Element Detection in Medical Text via Long Short-Term Memory Neural Networks." Proceedings of the BioNLP 2018 workshop. 2018.](http://www.aclweb.org/anthology/W18-2308)*.

Abstract

>Successful evidence-based medicine (EBM) applications rely on answering clinical questions by analyzing large medical literature databases. In order to formulate a well-defined, focused clinical question, a framework called PICO is widely used, which identifies the sentences in a given medical text that belong to the four components: Participants/Problem (P), Intervention (I), Comparison (C) and Outcome (O). In this work, we present a Long Short-Term Memory (LSTM) neural network based model to automatically detect PICO elements. By jointly classifying subsequent sentences in the given text, we achieve state-of-the-art results on PICO element classification compared to several strong baseline models. We also make our curated data public as a benchmarking dataset so that the community can benefit from it.

Some miscellaneous information:
-  `structured_abstracts_PICO` contains the original abstracts. The line that starts with `###` indicates the PMID. After that line, each line contains the original section heading, the assgined gold label for train and test and the section content, separated by the symbol `|`. To create the gold label, key words in the section heading are checked and the mapping rule can be referred to the paper above-mentioned.
- `structured_abstracts_sentences_PICO` is almost the same as `structured_abstracts_PICO` except that each section conent is sentence splitted using the [Stanford CoreNLP toolkit](https://stanfordnlp.github.io/CoreNLP/index.html) so that each line has only one sentence and all numbers have been replaced by `@`.
- The folder `splitted` contains the train, validation and test sets that are randomly splitted from the file `structured_abstracts_sentences_PICO` at the ratio of 8:1:1.

You are most welcome to share with us your analyses or work using this dataset by citing our paper!
