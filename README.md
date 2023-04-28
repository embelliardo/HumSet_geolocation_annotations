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
The file `annotated_dataset.json` contains the following fields:
- *lead_id*: reference to the document id in the HumSet database
- *source*: url of the original document
- *text*: text extracted from the original document (first 4000 chars)
- *annotations*: locations annotations with the labels **LOC** and **AST**. This field contains the text of the annotation (*text*), offset references in the document text (*start*, *end*) and type of the annotation (*label*)

### Languages
The dataset contains English documents

### Annotation process
The annotations are performed by expert analysts in the humanitarian field

### Curators
The dataset is maintained by Enrico Belliardo - enrico.m.belliardo@gmail.com

