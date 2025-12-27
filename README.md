# Penetration in gram-negative bacteria

The model uses the data used to create the Entry rules (Richter et al, 2017) to predict the probability that a molecule permeates across gram-negative membranes. The classifier has been trained using the classification from the original publication into Accumulation class High (Active, or 1) and Low (Inactive, or 0). After cleaning and combining the different datasets, we have 280 molecules of which 107 are labelled as high accumulators in E.coli.



## Information
### Identifiers
- **Ersilia Identifier:** `eos4r1g`
- **Slug:** `entry-classifier`

### Domain
- **Task:** `Annotation`
- **Subtask:** `Activity prediction`
- **Biomedical Area:** `Antimicrobial resistance`
- **Target Organism:** `Escherichia coli`
- **Tags:** `E.coli`, `ESKAPE`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `1`
- **Output Consistency:** `Fixed`
- **Interpretation:** Probability of entering gram negative bacteria

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| entry_proba | float | high | Probability of entering inside gram-negative bacteria |


### Source and Deployment
- **Source:** `Local`
- **Source Type:** `Internal`

### Resource Consumption


### References
- **Source Code**: [https://github.com/HergenrotherLab/GramNegAccum](https://github.com/HergenrotherLab/GramNegAccum)
- **Publication**: [https://www.nature.com/articles/nature22308](https://www.nature.com/articles/nature22308)
- **Publication Type:** `Peer reviewed`
- **Publication Year:** `2017`
- **Ersilia Contributor:** [GemmaTuron](https://github.com/GemmaTuron)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [GPL-3.0-or-later](LICENSE) license.

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
