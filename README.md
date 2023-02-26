# omr
Optical music recognition - translate PDFs into MusicXML.

A model that can perform optical character recognition on music. Specifically, it should be able to read in PDFs for single-part scores, produce corresponding MusicXML, and do nothing else. Work in progress.

## Pipeline

In order for the learning steps to be effective, there should be a clearly-defined pipeline. It currently consists of the following steps:

* Pre-processing the data from PDF into a digestable, minimal format
* Training the model to convert it into another digestable, minimal format
* Post-processing the data into MusicXML

### Data preprocessing

So that the model is only being trained on necessary data, and to make the training process quicker:

* Binarisation to retain only the musical notation
* Sequencing into one dimension, i.e. converting multiple lines into one line
* Removing extraneous stave lines to separate notes
