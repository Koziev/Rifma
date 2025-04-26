# RIFMA: A Dataset of Russian Poetry with Accentuation Annotations

The `RIFMA` dataset consists of [3,834](poetry_aligner_tests.md) samples of Russian-language poems (stanzas and whole poems)
with stress marks and a rhyme scheme information. Fragments are taken from poems of different genres,
forms and authored by different poets, to ensure the widest possible coverage.

An example of poem accentuation is as follows:

```
За́йку бро́сила хозя́йка —
Под дождё́м оста́лся за́йка.
Со скаме́йки сле́зть не мо́г,
Ве́сь до ни́точки промо́к.
```

This dataset is a supplementary material for our paper [Automated Evaluation of Meter and Rhyme in Russian Generative Poetry](https://arxiv.org/abs/2502.20931).

This dataset was initially created to validate the [Russian Poetry Scansion Tool](https://github.com/Koziev/RussianPoetryScansionTool).
Recognizing the lack of similar resources for Russian poetry, we have made it publicly available under an open license
to support research in natural language processing (NLP) and computational poetry analysis.


### Dataset file

[rifma_dataset.json](rifma_dataset.json)


### Structure of dataset

Each entry in the dataset is a tuple with the following fields:

`poem_text` - The poem plain text.  

`accentuation_markup` - The poem text with stress annotations. Primary stresses are marked with `\u0301`, and secondary stresses with `\u0302`, as in example: `И сло̀вони́тью сде́лайте окно́`.

`rhyme_scheme` - The rhyme scheme of the poem. If not applicable, this field is null.
Common patterns include `ABAB` (where the first line rhymes with the third, and the second with the fourth).


### Rhyme Scheme Format

When using this poetry dataset, please note our unique rhyme scheme encoding approach:

- **Non-rhyming lines** are marked with hyphens (`-`) rather than unique letters  

#### Examples:

| Conventional | Our Notation |
|--------------|--------------|
| `ABCA`       | `A--A`       |
| `ABAC`       | `A-A-`       |
| `AABB`       | `AABB`       |


### Statistics

Some information is presented in [automatically generated report file](poetry_aligner_tests.md).


### Content Note

This dataset intentionally includes:

- Non-professional poetry
- Meter deviations
- Grammatical errors
- Other imperfections

Its purpose is to test poetry analysis tools under realistic conditions, including edge cases and defects.


### Additional Resources

[Ars Poetica](https://huggingface.co/datasets/inkoziev/ArsPoetica) is a dataset comprising Russian-language syllabo-tonic poetry with stress placement performed by [Russian Poetry Scansion Tool](https://github.com/Koziev/RussianPoetryScansionTool).


### Citation

If you use this dataset in your research or projects, please cite it as follows:

```
@misc{koziev2025automatedevaluationmeterrhyme,
      title={Automated Evaluation of Meter and Rhyme in Russian Generative and Human-Authored Poetry},
      author={Ilya Koziev},
      year={2025},
      eprint={2502.20931},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2502.20931},
}
```
[DOI: 10.5281/zenodo.15202823](https://doi.org/10.5281/zenodo.15202823)
