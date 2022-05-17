## Description

<!--- Provide any details specific to your submission and don't hesitate to ask questions! It's fine to omit the information provided in the bib-file in the description. -->

## Checklist Organizers (you)

Go over all the following points, and put an `x` in all the boxes that apply.
If you're unsure about any of these, don't hesitate to ask. We're here to help!

- [ ] I have read the [PMLR Proceedings Specification](https://proceedings.mlr.press/spec.html).
- [ ] This PR consists of a single bib-file in the root of this repository named after my conference.
- [ ] The bib-file does not contain any errors, the tests in this PR pass.
- [ ] I have provided a link to the PDFs (and optional supplementary files).

## Checklist Editors (@mlresearch/pmlr)

- [ ] The submission has been assigned to an editor @lawrennd @mrksr
- [ ] The submission has been assigned a volume ID.
- [ ] The publication date has been set correctly.

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
