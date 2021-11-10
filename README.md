# SubSumE Dataset

This repository contains the SubSumE dataset for subjective document summarization. See [the paper](https://aclanthology.org/2021.newsum-1.14/) and the [talk](https://www.youtube.com/watch?v=0vyUQArRrvY) for details on dataset creation.

## Dataset Files
Download the dataset from [here](https://drive.google.com/file/d/1tEDDHzZM_idnv-_PfRE5BmJU5E8yKLRH/view).

The dataset contains :
* Simplified text from 48 Wikipedia pages of the states in the US. Additionally, all the sentences in these documents
are put together in a single file `processed_state_sentences.csv` and are assigned a unique sentence id that 
is used in summary json files. 
* Intent-based summaries created by human annotators.

 
Each datapoint file in the directory `user_summary_jsons` contains a json containing summaries of Wikipedia pages
of eight states with following keys:
* **intent** : Summarization intent provided to human annotators for generating the summary
* **summaries**: List of summary jsons for eight states assigned to the annotator. Each json in the list contains following keys:
    * **state_name**: Name of the state
    * **sentence_ids**: Global ids of sentences (wrt `processed_state_sentences.csv`) present in the summary
    * **sentences**: List of sentences present in the summary
    * **use_keywords**: Keywords used by the annotator to search the document when creating summaries
	
	
### Acknowledgements
This work was supported by the NSF under grants IIS-1453543, IIS1943971, and
CCF-1763423, and a [Microsoft Research Dissertation
Grant](https://www.microsoft.com/en-us/research/academic-program/dissertation-grant/).
