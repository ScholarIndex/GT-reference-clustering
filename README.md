# Ground truth data for bibliographic reference clustering

This repository contains a small dataset of ground truth data to evaluate reference clustering algorithms. It consists of pairs of references (`ref`, `seed_ref`), with a ground truth value (`same-bibl-entity`) indicating whether the two references in the pair are referring to the same bibliographic entity or not (`1` = true, `0` = false, `0.5` = partly). 

These reference pairs were sampled from all clusters of LB references, trying to represent clusters of different sizes. The cluster size can be derived from values in the column `cluster_file` as it is coded in the integer preceding the `_` character.

The dataset is contained in the file `data/dataset.tsv`, obtained by concatenating (and filtering columns) the `.tsv` files in `data/partials/*.tsv` (see [notebook](./concatenate-csv-partials.ipynb)).

Some stats:
- total number of reference pairs: 3638
- number of positive ref. pairs (`same-bibl-entity` == 1): 749
- number of negative ref. pairs (`same-bibl-entity` == 0): 2886
- number of partly positive ref. pairs (`same-bibl-entity` == 0.5): 3 

## Credits

The dataset was manually corrected by Silvia Ferronato in the context of the SNF-funded [LinkedBooks project](https://p3.snf.ch/project-159961). It was created for the evaluation of the clustering algorithm by [Tao Sun](https://github.com/TaoSunVoyage), carried out in the context of his semester project student at DHLAB EPFL (see [project report](https://github.com/TaoSunVoyage/Semester-Project-References-Disambiguation/blob/master/materials/report.pdf)).