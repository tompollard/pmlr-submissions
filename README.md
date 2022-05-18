# PMLR Proceedings Submissions
![PMLR](./logo-pmlr.svg)

This repository is used for bookkeeping for [PMLR proceedings](https://proceedings.mlr.press) submissions.
We use PRs and bibfiles to collect the meta-data of your submission and assign a volume number.
Once the proceedings are ready for publication, we create [a separate repository](https://github.com/mlresearch/v151) for the proceedings containing the compiled webpages.

## The Submission Workflow

We handle PMLR submissions and publication via the @mlresearch Github organization.

1. This repository is the first point of contact and we handle communication [via pull requests](https://github.com/mlresearch/pmlr-submissions#creating-a-new-submission=).
1. Once your submission has been finalized, we will create a repository ([example](https://github.com/mlresearch/v151)) containing your proceedings which will then be published on [the PMLR website](https://proceedings.mlr.press/pmlr.html).
1. You can find your submission via the volume number:
    * Repo: [`https://github.com/mlresearch/v<VOLUME>`](https://github.com/mlresearch/v151)
    * Website: [`https://proceedings.mlr.press/v<VOLUME>/`](https://proceedings.mlr.press/v151/)

## Creating a new Submission

To create a new proceedings submission, please follow these steps:

1. Carefully read the [PMLR Proceedings Specification](https://proceedings.mlr.press/spec.html).
1. [Fork and clone](https://docs.github.com/en/get-started/quickstart/fork-a-repo) this repository and [create a local branch](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository) using

   ```shell
   > git checkout -b my-example-submission
   ```

1. Prepare the bib-file for your submission according to the specification. You can use [the template](https://github.com/mlresearch/pmlr-submissions/TEMPLATE.bib) provided in this repository as a starting point. It's fine if your submission is not complete yet at this point.

   ```shell
   > git add example22.bib
   ```

1. Commit and push the bib-file and [create a pull request (PR)](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) in [this repository](https://github.com/mlresearch/pmlr-submissions/compare) which will automatically use the PR template. Do not add the submissions (pdfs or supplementary material) to the PR, as these will end up in a separate repository. Please use a descriptive title for the PR.

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
