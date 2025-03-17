# QGIS Folder
Contains:
1. example1.qgz - QGIS Project file used to create the initial PDF. Note that for the latest iteration, Metadata (Title, Author, and Language) was set in the Project Properties, so that it could be included at export.
2. export_options.png - screen grab of the PDF export options used to create the initial PDF
3. PDFs demonstrating accessibility options

## Untagged PDF
"region_example_untagged.pdf" is the PDF file exported directly from QGIS, with no alterations made, using the ![export options shown](export_options.PNG). It can be used to test other techniques listed here.

## Tagged PDF
"region_example_tagged.pdf" is the result of tagging via the technique described in [Tagging Maps with Acrobat Professional](https://mn.gov/mnit/assets/map-tagging-acrobat-professional_tcm38-382613.pdf) (see page 3). You can see that an H1, P, and Figure tags have been created, and they are not empty. After running the accessibility checker, alt text was assigned to the map as a Figure tag. Elements were reorderd to be top-to-bottom using the "Order Panel".

Activating Read Out Loud will read the tags for both items (the text for the H1 tag was automatically created). Read out loud should also help you spot the typo in the explanatory text box!

### Fixes after Accessibility Check
["region_example_tagged_passed.pdf"](region_example_tagged_passed.pdf) is the result of the following actions after running the Accessibility Check:
- Under "Document":
    - right-click "Tagged PDF - Failed", and choose "Fix".
    - right-click "Primary language - Failed", and choose "Fix". English is likely the default in the resulting popup.
    - right-click "Title - Failed", and choose "Fix". It should automatically use the title from the QGIS project's metadata.
- Under "Page Content":
    - right-click "Tab order - Failed", and choose "Fix". Click OK in the popup.
Save the document, and outside of items requiring manual checks, the Accessibility Check passes the document.

## See Also
The [etc folder](./etc/) contains more information about a particularly sticky issue with using the Calibri font in QGIS, and resulting "ligature" problems when converting text boxes with that font to PDFs. This work has not been re-tested with QGIS 3.40.3-Bratislava, but ligatures with Calibri appear to still be a problem.

# Software Versions
Contents of this folder were created with QGIS 3.40.3-Bratislava and Adobe Acrobat Pro DC Version 2024.005.20399.