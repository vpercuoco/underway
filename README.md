# Underway processing

Underway trackline data must be processed and converted to MGD77T format (not MGD77) before being sent to NCEI for archival. The content of this repository include an example Jupyter Notebook ("processing_underway_data") which shows steps for processing bathymetric data in seg-y file format and towed magnetometer data in .XYZ file format.

The original seg-y files used by this notebook are not included due to their size. They can be found on \\\\PACIFIC\Data1 in the appropriate subfolder. The representative csv files are included.

For each trackline type there must be one header file. The header file uses the extension ".h77t". Measurement files use the extension ".m77t". The main difference between bathymetric and magnetic header files are the measurement columns that are specific to the individual measurement types, and the navigational data (datetime/latitude/longitude) will likely differ depending on the transects on which they were measured and measurement sampling rates. Don't expect to have exact latitude/longitude matches between the two. The cruise metadata should be the same if all the data were acquired on the same cruise. A cruise is a port-to-port journey.

In the example provided the cruise was expedition 378, given the survey_id "jr378" for bathymetric files and "jr378m" for magnetic files. The final file exports reside in the "export files" subdirectory.

Links to various additional resources are provided in the processing_underway_data.ipynb file.

