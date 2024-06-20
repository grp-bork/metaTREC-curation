# metaTREC-curation

1. Open Excel spreadsheet.
2. Check identified values and fix wrong ones.
3. Save and close the spreadsheet.

More details:
-------------

1. Open the file in your favourite Excel spreadsheets editor (Excel, LibreOffice, Google sheets, ...)
	* If you use Excel, you can benefit from multiple choice options for individual cells. However, it is up to discussion if this is even useful (often can actually slow down the process).
2. Edit 'Extracted content' column such that the values correspond to the reference pictures. NEVER change the 'Variable name' column.
3. Pay special attention to fields such as site ID name and number, station number, transect and sample. These are used to properly identify particular sites and spots within them.
4. Check alignment - there are cases when alignment of scanned logsheet to the template was not successful. You can spot this immediately. Such a case needs to be documented, the alignment needs to be done manually, and then extraction is run again.
5. Details in individual types of cells:
	* Barcodes [integer values] - these are rarely wrong. If so, it is usually visually obvious (way too long number, some extra content, multiline values). If barcode is not present, the cell needs to be empty.
	* Checkboxes [boolean values] - success rate depends a lot on the type of checkmark used. Typically checkmarks with most of pixels in the center of checkbox (a large dot) work the best. The success rate goes rapidely down with decreasing size of the dot and with usage of other symbols.
	* In general, numerical fields should contain only numbers (plus a decimal dot, never a comma!). Units are always printed on the logsheet or default is used, so remove them completely from the cells. If a different unit was really used, a conversion needs to be done here.
	* GPS coordinates - there are various ways implemented for capturing GPS coordinates: Degrees Decimal Minutes (e.g. "E 56 22.323" for LSI), Degrees Minutes Seconds (e.g. "W 102 12 54" for plankton), and Decimal Degrees (e.g. "-57.15376" for Tara). For each type there are respective cells in the spreadsheet - direction ('N', 'S', 'E', 'W', '+', or '-'), degrees (an integer), and minutes (can be decimal number or integer). If the direction is empty, default is used ('N', 'E', '+').
	* Free text areas - the most crutual ones are used for site names and GPS direction. Otherwise, these are mostly operator names and comments.
	* Multiline values - on some logsheets, multiple numerical values are written under each other. In other rare cases, multiple barcodes are fit (kind of) into single dedicated box. In all these cases, remove the newlines from the cell and separate the values with a comma.
6. Other tips
    * Crosscheck within site - consistency within a site can help us detect outlier values. For example, if all logsheets for the same site are done on a certain day and one of them is off, it's probably a typo. 
