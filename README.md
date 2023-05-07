## Humset toponym annotations
Humanitarian document excerpts annotated with location tags.
### Overview
The dataset includes 467 excerpts from humanitarian documents annotated with location tags. Documents are chosen among the ones used to build the HumSet dataset (Fekih *et al.*, [2022](https://aclanthology.org/2022.findings-emnlp.321/)), spanning 33 different project countries.
Documents are selected from different sources, ranging from official reports by humanitarian organizations to international and national media articles.
Only English documents are included in this datasets. Longer documents are truncated at first 4000 characters.
Location annotations are performed using 2 tags, according to the general distinction described in Gritta *et al., [2019](https://link.springer.com/article/10.1007/s10579-019-09475-3)*:

- **LOC** (location) - proper physical location (e.g. "Bob went to *UK* with his family")
- **AST** (associative) - generic reference to some location related meaning (e.g. "*UK* government passed a new law") 

Annotation were performed by expert analysts in the humanitarian field

### Description
The file `toponym_annotations.json` contains the following fields:
- *lead_id*: reference to the document id in the HumSet database
- *source*: url of the original document
- *text*: text extracted from the original document (first 4000 chars)
- *annotations*: locations annotations with the labels **LOC** and **AST**. This field contains the text of the annotation (*text*), offset references in the document text (*start*, *end*) and type of the annotation (*label*)

### Languages
The dataset contains English documents

### Annotation process
The annotations are performed by expert analysts in the humanitarian field

## Geocoding annotations
### Overview
the dataset includes 561 unique document/toponym pairs from 39 documents among the HumSet database, annotated with corresponding geonames id (https://www.geonames.org/). There are 474 pairs having non-empty matches, spanning 78 countries.

### Description
The file `geocoding_annotations.csv` contains the following fields:
- *lead_id*: reference to the document id in the HumSet database
- *toponym*: the location entity extracted in the document. Not all entities extracted are correct toponyms 
- *match*: longest toponym substring matching some results in geonames. Each toponym can have none, one or multiple matches with geonames (e.g. "central america" matches "central" and "america", but not "central america")
- *geonameid*: id in geonames. It can take different values:
  - None (empty): there is no correct match fot the toponym extracted in geonames.
  - -1: The extracted entity is not a toponym, therefore should not be tagged
  - geonameid (int): geonameid in the geonames database

### Annotation process
The annotations are performed by the author of the repository

## Curators
The dataset is maintained by Enrico Belliardo - enrico.m.belliardo@gmail.com

