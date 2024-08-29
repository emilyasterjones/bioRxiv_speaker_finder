# BioRxiv Speaker Finder [![DOI](https://zenodo.org/badge/288616848.svg)](https://zenodo.org/doi/10.5281/zenodo.13512465)
This iPython notebook extracts first and last authors who have published bioRxiv preprints or Pubmed manuscripts relevant to an inputted subject area. You can use it to find researchers outside of your network to invite them as a speaker or cite their work.

**March 2023 update**: [Rxvist](https://rxivist.org/), the API required for bioRxiv search portion of this tool, has shut down. The remaining [bioRxiv API](https://api.biorxiv.org/) doesn't have keyword search functions. The Pubmed search portion still works.

**Inputs:** keyword (in title or abstract) & whether you are looking for trainees (first authors) or PIs (last authors)

**Outputs:** Printed data frame & CSV with a list of authors who have published manuscripts containing all keywords, with the following attributes:
* institution
* email
* ORCID link
* \# manuscripts with provided keywords
* source (bioRxiv or Pubmed)
* \# total preprints
* \# total downloads
* \# total works (from ORCID).

Lists are sorted in order of # of keyword manuscripts so the most relevant authors will be at the top.

**Optional:** code cells at the end use APIs to predict the gender & ethnicity of the authors. Predicted female & minority authors are printed and the predictions are appended as columns to the CSV.  
If you use these cells, please read the important caveats at the top of the notebook and treat these predictions with caution.

If you use this tool, please cite the original paper which created the Rxivist API:  
*Abdill RJ, Blekhman R. "Tracking the popularity and outcomes of all bioRxiv preprints." eLife (2019). doi: 10.7554/eLife.45133.*

# Citation Overrepresentation Tool
This second iPython notebook identifies overrepresented authors, journals, & institutions from a citation list.

**Inputs:** .bib file extracted from a paper

**Outputs:** prints sorted list most-cited last authors, journals, & institutions (as extracted from ORCID)

# Launch both notebooks
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/emilyasterjones/bioRxiv_speaker_finder/master)



