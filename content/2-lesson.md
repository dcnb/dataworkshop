---
title: Open Refine Step Thru
nav: Step Thru
topics: OpenRefine; Split Columns; Clean Data
---

1. Turn the KMZ file into a KML File
    - Rename the file so that it has a .zip extension
    - Open the folder it creates
    - Open the KMZ file found in that folder using Visual Studio Code
    - Copy the contents of the file
2. Open OpenRefine 
3. Click the clipboard option
    - Paste the contents of the KML file into the paste box. 
    - Click the "Next" button at the bottom.
4. Select the items you'd like to feature in the dataset
    - XML formats like KML nest items to create hierarchical/structured data
    - Find and select the content in a `<Placemark>` tag
    - Edit the project name box at the top then click "Create Project"
5. Identify and rename the columns you want to use
    - Rename the column "Placemark - Point -" to "latng"
    - Rename the column "Placemark - name -" to "title"
    - Rename the column "Placemark - description -" to "link"
6. Remove unnecessary columns
    - Click the triangle button to the left of the "All" column at the far right of the spreadsheet
    - Hover over the "Edit Columns" option then select "Re-order / remove Columns"  
    - Drag and drop all the columns we're not using (i.e. all columns except those we renamed above) to the remove box 
    - Reorder the columns by dragging title to the top and link to the bottom of the list of columns you're keeping on the left
    - Click "OK"
7. Remove unnecessary rows
    - Click the triange net to the "title" column
    - Hover over "Facet", then "Customized facets", then select "Facet by blank (null or empty string)"
    - This will create a facet option in the left hand Facet/Filter menu
    - Hover over "true" in the options presented and click the "include" link that appears
    - This will reduce your dataset just to those rows that do not include any information 
    - Click the triangle button in the All column at the far right
    - Hover over "Edit rows" then select the "Remove all matching rows" option
    - This will delete all those rows with no information
8. Split latlng column into latitude and longitude
    - Click the triangle next to the latlng column, hover over "Edit Cells" then select "Split mutli-valued cells ..."
    - "by separator" will be selected and the "Separator" will be a comma. That's what you want! Click "Ok"
    - Rename column latlng 1 to longitude
    - Rename column latlng 2 to latitude
9. Edit the link column down so that it's just a link.
    - Copy this string: `<p><a target=\"_blank\" href=\"http://www.firelookout.com/id/` from any cell in the link column
    - Click the triangle next to the "link" column
    - Hover over "Edit Cells" then select "Replace" at the bottom.
    - Paste the string you copied into the "Find" box
    - Leave the "Replace" box blank
    - Click "Ok"
    - Now repeat the find/replace process above by finding and replacing this string: `</a></p>`
10. Split the link column
    - Click the triangle next to the "link" column, hover over "Edit Cells" then select "Split mutli-valued cells ..."
    - "by separator" will be selected and the "Separator" will be a comma. Edit that to be `">"` then click "Ok"
    - Rename column Link 1 to page
    - Rename column Link 2 to url


{% capture text %}
If you'd like to see all these steps in an Open Refine project, download the project file by right clicking this link --> [idaho-standing-fire-towers.openrefine.tar.gz](/idaho-standing-fire-towers.openrefine.tar.gz) and pressing 'Save As'

Then, in OpenRefine, select "Import Project" at the OpenRefine start page and add the project file by selecting the "Browse ..." button and finding the downloaded file. 
{% endcapture %}
{% include card.html text=text header="Project File for Open Refine" %}







