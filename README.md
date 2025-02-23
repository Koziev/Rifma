# RIFMA: A Dataset for Russian Poetry with Accentuation Annotations

The `RIFMA` dataset consists of approximately [3598](poetry_aligner_tests.md) fragments of Russian-language poems (stanzas and poems)
with stress marks and a rhyme scheme information. Fragments are taken from poems of different genres,
forms and authored by different poets, to ensure the widest possible coverage.

This dataset is a supplementary material for our paper [Automated Evaluation of Meter and Rhyme in Russian Generative Poetry](link).
The initial purpose of this dataset was to automatically check the correctness of the Russian Poetry Scansion Tool library.
Then it turned out that there are no similar datasets for the Russian language,
and we decided to publish it under an open license for the NLP community.


### Structure of dataset

The dataset is a list of tuples each containing the following fields:

`poem_text` - the poem plain text.  

`accentuation_markup` - the poem text with accentuation using \u0301 for primary stress positions and \u0302 for secondary ones.  

`rhyme_scheme` - rhyme sceme information. `null` if not assigned, `ABAB` for the case when the first line
rhymes with the third, and the second with the fourth, and so on.  


### Statistics

Some information is presented in [automatically generated report file](poetry_aligner_tests.md).

