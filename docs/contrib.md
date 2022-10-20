# Contribute

To contribute your knowledge you need the following:
1. Open Researcher and Contributor ID ([ORCID](https://en.wikipedia.org/wiki/ORCID)), your unique scientific identifier. If you do not have an ORCID, register for it [here](https://orcid.org/register).
1. A GitHub account. If you do not have an account, follow these [instructions to sign up for one](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account).


This knowledge-base follows the standard GitHub
[fork and pull request, triangular workflow](https://guides.github.com/activities/forking/).

## One time setup
1. Install [git](https://git-scm.com/downloads) and [git-lfs]().
2. If you are not comfortable working with git and GitHub from the command-line, download the [GitHub Desktop](https://desktop.github.com/) application and [read the installation and configuration help](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop).
3. Fork the [IBEX Imaging Community repository](https://github.com/zivy/ibex_microscopy) and clone it to a local directory ([GitHub Desktop instructions](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/adding-and-cloning-repositories/cloning-and-forking-repositories-from-github-desktop)).
4. Add your information to the "creators" section in the .zenodo.json file.

## Adding information to the knowledge-base

### Before starting to work
Create a new local git branch based off of the `main` branch ([GitHub Desktop instructions](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/managing-branches#creating-a-branch)).

### Modifying the *publications.bib* file:
Simply add an entry to the file using the appropriate [bibtex entry type](https://www.bibtex.com/e/entry-types/).

To give credit where credit is due, we ask that you provide the complete list of authors and do not truncate it, even if it is long.

### Modifying a markdown file:
Simply edit the relevant file.

Do not edit the **reagent_resources.md** or **publications.md** files, they are automatically generated from the *reagent_resources.csv* and *publications.bib* files respectively.

### Modifying *reagent_resources.csv*:

Do not use non ASCII characters such as &trade; or &alpha; (either remove or represent using standard ASCII "alpha").

#### Adding new line:
1. Add a line to the [reagent_resources.csv](https://github.com/zivy/ibex_microscopy/blob/main/reagent_resources.csv).
2. Create corresponding supporting material sub-directory using the target_conjugate as the directory name and add a markdown file with your ORCID as the file prefix (see existing files for reference). Supporting material file has a fixed layout, given in the [supporting_template.md](supporting_material/supporting_template.md).
3. Optionally add **small** image files (jpg, png, tiff) and refer to them in the supporting material file.

#### Adding information to existing line:
---

We only accept up to 5 ORCID additions in the `Agree` or `Disagree` columns. This means that, the original contributer's work was replicated by up to 4 people from other laboratories or refuted by up to 5 people from other laboratories.

---

1. Add your ORCID to the `Agree` or `Disagree` column on the appropriate line in the reagent_resources.csv file, use a semicolon `;` to separate from the previous ones (e.g. `ORCID1; ORCID2; ORCID3`).
2. If after adding your vote:
  * The number of ORCIDs in the `Disagree` column is greater than those in the `Agree` column:
    1. Change the content of the `Result` column from "Success" to "Failure" or the other way round and swap the ORCIDs between the `Agree` and `Disagree` columns.
    2. Modify all the supporting material markdown files associated with this row, changing the `Result` and `Recommendation` sections.
3. Add a markdown file with your ORCID to the existing sub-directory. Easiest option is to copy the contents of one of the markdown files already in this directory and modify it.
4. Optionally add **small** image files (jpg, png, tiff) and refer to them in the supporting material file.

### After work is completed
After completing the work, update the public knowledge-base. This can be done using git on the command-line or using GitHub desktop:
1. Commit the changes ([GitHub Desktop instructions](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/committing-and-reviewing-changes-to-your-project)).
2. Push the commit to GitHub ([GitHub Desktop instructions](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/pushing-changes-to-github)).
3. Create a pull-request on GitHub ([GitHub Desktop instructions](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/working-with-your-remote-repository-on-github-or-github-enterprise/creating-an-issue-or-pull-request#creating-a-pull-request)).
