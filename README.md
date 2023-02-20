# omr
Optical music recognition - translate PDFs into MusicXML.

A model that can perform optical character recognition on music. Specifically, it should be able to read in PDFs, produce corresponding MusicXML, and do nothing else. Work in progress.

## Pipeline

In order for the learning steps to be effective, there should be a clearly-defined pipeline. It currently consists of the following steps:

* Pre-processing the data from PDF into a digestable, minimal format
* Training the model to convert it into another digestable, minimal format
* Post-processing the data into MusicXML
