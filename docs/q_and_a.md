# Questions and Answers

Multiplex imaging protocols are complex, they involve a variety of technologies and deal with both physical elements and computational ones. Accurately describing all aspects of a protocol in sufficient detail to consistently obtain high quality results is a work in progress. Detailed descriptions addressing all aspects of a protocol need to span the gamut from physical sample handling to software settings used by the computational components utilized in the work.

This file contains questions and answers addressing various aspects of the IBEX imaging protocol which were not addressed in publications, or which were not sufficiently clear to scientists from their descriptions in the publications.

---

If you have a question that does not appear here, please ask on the [knowledge-base GitHub issue tracker](https://github.com/zivy/ibex_microscopy/issues). Posting to the issue tracker requires a GitHub account. If you do not have an account, please follow these [instructions to sign up for one](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account).

---

1. **Is IBEX compatible with FFPE samples?**  
  The use of IBEX on heavily fixed mouse FFPE samples using Opal-plex is shown in [[Figure 6, Radtke et al., PNAS 2020](https://doi.org/10.1073/pnas.2018488117)] and in [[Figure 4, Radtke et al., Nature Protocols 2022](https://doi.org/10.1038/s41596-021-00644-9)] for human FFPE samples using automated IBEX. Additionally, the manual IBEX method was applied to FFPE tissue sections adhered to glass slides, [[Figure S3A, Radtke et al., PNAS 2020](https://www.pnas.org/doi/suppl/10.1073/pnas.2018488117/suppl_file/pnas.2018488117.sapp.pdf)].

1. **Do I have to use the two-well chambered coverglass for my samples?**  
No. The use of sections adhered to glass slides is shown in [[Figure S3A, Radtke et al., PNAS 2022](https://www.pnas.org/doi/suppl/10.1073/pnas.2018488117/suppl_file/pnas.2018488117.sapp.pdf)]. Detailed instructions on how to section tissues onto glass coverslips for the automated IBEX configuration are given in [[Radtke et al., Nature Protocols 2022](https://doi.org/10.1038/s41596-021-00644-9)].

1. **Is LiBH4 safe to use?**  
We appreciate your concerns. IBEX has been performed hundreds of times by dozens of junior and senior investigators in the laboratory. Please follow the safety instructions describe in the [protocols](https://doi.org/10.1038/s41596-021-00644-9):  
*“Perform these steps in a chemical hood with appropriate PPE. Always work with small amounts (<10 mg) of LiBH4. Replace vial of LiBH4 after 4 weeks of prolonged use as we have observed reduced bleaching efficiency after repeated exposure to air. We recommend purchasing the smallest aliquot (1 g) available. Alternative borohydride solutions may also be considered and empirically tested for their compatibility with the fluorophores and panels described here.”*   
**Please make sure to train all members of your lab in the safe handling of all reagents used for IBEX.**

1. **When following the SimpleITK Imaris Extensions [setup instructions](https://github.com/niaid/imaris_extensions#setup) I get the following error, "CondaHTTPError: HTTP 000 CONNECTION FAILED for url...". What should I do?**  
This error is most likely due to your institution's proxy server security settings. To resolve proxy server issues, see the [instructions provided in the anaconda documentation](https://docs.anaconda.com/anaconda/user-guide/tasks/proxy/) and possibly the instructions for using [non standard certificates](https://conda.io/projects/conda/en/latest/user-guide/configuration/non-standard-certs.html).
This [stack-overflow discussion](https://stackoverflow.com/questions/33883371/python-anaconda-proxy-setup-via-condarc-file-on-windows) may also be of interest.  
Another possible solution is to install packages from PyPi using the `requirements.txt` file found in the source root directory:  
    ```
     conda create -n imaris python=3.7.0
     conda activate imaris
     pip install --upgrade pip
     pip install -r requirements.txt
    ```

1. **I am using the registration application from the [imaris extensions GitHub repository](https://github.com/niaid/imaris_extensions) and it fails. Are there settings I can change to make it work?**  
Yes, there are. For common failure modes and various settings that you can try, see the application's `Help` menu or [this web page](https://niaid.github.io/imaris_extensions/XTRegisterSameChannel.html).