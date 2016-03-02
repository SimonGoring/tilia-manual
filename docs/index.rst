.. tilia_manual documentation master file, created by
   sphinx-quickstart on Tue Mar  1 11:11:33 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Tilia Documentation
========================================

Contents:

.. toctree::
   :maxdepth: 2



Indices and tables
========================================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

Acknowledgements
========================================
This documentation would not be possible without the extrordinary work of Eric C. Grimm who has spent countless hours developing the Tilia platform.  The documentation here makes use of content and structure initially developed by K.C. Maguire, C. Jorgensen, and J. Blois as part of an effort to input mammal records into the Neotoma Paleoecological Database.

This document is in continuous development.  Currently this document supports Tilia v2.0.  To contribute to this document visit our BitBucket_ account or contact me through

.. _BitBucket : http://bitbucket.org/neotomadb/tilia

**Pro-tip.  Make sure you save your Tilia file often throughout this process!!**

Obtaining & Installing Tilia
========================================

Obtaining Tilia
---------------------------------------------------------------------
Tilia can be downloaded directly from TiliaIT_ using the *Download* tab.  Once the ZIP file is downloaded it can be opened using a program such as WinRAR, 7ZIP or WinZip.  The downloaded file contains a single file *setup_tilia_X_Y_ZZZ.exe* (where the X, Y and ZZZ represent the version numbering).  This file is an executable that will lead you through the setup process.  Tilia is built for Windows, but can be installed on Macintosh Brand or Linux system using an emulator.

.. _TiliaIT : http://tiliait.com

Installing Tilia on a Macintosh or Linux Machine
---------------------------------------------------------------------
Tilia is built on a platform that requires the use of Windows.  Given its popularity however, people have found solutions for using the software on multiple platforms.

Installing Tilia on a Macintosh
``````````````````````````````````````````````````````````````````````
*The following instructions were kindly provided by `Jonathan Nichols`_:*
To run Tilia on an OSX machine, the following programs must be installed:

* WINE_ for Darwin and OSX.
* XQuartz_ (or X11 if you are using OSX 10.5 or older) must be installed.

Once Wine and XQuartz (or X11) are installed and running, navigate to the “Start” menu in Wine and select “Run”

.. _WINE : http://sourceforge.net/projects/darwine/
.. _Jonathan Nichols : http://www.ldeo.columbia.edu/~jnichols/
.. _XQuartz : http://www.xquartz.org

.. image :: images/image16.png

Click “Browse” and navigate to the Tilia installer executable (see `Obtaining Tilia`_) and then click “OK”. Hint: Your regular Mac drive is listed as drive “Z:”

Once Tilia is installed it can be run as any other program through Wine.

Installing Tilia on a Linux Machine
``````````````````````````````````````````````````````````````````````
If you use Linux you can probably figure it out yourself.

Creating a New Tilia File:
========================================

Open up the Tilia program and open a new file (**File** > **New**).  A new window will open up, with two tabs at the top (Data & Metadata), several columns (Code, Name and Group) and a single header cell, by default **Pollen**.

.. figure :: images/image01.png
   :scale: 70

   A brand new empty data file.

The cell that contains the term **Pollen** can be modified to represent one of the other dataset types that Neotoma supports.  Once you have selected the dataset type, it’s possible to then load the lookup files that Tilia uses to standardize taxonomy and other associated sample information.

An Overview of a Tilia File
---------------------------------------------------------------------

The Data Tab
``````````````````````````````````````````````````````````````````````
The Data Tab is the first panel you see when you create a new file.  The Data tab will be the main location for the raw data collected at a site or collection unit within a site.

The Data tab contains three fixed columns that are visible immediately: “Code”, “Name” and “Group”.  The Data tab is organized in a Column/Row format, where rows represent variables and the columns are for each individual stratum or sample within the collection unit (e.g., there would be a row for *Pinus* pollen, with each column representing depths within a sediment core).
There are additional columns (“Elements”, “Units”, “Context”, and “Taphonomy”) that are also available by selecting **Tools** > **Options** and clicking the checkboxes within the “Show Columns” section.

.. figure :: images/ShowColumns.png

   Spreadsheet options for the data tab.  You can make extra variable-related columns visible using Tools > Options

Columns
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
Codes
  Variables are assigned shortened “codes” for identification.  These codes are associated with a **Lookup Table** for a particular dataset type.  For example, *Asarum* (wild ginger) is associated with the code “Asu”.
Element
  Varies based on dataset type (“Pollen”, “Vertebrate Fauna”, &cetera).
Units
  Varies based on dataset type (“Pollen”, “Vertebrate Fauna”, &cetera).
Context
  Varies based on dataset type (“Pollen”, “Vertebrate Fauna”, &cetera).
Taphonomy
  Varies based on dataset type (“Pollen”, “Vertebrate Fauna”, &cetera).
Groups
  Varies based on dataset type (“Pollen”, “Vertebrate Fauna”, &cetera).

The Metadata Tab
``````````````````````````````````````````````````````````````````````
The Metadata Tab is where you put information about the dataset that is not explicitly raw data.  This includes information about the spatial location, the collection unit itself, the particular dataset, the geochronological data associated with the record, how that geochronological data was used to construct a chronology, the lithology, a special tab for Loss on Ignition sampling, contact information and associated publications.  These entries are intended to help you navigate through the tabs so that you understand what is expected of you.  We will learn how to enter data in each tab further down in this guide.

Site
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure :: images/metadata_tab.png
   :scale: 70

   The "Site" metadata tab.

Collection Unit
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure :: images/metadata_collunit.png
   :scale: 70

   The "Collection Unit" metadata tab.

Dataset
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure :: images/metadata_dataset.png
   :scale: 70

   The "Dataset" metadata tab.

Geochronology
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

Chronologies
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure :: images/metadata_chronologies.png
   :scale: 70

   The "Chronologies" metadata tab.

Lithology
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure :: images/metadata_lithology.png
   :scale: 70

   The "Lithology" metadata tab.

LOI
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure :: images/metadata_loi.png
   :scale: 70

   The "LOI" metadata tab (very different from the LOL tab).

Editing Your Data
---------------------------------------------------------------------

Loading the Variable Lookup Files
``````````````````````````````````````````````````````````````````````
Before you begin, you need to load lookup files appropriate for your data type.  This does not (yet) happen automatically. To do so, click **Tools > Variable Lookup**.  The following window will appear:

.. image :: images/image04.png

Then choose the tables that apply to the dataset type you are entering (you can use the Browse button if you don’t see what you need). In general, these will be auto-filled.  This enables you to provide your own tables if needed, however, custom tables may make the upload & validation process more difficult for the Data Stewards. In the above figure, you can see the “Long Form” entry.  The “Short Form” allows you to define only the Taxa Names and “Modifiers”.

Because of the way lookup tables are structured, it is often difficult to include two data types at the same time, since units or taphonomies specific to both proxies may not be available simultaneously.

Editing Your Metadata
``````````````````````````````````````````````````````````````````````
In general, it’s easiest to start editing your collection information starting with the **Metadata** tab.  If you happen to be entering multiple datasets for the same site (or study) you can enter the **Metadata**, and then save the file (without entering any data) so it serves as a template for each subsequent dataset.  This helps speed up the process of generating Tilia files, particularly for large studies or multiproxy analyses.

.. image :: images/metadata_tabs.png

Metadata editing requires information to be entered on the following subtabs:

+ Site
+ Collection Unit
+ Dataset
+ Geochronology
+ Chronologies
+ Lithology
+ LOI
+ Publications :ref:`publications-tab`
+ Contacts :ref:`contacts-tab`

.. _publications-tab:

Modifying the Publications Tab
``````````````````````````````````````````````````````````````````````
The publications tab is where publication data associated with the record will be stored.  This data goes into Neotoma (and may already be stored in Neotoma) as part of the record, but is also stored apart from the collection record.

.. figure :: images/metadata_publications.png
   :scale: 70

To add a new record click **New**. Then click on the packrat to check if the publication already exists in the Neotoma database. The easiest way to do this is enter in the author’s last name as a wildcard search. If an appropriate reference shows up, click the reference and then click **Use**. If not, click **Cancel**. Choose whether the publication is a journal, book chapter, etc. Then fill in the appropriate fields. Filling in author’s data will also enter data into contacts as well.

Note that if you are adding records via Tilia on a Mac, Tilia freezes when entering new publications.  So save often, and perhaps do this step from a PC.

Contacts Tab
``````````````````````````````````````````````````````````````````````

Contacts are all individuals related to the record.  This includes the individuals who produced & published the record, but also the individuals who assisted in the preparation of chronologies, or in the submission of the data.

.. figure :: images/metadata_contacts.png
   :scale: 70

Contacts can (and likely will) be entered as you enter data into the other tabs.  You don't need to enter information in all at once, but you will need to link to individual contacts from a number of tabs (for example the :ref:`cronology-tab`). If you need to enter a Contact directly, follow the directions below:

First, check to confirm that contact information from the publications tab was entered correctly. Remember, contacts include the authors of the published paper you are entering, yourself (the data enterer), and the fossil collector(s). Authors should have been inserted previously when entering data in the publications tab. To add a new contact click the green + at the bottom. Enter a family name and click the rat. A new screen will appear. In the search box enter the family name and click the binoculars. If the correct contact is found and all data is up-to-date, click Match and it will be added to the Contacts Tab. If the contact info needs to be updated, click the blue arrow and add any additional information. Then click Update Contact. If there is not a contact in the database, press OK and then press the blue arrow to transfer the family name from the Tilia Contact to the Neotoma Contact. Fill in any data you can in the Neotoma Contact. Leading initials are the initials of the first and middle names with a period after them. Phone numbers should be entered in the following format: +1-XXX-XXX-XXXX. When all data is entered click Upload Contact.

Site Tab
``````````````````````````````````````````````````````````````````````
Site Name – Use the common name or most popular name used from the publication. Check Neotoma to make sure this name doesn’t already exist.
First Geopolitical Division - Country the site is in.
Second Geopolitical Division – State the site is in.
Third Geopolitical Division – County the site is in.
Administrative Unit –  Site is in private, state, federal, etc. land.
Latitude/Longitude – For exact locations, click “Point”. Enter in latitude and longitude. You will have the option to enter in either the decimal, degree or combination of decimal and degree. Enter data as decimals. Click the “Fuzzy” option if you don’t want the exact location of the site made publicly available and choose the radius of the range. If the general locality is unclear, click “Box” and fill in the four coordinate points. Hit OK. To add a bounding box directly from map view, click the google maps icon. A new tab named “Site Locator” will open. Select the “Box” button and N, E, S, W orientations will appear. Select one of the orientation buttons at a time, and click around the pin dropped on the map,  to create the perimeter of the bounding box.Doing so will set the north and south latitudes equal and the east and west longitudes equal.
Site Description – Enter in any additional information that describes the general description of the location.
Site Notes – Enter in any additional notes about the locality that may clear up any confusion, such as abbreviations, or changes in the site’s historical naming. [I’ll ADD ANYTHING ELSE I CAN THINK OF HERE]

Collection Unit Tab
``````````````````````````````````````````````````````````````````````
Handle – Create a unique handle name in all caps. This should be 4-10 letters long.
Collection Unit Type – This is what type of collection is it. For mammals, the most common choices will be Excavation, Isolated Specimen, Animal Midden, Surface Float, Midden.
Collection Unit Name – Enter in a name if there are multiple collections from the same locality. The name should be descriptive of the particular collection (e.g. collection number).
Collection Device/Location in Site – These fields are for pollen collection and can be left blank.
Collectors – Choose the appropriate person from the contact list. The format should be first name initial, middle name initial and last name (e.g. K.C. Maguire)
Date Collected – Record the most accurate date provided. If only the year is known, use January 1st. If only the month and year are known, use the 1st.
Depositional Environment – This will most likely be under terrestrial, so click the arrow next to terrestrial to get more options and search and then click on the appropriate subcategory to get more options.
Substrate – If known use the arrows to get more options and click the appropriate category.
Collection Unit Notes – add in any additional information about this specific collection that would be useful to other researchers. (e.g. notes on how the unit was collected, when the unit was collected, etc.)
Slope Angle, Slope Aspect, Water Depth – generally used for pollen collections - so leave blank.

Dataset Tab
``````````````````````````````````````````````````````````````````````
Dataset Type – Vertebrate fauna.
Dataset Name – Unique name to this faunal list (not always necessary to fill out).
Investigators – Who is responsible for the dataset, often but not always the author(s) of the published paper. The format should be first name initial, middle name initial and last name (e.g. K.C. Maguire).
Publications – Full publication record. Choose the appropriate publications associated with this locality. Format: Maguire, K.C., Blois, J.L., 2015. The best paper ever written.Nature Journal 36:3-15.
Repository – The museum or institution that houses the collection [S THERE SOME WAY WE CAN ADD MORE REPOSITORIES INTO TILIA? i’VE COME ACROSS SOME THAT WERE NOT PRESENT.]
Dataset Notes – any additional notes regarding the dataset, including the locality number for the repository institution (e.g. UCMP V35864).
Data Processors – The person who enters the data into the database. Format: K.C. Maguire
Spatial Extent – Don’t worry about this box, it’s mainly relevant to aggregate dataset. But if you want to add something, for most cases click Single Stratigraphic. Unclick box if the top sample is not modern surface sample.
Data Tab
Now that the basic metadata have been entered, the taxonomic data can be entered, so navigate to the main Data tab.
First, add the Analysis Unit names to the row headers, row 2.
If depths are available, add them (midpoints, generally) to the first row, above the relevant named analysis unit.
To add thicknesses, add a blank row UNDER the Analysis Unit name.  Then right click in the top left cell of that row, and enter Metadata → Analysis Unit → Thickness
If known, you can add the analyst too (e.g., if different people identified different strata within the deposit).  To do this, add another row below thickness using the same procedure as above, adding Metadata → Sample  Analyst.  Then, go to the cell below the first analysis unit, regular click in the cell, and add the relevant contacts from the `Contacts Tab`_.  Once you’ve added the first cell, you can then copy and paste to other analysis units.
Next fill in the taxa list, starting directly below the header metadata.
First fill out the Name column using the automatic pull down menu to select the taxon. This will automatically fill out the Code column and the Group column for you.
Element – the type of element representing that taxon. Typical faunal elements are bones, teeth, scales, and other hard body parts. Bone and tooth elements may be specifically identified (e.g. «tibia» or even more precisely «tibia, distal, left», «M2, lower, left»). Use the pull down menu.
Units – choose the appropriate unit that the data represent. If you have more than one unit type (e.g. Present/Absent, MNI and NISP), add a second row for that taxon and include data for the second unit type.
Context – add if known
Taphonomy  – add if known
Data –  Fill in the appropriate values for each cell, e.g., 1s or 0s if entering presence/absence data, or integer values if entering NISP or MNI
Specimens –  Eventually, will need to add in info about individual specimens.
OK, once the main data are entered, I go back to the metadata and work on the geochronology and chronology information

Geochronology Tab
``````````````````````````````````````````````````````````````````````
The Geochronology tab is central to generating the chronologies for your record.  It becomes linked to the `Contacts Tab`_ and to the `Chronology Tab`_.  The tab contains all geochronological records used for chronology construction.  In pracitice most Neotoma records include geochronological data, but this is not always the case.

.. figure :: images/metadata_geochronology.png
   :scale: 70

   The "Geochronology" metadata tab.

First, at the top add the Investigator name and any notes. Then there is the option to click Depth or Analysis Unit. If the site has individually dated layers with depth and thickness data, then choose Depth. If the site is an assemblage, choose Analysis Unit. Since you have added this information into the Data tab, it should be automatically linked (at least the Analysis Unit info).
Click the green + button at the bottom to add a new record, or just start typing in row 1.

Method
  Use the drop down menu to choose the appropriate dating method. This will be Carbon-14 in the majority of cases.
Age Units
  Use the drop down menu.
Depth
  Depth of the unit that is dated. Optional depth of the Analysis Unit in cm. Depths will typically be designated for Analysis Units from cores and for Analysis Units excavated in arbitrary (e.g. 10 cm) levels.
Thickness
  The thickness of the dated unit.
Analysis Unit
  This will most likely be an assemblage.
Lab Number
  The lab number of that sample.
Age
  The raw age of the sample.
SD
  The standard deviation of the raw age.
Params
  Click on the empty cell and a drop down box will appear. Click in the cell to the right of Methods and choose a dating method (e.g. accelerator mass spectrometry).
Material Dated
  What kind of material was dated (free-form text entry)
Publication
  Choose the publication from the drop down menu. (This should appear after entering the contact information.)

Click the green Check mark to post your edits once you're done.  The row you've just edited will get pushed down below the header.  You're not done quite yet.  There's still more information to add.

Once the record gets added to the Geochronology for the collection, you can add more information to the record.  To do this, click the "+" tab at the front of the row. A sub-row will appear.

ID
  This will fill in automatically. Leave it blank.
Taxon
  The taxon name for organic elements.
Element
  Use the pull down menu to select the element that was dated.  This is defined in part by the `Lookup Table`_ you've decided to use.
Fraction
  Use the pull down menu to select how the element/specimen was prepped for dating.  There are a pre-defined set of terms for use, including "Unknown", but you can also add your own terms if the available terms aren't appropriate.
Cal Age Older/Younger
  These are the calibrated dates for the samples.  You have two options here:

  1. Enter the calibrated ages by hand if they are provided in the paper (or you're handy with an Intcal table)
  2. Calibrate ages using Tilia. To do this, click **Tools** in the menu bar and then **Calibrate**. In the new menu put in the age of the sample and the standard deviation and press **Go**. This will automatically provide an older and younger calibrated age.

Cal Curve
  This is the calibration curve used to generate the calibrated dates.  If you used Tilia to calculate the date this will be Intcal13. If you used something else to calibrate the age (or if it was provided from a publication), choose the appropriate calibration curve from the drop down menu.
Cal Program
  Choose the calibration program that was used to generate the calibrated date.

Click the green check at the bottom to post the changes.

If you have more than one dated sample for this geochronology element, click the green + at the bottom of the page and add a second record. Continue process until all samples are recorded.

Chronology Tab
``````````````````````````````````````````````````````````````````````
The Chronology is separate from the `Geochronology`_.  Geochronology records dated samples, while the chronology includes undated samples (like a core-top in a sediment core) and tells the user how the age model for a record was put together.

To get started, open the “Chronologies” tab and click within the white bar containing the text “Click here to add a new row”.

.. figure :: images/image17.png
   :scale: 70

You will see that the solid bar becomes divided into cells when you click.  For each cell fill in the appropriate information:

Name
  A name for the chronology.  Give the Chronology a descriptive name (it’s a good rule of thumb not to just use “linear” or “Bacon” since you might make multiple models using the same method).
Age Units
  The chronology age units. This is a drop-down selection & does not permit multiple selections.
Default
  If you have only one model click the “Default” box.  Otherwise, if you have multiple models, decide which model will be the default.  This decision is important.  Once the data goes up to Neotoma the default model will be the one used in searches and to display the data.  *Only one record can be the Default.*
Age Model
  The “Age Model” cell is where you will describe the model used, for example “clam - linear”.
Older/Younger Bound
  The oldest & youngest ages of the model (used for searching).  Be careful here.  In a bootstrapped or Bayesian model it is possible to get estimates that are well beyond the range of acceptable values, particularly if you extrapolate below dated material.  Generally, the protocol is that the Older Bound is rounded up to the nearest 10 years and the Younger Bound is rounded down, e.g. if the sample age bounds are -44 to 10773, the Older Bound would be 10780 and the Younger Bound would be -50.
Preparers
  These are obtained from the `Contacts Tab`_ list.  If the Preparer is not already in that list then it is best to fill them in and then continue with the chronology tab. (NOTE: read below first)
Date Prepared
  When did you generate the age model?  This drop down menu provides a calendar, which is a nice touch.
Notes
  For more complex models including Bacon it is standard protocol to copy the settings into this field.  Otherwise this is a “free-form” cell.

Once the fields have been filled, click the tiny “+” sign at the bottom of the window.

This adds the entered data into the Chronology tray, allowing us to associate more data with the record.
Now we need to associate *Geochronological* data with the Chronology we’ve just created.  To begin this, we need to add the data from the `Geochronology Tab`_ to our chronology.  To do this we expand the Chronology we just created.  We do this by clicking the “+” sign at the beginning of the row (in the figure below).

Once you’ve clicked the "+" button you’ll see a new spreadsheet.  By clicking into the spreadsheet you will cause new buttons to appear under the Metadata Tabs.  The buttons say “Link”, “Import” and “Export”.
If you’ve already entered the Geochronological data into the metadata table, all you need to do is click “Import”.  A new window will appear (below).  Select the appropriate values.

In general it makes sense to use the defaults unless there is a very good reason to do so.

At this point you can enter any extra (non-geochron) dates that you may have used in generating your age model. The idea here is that this table will reflect the input data used to generate your age model.  For example, to add a “Core Top” date enter data in the top row, and then select **Age Basis > “Stratigraphic” > Core Top**.  You’ll see a number of options under these fields.

In cases where you are being proactive (congratulations!) and entering your data before you've built your age model, you may have enough information to construct a proper chronology, which allows you to estimate the ages of undated depths.  If you want to use Bacon or Clam to build your chronology then you can click the **Export** button at the top of the Chronologies worksheet.

.. image :: images/export_bacon.png

This will save the appropriate ``csv`` file for Bacon or Clam (in this case, make sure you have dates entered in the `Data Tab`_).  You can then build your age model using R and import the age model back into your record (discussed in the `Data Tab`_ section).

If you do use Bacon or Clam to generate your interpolated chronology then remember to copy your ``settings`` file into the Notes field.  This will allow people to replicate your results.

Data Tab
---------------------------------------------------------------------
Entering New Data
``````````````````````````````````````````````````````````````````````
Adding the Chronology
.................................................................................
Once the dates are added to the Chronology table, navigate back to the Data Tab.  Here we can import the dates for the model.  There are two options.  If you want Tilia to build the model for you you can select Tools > Chronology.  If you’ve built the model yourself using Bacon or Clam then you can import the output file directly using Tools > Import Chronology > Bacon/Clam.  If you have a record for which the age model is entirely made up of directly dated objects (or absolutely dated records) where the Chronology tab sheet is equivalent to the actual depths/records in the Data sheet then it is possible to directly import the Chronology Tab Sheet using Tools > Import Chronology > Chronologies Tabsheet.

To add the chronology from Bacon or Clam that you have already created, Go to Tools > Import Chronology > Bacon/Clam.  Your Chronologies have numbers associated with them in the Chronologies Tab.  Make sure you’re using the right Chronology number.  Bacon and Clam have different options, but you should choose the right file and the age values that make the most sense to you.

Once you click *OK*, navigate to the appropriate file and click okay.

Copying an Existing Spreadsheet
``````````````````````````````````````````````````````````````````````

Importing the


+ Geochronologic

  + Amino acid racemization
  + Argon-Argon
  + Caesium-137
  + Electron spin resonance
  + Fission track
  + Lead-210
  + Obsidian hydration
  + Optically stimulated luminescence
  + Potassium-argon
  + Radiocarbon

    + Radiocarbon - average of two or more dates
    + Radiocarbon, calibrated
    + Radiocarbon, calibrated from calendar years
    + Radiocarbon, calibrated, combined
    + Radiocarbon, summed probabilities
    + Radiocarbon, infinite
    + Radiocarbon, reservoir correction
    + Radiocarbon, reservoir correction, calibrated
    + Thermoluminescence
    + Uranium-series

+ Other Absolute Dating Methods

  + Annual laminations (varves)
  + Archaeomagnetic
  + Collection date
  + Dendrochronologic
  + Historical documentation

+ Palaeomagnetic
+ Other Dating Methods

  + Complex (mixture of types)
  + Extrapolated
  + Guess
  + Interpolated
  + Interpolated, correction for compaction

+ Relative Time Scale

  + Geologic time scale

    + Quaternary
    + Holocene
    + Late Holocene
    + Middle Holocene
    + Early Holocene
    + Early Holocene/Late Pleistocene
    + Pleistocene
    + Late Pleistocene
    + Middle Pleistocene
    + Early Pleistocene
    + Ionian
    + Calabrian
    + Gelasian

+ Geomagnetic polarity time scale
+ Marine isotope stages
+ North American Archaeological time scale
+ Stratigraphic

The chronology will be added to the Data tab.  Some issues may arise in doing this:
I’ve added my chronology, but the ages don’t appear:
This may be the result of a chronology whose depths aren’t aligned with the reported depths in the Tilia file.  In the case that

click on the first taxon, first column (the age model info will be inserted on a line above where you click).
Click on Tools, import chronology.  Check Bacon, make sure the Chronology number is correct, use the weighted mean (default),  click ok.
This will take you to the Bacon folder, click on the _ages.txt file.  Make sure that you are in the correct directory!  Click import, and viola.