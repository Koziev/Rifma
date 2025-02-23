# RIFMA: A Dataset for Russian Poetry with Accentuation Annotations

The `RIFMA` dataset consists of approximately [3,598](poetry_aligner_tests.md) fragments of Russian-language poems (stanzas and poems)
with stress marks and a rhyme scheme information. Fragments are taken from poems of different genres,
forms and authored by different poets, to ensure the widest possible coverage.

This dataset is a supplementary material for our paper [Automated Evaluation of Meter and Rhyme in Russian Generative Poetry](link).

This dataset was initially created to validate the [Russian Poetry Scansion Tool library](https://huggingface.co/inkoziev/RussianPoetryScansionTool).
Recognizing the lack of similar resources for Russian poetry, we have made it publicly available under an open license
to support research in natural language processing (NLP) and computational poetry analysis.


### Dataset file

[rifma_dataset.json](rifma_dataset.json)

### Structure of dataset

Each entry in the dataset is a tuple with the following fields:

`poem_text` - The poem plain text.  

`accentuation_markup` - The poem text with stress annotations. Primary stresses are marked with \u0301, and secondary stresses with \u0302.  

`rhyme_scheme` - The rhyme scheme of the poem. If not applicable, this field is null.
Common patterns include `ABAB` (where the first line rhymes with the third, and the second with the fourth).


### Statistics

Some information is presented in [automatically generated report file](poetry_aligner_tests.md).

