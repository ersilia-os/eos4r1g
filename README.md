# Penetration in gram-negative bacteria

Estimates the probability that a compound accumulates inside Gram-negative bacteria, the barrier that keeps most antibacterial chemistry from reaching its target. Richter and colleagues measured accumulation in Escherichia coli for over 180 diverse compounds and sorted them into high and low accumulators. Ersilia cleaned and combined those datasets into 280 molecules, 107 of them high accumulators, and fitted a binary classifier with its LazyQSAR package. Accumulation was measured only in E. coli, so other Gram-negative species are an extrapolation.

This model was incorporated on 2025-12-27.Last packaged on 2026-10-19.

## Information
### Identifiers
- **Ersilia Identifier:** `eos4r1g`
- **Slug:** `entry-classifier`

### Domain
- **Task:** `Annotation`
- **Subtask:** `Activity prediction`
- **Biomedical Area:** `Antimicrobial resistance`
- **Target Organism:** `Escherichia coli`
- **Tags:** `Antimicrobial activity`, `ESKAPE`, `Permeability`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `1`
- **Output Consistency:** `Fixed`
- **Interpretation:** Rank score of accumulation inside Escherichia coli calibrated against the Ersilia reference library of 50K compounds. A score above 0.65 beats 99% of that library. Trained on 107 high accumulators against 173 low accumulators.

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| entry_rank | float | high | Rank score of the compound's predicted accumulation inside Escherichia coli. Calibrated against 50K compounds from the Ersilia reference library so that a score of 0.65 is better than 99% of them. Recommended threshold: 0.65. |


### Source and Deployment
- **Source:** `Local`
- **Source Type:** `Internal`
- **DockerHub**: [https://hub.docker.com/r/ersiliaos/eos4r1g](https://hub.docker.com/r/ersiliaos/eos4r1g)
- **Docker Architecture:** `AMD64`, `ARM64`
- **S3 Storage**: [https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos4r1g.zip](https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos4r1g.zip)

### Resource Consumption
- **Model Size (Mb):** `7`
- **Environment Size (Mb):** `7514`
- **Image Size (Mb):** `6497.4`

**Computational Performance (seconds):**
- 10 inputs: `31.53`
- 100 inputs: `25.99`
- 10000 inputs: `460.84`

### References
- **Source Code**: [https://github.com/HergenrotherLab/GramNegAccum](https://github.com/HergenrotherLab/GramNegAccum)
- **Publication**: [https://doi.org/10.1038/nature22308](https://doi.org/10.1038/nature22308)
- **Publication Type:** `Peer reviewed`
- **Publication Year:** `2017`
- **Ersilia Contributor:** [GemmaTuron](https://github.com/GemmaTuron)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [None](LICENSE) license.

**Notice**: Ersilia grants access to models _as is_, directly from the original authors, please refer to the original code repository and/or publication if you use the model in your research.


## Use
To use this model locally, you need to have the [Ersilia CLI](https://github.com/ersilia-os/ersilia) installed.
The model can be **fetched** using the following command:
```bash
# fetch model from the Ersilia Model Hub
ersilia fetch eos4r1g
```
Then, you can **serve**, **run** and **close** the model as follows:
```bash
# serve the model
ersilia serve eos4r1g
# generate an example file
ersilia example -n 3 -f my_input.csv
# run the model
ersilia run -i my_input.csv -o my_output.csv
# close the model
ersilia close
```

## About Ersilia
The [Ersilia Open Source Initiative](https://ersilia.io) is a tech non-profit organization fueling sustainable research in the Global South.
Please [cite](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff) the Ersilia Model Hub if you've found this model to be useful. Always [let us know](https://github.com/ersilia-os/ersilia/issues) if you experience any issues while trying to run it.
If you want to contribute to our mission, consider [donating](https://www.ersilia.io/donate) to Ersilia!
