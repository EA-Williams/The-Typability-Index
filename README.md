
# The Typability Index

Quick links: [Web App](https://emily-a-williams.shinyapps.io/the-typability-index-web-app/) | [Pre-print](https://osf.io/preprints/psyarxiv/qxuv5)

---

This repo contains the R project for creating and testing The Typability Index, including scripts and generalisation data. **This project is not required to use [Web App](https://emily-a-williams.shinyapps.io/the-typability-index-web-app/)**. The accompanying paper is currently under review as of December 2024 - view the [Pre-print](https://osf.io/preprints/psyarxiv/qxuv5).

### Datasets
- **Training and Testing Dataset:** The 136M Keystrokes Dataset (Dhakal et al., 2018) must be ***downloaded manually*** (instructions below).
- **Generalisation Dataset:** Provided within this repository.

### License

This GitHub repository is licensed under CC BY-NC-SA 4.0 to comply with the stipulation of the 136M Keystrokes Dataset (Dhakal et al., 2018) of non-commercial research purposes only.

---

## Notes on the Scripts

- **Format:** Scripts are written in R Markdown but are not intended to be knitted. They are designed for execution chunk-by-chunk.
- **Outputs:** Pre-generated outputs are included in the repository. Running the scripts will overwrite these files.
- **Recommendation**: Set up the data following the three steps below, then skip the first script (`scripts/0-handle-timestamp-errors.Rmd`) . Its resultant amended datafiles are already provided, which otherwise take a long time to recreate.

---

## Ignored Files / Setting Up Correctly

Certain files are intentionally excluded from GitHub due to size or licensing constraints. To fully use this repository, you need to manually download a separate dataset. 

### 1. 136M Keystrokes Dataset

**Ignored Files:**  
`data/dhakal_files_with_replacements_for_both_issues/*_keystrokes.txt`

The Typability Index relies on the 136M Keystrokes Dataset (Dhakal et al., 2018), available at [https://userinterfaces.aalto.fi/136Mkeystrokes/](https://userinterfaces.aalto.fi/136Mkeystrokes/).  
**We do not redistribute this original dataset here.** You must manually download and amend it as described below.

Minor corrections (<6% of files) were applied to the dataset for parsing and timestamp errors (details in Appendix 2 of our associated paper).  
This repository includes only the amended files (67 manually fixed + 10,098 programmatically fixed). **Rights remain with Dhakal et al. (2018); usage must comply with their original licence.**

#### Steps to Configure the Dataset
1. **Download**: Obtain the original dataset from the website above.
2. **Organise**: Place the participant keystroke `.txt` files directly in `data/dhakal_files_with_replacements_for_both_issues/` (no intermediate subfolders).
3. **Apply Amendments**:
   - Copy files from `data/fixed_parsing_issues/` and paste into `data/dhakal_files_with_replacements_for_both_issues/` to overwrite 67 files with parsing fixes.
   - Copy files from `data/fixed_timestamp_error_codes/` into the same directory to overwrite 10,098 files with timestamp fixes. (Alternatively, you can regenerate these amended files by running `scripts/0-handle-timestamp-errors.Rmd`.)

---

### 2. Stitched Participant Speed File

**Ignored File:**  
`output/processed_data/ptps_sents_inputs_wpms/full_ptps_sents_inputs_wpms.txt`

This file contains every participant's speed for each of their 15 sentences, and is created by concatenating 34 other txt files (each containing 5000 participants, except the final file). 
**Reason for Ignoring:** File size exceeds GitHub's 100MB limit.

#### Recreating This File
You don’t need to take any additional steps to recreate this file. It will be generated automatically when running the `readBatched` chunk in `scripts/1-calculate-typability-scores.Rmd`.

---

## Additional Notes
- All rights to the amended data remain with the original authors (Dhakal et al., 2018). See their website for licence details.
- If you encounter issues or have questions, please raise them via GitHub Issues.

---

Thank you for your interest in The Typability Index!
