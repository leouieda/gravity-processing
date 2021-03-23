# Gravimetry processing computational report

This report is a summative assessment for ground-based gravity processing. It
is designed to test if students are able to repeat the processing steps on a
different dataset under slightly different conditions: there are more surveys
and surveys are tied to different base stations. The location of the surveys is
also different, providing an opportunity for assessing their interpretation.

## General background

The [Bushveld Igneous Complex](https://en.wikipedia.org/wiki/Bushveld_Igneous_Complex)
in South Africa is a large layered igneous intrusion.
It is an important economic resource and a source of platinum, vanadium, iron,
chromium, uranium, and more.
Recently, the intrusions are also being considered as a key geothermal resource
due to their high heat production (Dhansay et al., 2017).
To further study the Bushveld, a series of ground gravity surveys have been
commissioned covering a majority of the complex.
Gravity data can provide crucial information about the shape and possible
vertical extent of the intrusions, as well as the crustal structure as a whole.

## Instructions

Your job is to:

1. Process the raw gravimeter readings into absolute gravity.
1. Produce a map of the residual topography-free (Bouguer) gravity disturbance
   for the entire area.
1. Provide a brief initial interpretation of the map of residuals by comparing
   with the known surface geology.

You will deliver a computational report (Jupyter notebook) that contains:

* All of the code required to go from the raw data to the map of the residual
  disturbance.
* Headings and subheadings to separate different sections.
* Text **briefly** explaining the logic behind each processing step (what the
  code does and why). One or two sentences per processing step should be enough
  for this.
* Figures (5 maximum) with the intermediate results of your processing (raw
  gravity, normal gravity, regional, etc).
* Pseudo-color map of the residual Bouguer gravity.
* Brief interpretation of the residual field (500 words maximum).
* List of any references cited for the interpretation/background (use any style
  you like, as long as you're consistent).

**Your submission should be a single Jupyter notebook (`.ipynb` file)**
containing all of the above, not a PDF/HTML/DOC file.

The report should look very similar to the notebooks we used for the practicals
(use them for inspiration but **do not** copy text straight out of them).

## Data

All data required is in the following zip archive:
[bushveld-surveys.zip](https://github.com/leouieda/gravity-processing/raw/22809b794e95982ca92f762d367843251afc8086/data/bushveld-surveys.zip)

It contains:

* CSV (comma separated value) files with the relative readings for each day of the survey.
* A CSV file with the gravimeter scaling table used to convert readings to mGal.
* A CSV file with the absolute gravity measurements at each of the base stations.
* A README file with information about the surveys, data files, datum for coordinates, etc.

Each survey starts and ends at the same base station but different surveys are
tied to different base stations. You'll know which base station a survey used
by looking at the station ID number at the beginning and end of the survey
data.

## Tips and pitfalls to avoid

* Backup your notebooks, data, and report!
* Start by processing only a single survey. When you have that working, then
  try using a `for` loop to process all surveys.
* Don't put functions/code in separate files. Keep everything within the notebook.
* Use the "Restart and run all cells" command in the "Kernel" menu to make sure
  your notebook runs correctly. This is what I'll be doing to check your
  submissions.
* Put the text explaining a processing step before/after each step, not all
  together in a single place.
* Add axis labels, titles, colorbars (with labels), to your figures.
* Make sure the figures are legible and of an appropriate size.
* Double check that your code runs from top to bottom (use "Restart and run
  all") before handing in your report.
* Use meaningful variables names (`elevation` instead of `h`).
* If you get an error, **read the error message** to find out what went wrong.
  Include the full error when asking a question.
* If your code doesn't seem to work, **don't change the code until you know
  why** this happened and what you can do to fix it. Randomly changing the code
  and hoping it will work is a great way to waste your time.
* Google search is your best friend. Answers from StackOverflow are generally
  good sources of information.
* Read the marking rubric to make sure you fulfill all of the necessary
  requirements.

## References

Dhansay, T., Musekiwa, C., Ntholi, T., Chevallier, L., et al. (2017) South
Africa's geothermal energy hotspots inferred from subsurface temperature and
geology. South African Journal of Science. 113 (11/12).
doi:[10.17159/sajs.2017/20170092](https://doi.org/10.17159/sajs.2017/20170092)
