# lost-scope
XML project form for Wildlife Acoustics Kaleidoscope
Overview
This project is a customized Wildlife Acoustics Kaleidoscope XML Project designed to output results in a CSV format compatible with the EcoBat proforma, while remaining fully re-openable in Kaleidoscope for further review or adjustments.

Kaleidoscope is primarily used for bat call analysis and auto-identification. EcoBat requires a specific CSV format to upload call data for acoustic activity analysis. This project bridges the two formats.

Goals
EcoBat Proforma Compatibility: Outputs a CSV that adheres to the column structure required by EcoBat (e.g., including recordingID, species, date, time, location, etc.).

Kaleidoscope Compatibility: The .kproj file can be reopened in Kaleidoscope without breaking project metadata or analysis capabilities.

Non-destructive Workflow: XML structure retains original paths, classifiers, and analysis parameters.

How It Works
The Project.kproj (XML file) is configured to:

Use custom fields in the output CSV to match EcoBat's required columns.

Include additional metadata (e.g., Site, GridRef, SurveyID, Method) if required by EcoBat.

Maintain a valid internal XML structure for compatibility with Kaleidoscope v5+.

The CSV export should be triggered via:

Kaleidoscope’s File > Export Table as CSV function

OR via an automated post-processing script that maps Kaleidoscope’s standard output to the EcoBat format.

Ensure the following fields are present in your CSV output:

Field	Source in Kaleidoscope
recordingID	Filename (without path)
species	Species label from auto-ID
date	Extracted from file or metadata
time	Extracted from file or metadata
location	Custom tag or extracted value
SurveyID	Custom field or folder-based
GridRef	Optional: added manually or via GPS
Method	Optional: survey method metadata

Reopening in Kaleidoscope
You can open Project.kproj in Kaleidoscope as usual:

Open Kaleidoscope.

Use File > Open Project and select Project.kproj.

All tags, settings, and file paths will remain intact.

CSV output can be regenerated at any time.

⚠️ Limitations
This setup assumes consistent file naming and date/time metadata in WAV files.

Some EcoBat fields may not be automatically populated without a supplementary script or manual entry.

GPS metadata requires embedded geotags or a linked GPS log.

📬 Questions?
For help with modifying or maintaining this integration, contact the original editor or consult:

Wildlife Acoustics Support

EcoBat Documentation
