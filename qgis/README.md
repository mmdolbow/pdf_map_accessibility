# QGIS Folder
Contains:
1. example1.qgz - QGIS Project file used to create the initial PDF
2. export_options.png - screen grab of the PDF export options used to create the initial PDF
3. PDFs demonstrating accessibility options

## Untagged PDF
"region_example_untagged.pdf" is the PDF file exported directly from QGIS, with no alterations made. It can be used to test other techniques listed here.

## Tagged PDF
"region_example_tagged.pdf" is the result of tagging via the technique described in [Tagging Maps with Acrobat Professional](https://mn.gov/mnit/assets/map-tagging-acrobat-professional_tcm38-382613.pdf) (see page 3). You can see that an H1, P, and Figure tags have been created, and they are not empty. After running the accessibility checker, alt text was assigned to the map as a Figure tag. Activating Read Out Loud will read the tags for both items (the text for the H1 tag was automatically created). Read out loud should also help you spot the typo in the explanatory text box!

## See Also
The [etc folder](./etc/) contains more information about a particularly sticky issue with using the Calibri font in QGIS, and resulting "ligature" problems when converting text boxes with that font to PDFs.

# Software Versions
Contents of this folder were created with QGIS 3.10.13-A Coruña and Adobe Acrobat Pro DC Version 2022.001.20169.