# ArcGIS Pro Folder
Contains:
1. Example Project (.aprx file)
2. Three PDFs demonstrating accessibility issues (details below)
3. Screen grab of export options used within ArcGIS Pro

## Untagged PDF
"region_example_untagged.pdf" is the file that is created when exporting the Layout in ArcGIS Pro as a PDF. Most default options are left except the georeferencing option is unchecked. (see export_options.PNG) Layers are not exported. You can use this PDF to test tagging capabilities as described below and see if you get the same results.

## Empty Tag PDF
"region_example_empty_tags.pdf" is the result of tagging the initial PDF using the technique described in [Tagging Maps with Acrobat Professional](https://mn.gov/mnit/assets/map-tagging-acrobat-professional_tcm38-382613.pdf) (see page 3). You can see that while tags are created for the document, they are empty and when you select them, you see nothing selected within the document. Assigning alt text is completely manual; nothing is automatically created. If you activate "Read Out Loud", you will hear "Warning: Empty Page".

## Tagged PDF
"region_example_tagged.pdf" is the result of tagging via an alternative method:
1. Run the full Accessibility Checker
2. Manually fix elements that come out as problems
You can see that the resulting "<Figure>" tag is not empty, and has alt text assigned. This text is read with "Read Out Loud". However, if you attempt to create additional tagged content with the "Reading Order" panel, it will _break the existing tag_ and create new empty tags just like the Empty Tag PDF.

# Software Versions
Contents of this folder were created with ArcGIS Pro 2.5 and Adobe Acrobat Pro DC Version 2019.021.20061.