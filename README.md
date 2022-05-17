# PMLR Proceedings Submissions

This repository is used for bookkeeping for [PMLR proceedings](https://proceedings.mlr.press) submissions.
We use PRs and bibfiles to collect the meta-data of your submission and assign a volume number.
Once the proceedings are ready for publication, we create [a separate repository](https://github.com/mlresearch/v151) for the proceedings containing the compiled webpages.

## Creating a new submission

To create a new proceedings submission, please follow these steps:

1. Carefully read the [PMLR Proceedings Specification](https://proceedings.mlr.press/spec.html).
1. Fork and clone this repository and create a local branch using

    ```shell
    > git checkout -b my-example-submission
    ```

1. Prepare the bib-file for your submission according to the specification. You can use [the template](https://github.com/mlresearch/pmlr-submissions/TEMPLATE.bib) provided in this repository as a starting point. It's fine if your submission is not complete yet at this point.
1. Commit and push the bib-file and create a pull request in this repository using the PR template. Do not add submissions (pdfs or supplementary material) to the PR, as these will end up in a separate repository. Please use a descriptive title for the PR.
1. Follow the instructions provided in the PR template.
