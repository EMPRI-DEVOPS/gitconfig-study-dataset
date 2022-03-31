# `.gitconfig` Date Study Dataset

This dataset has been created as part of the [EMPRI-DEVOPS](https://empri-devops.de) research project
to investigate how users of Git configure the presentation of date information
(author and committer date) in Git's command line output,
as well as what date-related output filters they use.

The dataset was built from about 20,000 publicly available `.gitconfig` files
and contains all date-related configuration options that are available in Git.

We originally built the dataset for the paper "[Data Minimisation Potential for
Timestamps in Git: An Empirical Analysis of User Configurations]()" to investigate
the potential for timestamp-focused data minimisation.
We recommend our read the paper to understand the methodology of extracting
this dataset from `.gitconfig` files published on GitHub.


## Dataset Format

The dataset is provided in the JSON format and comprises a list of objects each
representing the analytics for one `.gitconfig` file.

Each analytics lists alias evaluations for:

- commands like _log_ that allow date and pretty formatting (`alias_dp`),
- commands like _blame_ that only allow date formatting (`alias_do`), and
- commands like _log that only allow since/until filtering (`alias_su`).

This is followed by an analysis of `pretty.*` settings, i.e., pretty formatting
aliases in JSON field `pretty_aliases_stats`.
Finally, The settings for `log.date` and `blame.date` are provided.
Here, any free-form date formatting string is replaced by the word _custom_.

We recommend to first look at the examples provided in `example-configs/` to
get familiar with the format.


## Citation

If you use this dataset in your research, please cite the accompanying paper:
(Currently the paper is accepted but not yet published)

> Burkert, Christian and Ansohn McDougall, Johanna and Federrath, Hannes: "Data Minimisation Potential for Timestamps in Git: An Empirical Analysis of User Configurations". To be presented at IFIP SEC 2022.
```
