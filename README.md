# SubSumE Dataset

This repository contains the SubSumE dataset for subjective document summarization.  See [the paper](https://aclanthology.org/2021.newsum-1.14/) for details on dataset creation.

## Dataset Files:
The dataset contains :
* Simplified text from Wikipedia pages of the states in US. Additionally, all the sentences in these documents
are put together in a single file `processed_state_sentences.csv` and are assigned a unique sentence id that 
is used in summary json files. 
* Intent-based summaries created human annotators.

 
Each datapoint file in [user_summary_jsons]() folder contains a json containing summaries of Wikipedia pages
of eight states with following keys:
* **intent** : Summarization intent provided to human annotators for generating the summary
* **summaries**: List of summary jsons for eight states assigned to the annotator. Each json in 
the list contains following keys:
    * **state_name**: Name of the state
    * **sentence_ids**: Global ids of sentences (wrt `processed_state_sentences.csv`) present in the summary.
    * **sentences**: List of sentences present in the summary.
    * **use_keywords**: Keywords used by the annotator to search the document when creating summaries.
