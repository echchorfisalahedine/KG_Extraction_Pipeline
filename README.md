# Towards an Extensible Pipeline for Biomedical Knowledge Graph Construction from Scientific Papers

This repository contains the source code for a newly introduced knowledge graph extraction (KGE) pipeline.

The pipeline is divided into 3 parts in the form of files for performance reasons. Data is passed down among the different parts by text and Json files. 

The first part contains the paper collection step, which retrieves and preprocesses the documents from the CORD-19 dataset. The output of this phase is a txt file containing the processed text.

The second part contains the named entity recognition (NER) and entity linking (EL) phases. It takes as input the previous txt file, and outputs a json file containing the extracted entities.

The third and final part is the relation extraction (RE) and KG construction steps. This phase takes as input the txt file from the first step and the json file from the second part. This step generates the final xml file representing the final KG in an RDF format.

Considering that the input files and the training datasets are provided, the files are executed by running the cells sequentially (“run all” in the command panel). 
