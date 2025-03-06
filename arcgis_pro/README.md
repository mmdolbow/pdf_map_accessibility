# ArcGIS Pro Folder
Contains:
1. Example Project (.aprx file)
2. Three PDFs demonstrating accessibility issues (details below)
3. Screen grab of export options used within ArcGIS Pro

## ArcGIS Pro Actions
Note that in an attempt to increase accessibility in our output, we took the following actions in Pro after upgrading to 3.x:
1. Reordered the Drawing Order so that the Title was at the top of the order in the layout. (Second is the explanatory text, last is the map.)
2. In the Map Frame Properties, under "Accessibility", we set Alt Text to "Map of regions in Minnesota" within the "example_altText.aprx" file.

**WARNING !!** We encountered a situation where we did **not** take step 2 in Pro, and then we were **not** be given the opportunity to set Alt Text in Acrobat! In fact, the document  "passed" the Accessibility Check with respect to alt text, but there won't be any! Since we couldn't replicate this issue, we think it is because our initial export came before officially saving the project file as a 3.x version. **So be sure to "save up" your document before continuing!**

## Initial Export PDF
"region_example_initial.pdf" is the file that is created when exporting the Layout in ArcGIS Pro as a PDF. Most default options are left (see export_options.PNG) except:
1. Image compression set to "JPEG" instead of "JPEG2000"
2. The georeferencing option is unchecked
3. "Layers and attributes" are set to "None". 

This PDF is considerably better than results using 2.x. Assigning alt text is still manual; nothing is automatically created. But the document has some initial tags, they have contents, and if you activate "Read Out Loud", you will hear the text elements being read.

### Note on prior problems
When we tested this with ArcGIS Pro 2.6 (see archived branch), we needed the following:
1. "region_example_empty_tags.pdf" was the result of tagging the initial PDF using the technique described in [Tagging Maps with Acrobat Professional](https://mn.gov/mnit/assets/map-tagging-acrobat-professional_tcm38-382613.pdf) (see page 3).
2. "empty_tags.PNG" Showed that while tags were created for the document, they were empty. When you selected them, you saw nothing selected within the document. 

At 3.x, this problem is now resolved. We'v removed the "region_example_empty_tags.pdf" from the repo but left the "empty_tags.PNG" for reference.

## Tagged PDF
The "region_example_tagged.pdf" is the result of review and manual tagging work with Adobe Acrobat. Note:
- If you open the Accessibility Tools and the "Reading Order" panel, the title, explanatory paragraph, and map have already been tagged.
- The components appear in the order of the Drawing Order set in Pro. **Note** that if you don't take that step in Pro, "Read Out Loud" will use the original order, **even** if you manually rearrange the order in Acrobat.
- Despite being a "Title" element within Pro's layout, the title is only tagged as a paragraph element. We manually re-tagged it as a Heading 1 in Acrobat.
- After running a full "Accessibility Check", 4 issues were revealed:
  - Primary language failed - this is typical and easily remedied in Acrobat.
  - Title failed - this is also typical, but since we designated a title in the layout, it sure would be nice if this translated to the PDF. (It does not inherit the title from the layout metadta, either.) Fixed by right-clicking "Fix" in the Accessibility Checker, **un**checking "Leave As Is" in the resulting box, and entering a title.
  - Logical Reading Order needs manual check - this is typical.
  - Color contrast needs manual check - this is typical.

# Software Versions
Contents of this folder were created with ArcGIS Pro 3.3.0 and Adobe Acrobat Pro DC Version 2024.005.20399.