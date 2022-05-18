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

   ```shell
   > git add example22.bib
   ```

1. Commit and push the bib-file and [create a pull request](https://github.com/mlresearch/pmlr-submissions/compare) in this repository using the PR template. Do not add submissions (pdfs or supplementary material) to the PR, as these will end up in a separate repository. Please use a descriptive title for the PR.

   ```shell
   > git commit -m "Add example22 proceedings"
   > git push -u origin my-example-submission
   ```

1. Follow the instructions provided in the PR template.

## Hints for Debugging your Bibfile

If the validation job fails, our tooling was not able to correctly parse your bibfile according to the specification.
You can check the output of the job for some pointers as to where parsing failed, but the errors provided are not the best.
Here is a list of things to check:

1. Is there no information from the bibfile in the logs?
   - Is the bibfile present?
   - Does it have the correct name?
   - Are there fundamental syntax-errors in the file?
1. Does the error show info from the main `@Proceedings`-entry?
   - Are there fields missing?
   - Does the bibfile have both a `volume` and `published` entry, even if it has not yet been set correctly by the editors?
   - Are there syntax errors?
1. Does the script print short-names of specific publications?
   - Is there an error around the last short-name that has been printed?
