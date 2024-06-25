# Excel spreadsheets curation

1. Open the file in your favourite Excel spreadsheet editor (Excel, LibreOffice, Google Sheets, ...)
2. Edit the `Extracted content` column such that the values correspond to the reference pictures. NEVER change the `Variable name` column.
  * Crosscheck within site. Sometimes, a value might correspond to the picture, but it doesn't make sense in the context of the site.
  * Consistency within a site can help us detect outlier values. For example, if all logsheets for the same site are done on a certain day and one of them is off, it's probably a typo.
  * Correct these values regardless of what is written in the picture.
4. Pay special attention to fields such as site ID name and number, station number, transect and sample. These are used to identify particular sites and spots within them properly.
5. Check alignment - there are cases when the alignment of the scanned logsheet with the template was not successful. You can spot this immediately. Such a case needs to be documented, the alignment needs to be done manually, and then extraction is run again.
  * This should not happen anymore, but there might be some exceptions.
6. Details in individual types of cells:
	* Barcodes [integer values] - these are rarely wrong. If so, it is usually visually obvious (way too long number, some extra content, multiline values). If the barcode is not present, the cell needs to be empty.
	* Checkboxes [boolean values] - success rate depends a lot on the type of checkmark used. Typically, checkmarks with most of the pixels in the centre of the checkbox (a large dot) work the best. The success rate goes rapidly down with the decreasing size of the dot and with the usage of other symbols.
	* In general, numerical fields should contain only numbers (plus a decimal dot, never a comma!). Units are always printed on the logsheet or default is used, so remove them completely from the cells. If a different unit was really used, a conversion needs to be done here.
	* GPS coordinates - there are various ways implemented for capturing GPS coordinates: Degrees Decimal Minutes (e.g. "E 56 22.323" for LSI), Degrees Minutes Seconds (e.g. "W 102 12 54" for plankton), and Decimal Degrees (e.g. "-57.15376" for Tara). For each type, there are respective cells in the spreadsheet - direction ('N', 'S', 'E', 'W', '+', or '-'), degrees (an integer), and minutes (can be decimal number or integer). If the direction is empty, default is used ('N', 'E', '+').
	* Free text areas - the most crucial ones are used for site names and GPS directions. Otherwise, these are mostly operator names and comments.
	* Multiline values - on some logsheets, multiple numerical values are written under each other. In other rare cases, multiple barcodes are fit (kind of) into a single dedicated box. In all these cases, remove the newlines from the cell and separate the values with a comma.
7. Inspect the scanned logsheet - usually, it is not necessary to open the logsheet itself. But sometimes, you can notice there is something not clear in the spreadsheet, the alignment is not perfect, and some parts are not completely readable, or some text is crossed out. Then, open the logsheet and check the values manually.
