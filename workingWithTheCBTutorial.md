[![isis bibliography logo](https://github.com/IsisCB/IsisCB-Carpentry/blob/main/media/isisCBLogoThumbnail.jpg)](https://data.isiscb.org/)
# Tutorial: Working with the IsisCB
### Covering the Citations Ingest Process and the Curation of Citation and Authority Records

> Tutorial Author: Paul Kelley Vieth (pvieth@ou.edu)
>
>IsisCB Editor: Stephen Weldon
>
>Explore the IsisCB: [data.isiscb.org ](data.isiscb.org)
>
>Contact the IsisCB: isisbibliography@gmail.com

---

## Table of Contents

* 1 [Ingesting Citations](#1-ingesting-citations)
  * 1.1 [The Zotero Accessions Interface](#11-the-zotero-accessions-interface)
    * 1.1.1 [Searching for Ingests](#111-searching-for-ingests)
  * 1.2 [Doing a New Ingest](#12-doing-a-new-ingest)
    * 1.2.1 [Uploading .rdf Files](#121-uploading-rdf-files)
    * 1.2.2 [Resolving Attached Authorities](#122-resolving-attached-Authorities)
      * 1.2.2.1 [If the Authority Already Exists in Our Database](#1221-if-the-authority-already-exists-in-our-database)
      * 1.2.2.2 [If You Need to Create a New Authority](#1222-if-you-need-to-create-a-new-authority)
      * 1.2.2.3 [If You Need to Skip an Authority](#1223-if-you-need-to-skip-an-authority)
* 2 [Curating Citations](#2curating-citations)
  * 2.1 [Different Citation Types](#21-different-citation-types)
    * 2.1.1 [Articles](#211-articles)
    * 2.1.2 [Books](#212-books)
    * 2.1.3 [Book Reviews](#213-book-reviews)
    * 2.1.4 [Essay Reviews](#214-essay-reviews)
    * 2.1.5 [Other Citation Types](#215-other-citation-types)
  * 2.2 [The Citation Curation Interface](#22-the-citation-curation-interface)
    * 2.2.1 [Citation Curation Interface Views](#221-citation-curation-interface-views)
      * 2.2.1.1 [Fields Tab](#2211-fields-tab)
      * 2.2.1.2 [Attributes Tab](#2212-attributes-tab)
      * 2.2.1.3 [Linked Data Tab](#2213-linked-data-tab)
      * 2.2.1.4 [Related Citations Tab](#2214-related-citations-tab)
      * 2.2.1.5 [Related Authorities Tab](#2215-related-authorities-tab)
      * 2.2.1.6 [Tracking Tab](#2216-tracking-tab)
    * 2.2.2 [Attaching Subjects and a Category](#222-attaching-subjects-and-a-category)
      * 2.2.2.1 [Attaching Existing Subjects](#2221-attaching-existing-subjects)
      * 2.2.2.2 [Creating New Subjects](#2222-creating-new-subjects)
      * 2.2.2.3 [Attaching Categories](#2223-attaching-categories)
* 3 [The Datasets Management Interfaces](#3-the-datasets-management-interfaces)
  * 3.1 [The Citations Management Interface](#31-the-citations-management-interface)
    * 3.1.1 [Searching for Citations](#311-searching-for-citations)
    * 3.1.2 [Create a New Citation Record](#312-create-a-new-citation-record)
    * 3.1.3 [Bulk Change Citations](#313-bulk-change-citations)
    * 3.1.4 [Bulk Select Citations](#314-bulk-select-citations)
    * 3.1.5 [Export Citations](#315-export-citations)
    * 3.1.6 [Citations Collections](#316-citations-collections)
  * 3.2 [The Authorities Management Interface](#32-the-authorities-management-interface)
    * 3.2.1 [Searching for Authorities](#321-searching-for-authorities)
    * 3.2.2 [Create a New Authority Record](#322-create-a-new-authority-record)
    * 3.2.3 [Bulk Change Authorities](#323-bulk-change-authorities)
    * 3.2.4 [Bulk Select Authorities](#324-bulk-select-authorities)
    * 3.2.5 [Bulk Select (CSV) Authorities](#325-bulk-select-csv-authorities)
    * 3.2.6 [Export Authorities](#326-export-authorities)
    * 3.2.7 [Authorities Collections](#327-authorities-collections)
  * 3.3 [Creating New Authorities](#33-creating-new-authorities)
    * 3.3.1 [Creating a New Person](#331-creating-a-new-person)
    * 3.3.2 [Creating a New Institution](#332-creating-a-new-institution)
    * 3.3.3 [Creating a New Time Period](#333-creating-a-new-time-period)
    * 3.3.4 [Creating a New Geographic Term](#334-creating-a-new-geographic-term)
    * 3.3.5 [Creating a New Serial Publication](#335-creating-a-new-serial-publication)
    * 3.3.7 [Creating a New Concept](#337-creating-a-new-concept)
  * 3.4 [Editing Authorities in the Authority Curation Interface](#322-editing-authorities-in-the-authority-curation-interface)
---

# 1 Ingesting Citations
---
## 1.1 The Zotero Accessions Interface

![Image of Isis CB Zotero Accessions Interface](/media/zoteroAccessions.png)

The Zotero Accessions interface can be accessed through the "Zotero" dropdown menu in the upper righthand corner of the backend.

The Zotero Accessions interface allows you to:

  * [upload new .rdf files (containing citations from zotero)](#121-uploading-rdf-files)
  * [search for past uploads or ingests](#111-searching-for-ingests) to access the 3 accessions functions:
    * [**resolve** their attached authorities](#122-resolving-attached-authorities) (blue button seen above)
    * **ingest** the upload once resolved (green button above)
    * **view** a list of citations from that upload that have been resolved and ingested (yellow button above).

[^ Up to Table of Contents](#table-of-contents)

---
###  1.1.1 Searching for Ingests

![image of isis cb zotero accessions search interface](/media/accessionsSearch.png)

The accessions search interface allows you to find past uploads and ingests with a set of search filters.

To access the zotero accessions search interface, click the blue "Show/hide filters" bar at the top of the zotero accessions interface. Filters include:
* ID
  * each upload is assigned a unique ID
* Processed
  * a boolean denoting whether the upload has been processed (i.e. resolved and ingested)
* Imported by
  * the IsisCB user who originally uploaded the set of citations
* Name starts with
  * this refers to the name assigned to the upload. When you [upload an .rdf file](#121-uploading-rdf-files), by default the name assigned to that upload is the filename as it exists on your local machine, but can be changed at the time of upload
* Imported on or after/Imported on or before
  * a date that can be specified by:
    * typing in the date in the format `yyyy-mm-dd`
    * selecting the date using the calendar dropdown
* Ingested to
  * this refers to the dataset the .rdf file was uploaded to. By default, files are uploaded to the *Isis Bibliography of the History of Science (Stephen P. Weldon, ed.)* dataset

[^ Up to Table of Contents](#table-of-contents)

---

## 1.2 Doing a New Ingest

---

###  1.2.1 Uploading .rdf Files

Begin a new ingest by clicking the green button on the left-hand side of the zotero accessions interface labeled **+Upload RDF**

This opens to Upload dialog

![image of Isis CB upload page](/media/uploadPage.png)

From here  select an .rdf file from your local machine using the **Choose File** button seen above

Do not change the assigned dataset in the **Ingest to** section of the upload process unless you are sure that you need to

The `Name` field of the upload process will autofill using the name of the file you uploaded but can be changed if desired

**Then, click the green Upload button**

> Note: For help preparing .rdf files for this upload process, see our tutorial on [Data Prep with Zotero](/placeholder-link1.md)

[^ Up to Table of Contents](#table-of-contents)

---

###  1.2.2 Resolving Attached Authorities

Once your upload is complete you will automatically be redirected to the authority resolution page
* You can also access this page by searching for a previous upload through the Zotero Accessions interface and clicking the blue **Resolve** button attached to that upload

![image of Isis CB authority resolution page](/media/resolutionPage.png)

> Note: if the first authority to be resolved isn't highlighted in orange already (as seen above), click on that authority to do so

[^ Up to Table of Contents](#table-of-contents)

---

####  1.2.2.1 If the Authority Already Exists in Our Database

When the authority being resolved (in the left panel) is highlighted in orange, the authority search interface appears in the right panel

![image of Isis CB Resolution Page Search Panel](/media/resolutionPageSearch.png)

In this panel you can search for
* **Institutions** to link to book publishers
* **Serial Publications** to link to article journals
* **People** to link to authors, editors, translators, advisors (for theses), and contributors
* **Concepts**, **Time Periods**, **Geographic Terms**, **People**, or any other authority type to link to a citation's subject terms (if you assigned them as tags in zotero during data prep)

> If you're not sure if an authority in the search results is the one you're looking for (especially when searching for people) simply hover over the authority name and a list of related citations will pop up to guide your decision ![image of Isis CB resolution page authority related citations](/media/resolutionPageRelatedPopup.png)

**Then, Simply click the checkmark next to the search result to link it to the highlighted data item**

*The system will automatically progress to the next authority to be linked*

> Note of Caution: sometimes the search has difficulty locating the target authority. If this happens
> * make sure you have the correct authority type selected in the dropdown
> * try deleting the hyphen (and sometimes also the first half) of hyphenated names
> * try replacing characters with diacritical marks above them with the plain version of that character
> * (for people) try searching for only the surname and scanning the results list for the full name
> * if the name still does not appear in the search results, then go ahead and [create a new authority](#1222-if-you-need-to-create-a-new-authority)

[^ Up to Table of Contents](#table-of-contents)

---

####  1.2.2.2 If You Need to Create a New Authority

Click the **Create** button between the **Search** tab and the **Skip** button in the righthand Panel

This will take you to the authority creation interface. See the [Creating New Authorities](#33-creating-new-authorities) section for help doing this

After you create a new authority from within the resolution process, the system will automatically link that new authority to the highlighted data item, redirect you back to the resolution page, and advance to the next data item needing to be linked

> Note: if you decide you don't want to create a new authority after all and you use the browser's back button to return to the resolution page from the authority creation page, you may see some of your resolution progress appear to be undone. The post-data in the resolution page just hasn't caught up to your progress. Simply refresh the page and the system will catch up right where you left off


[^ Up to Table of Contents](#table-of-contents)

---

####  1.2.2.3 If You Need to Skip an Authority

If for any reason you need to skip one of the authorities imported with the citation in the upload process, simply click the **Skip** button (to the right of the **Create** button).
> Note: If you skip too many items in quick succession, the system may become confused about the authority resolution order and begin to rapidly refresh the search results. If this happens, simply refresh the page.

[^ Up to Table of Contents](#table-of-contents)

---

#  2 Curating Citations
##  2.1 Different Citation Types



[^ Up to Table of Contents](#table-of-contents)

---

##  2.2 The Citation Curation Interface



[^ Up to Table of Contents](#table-of-contents)

---
###  2.2.1 Citation Curation Interface Views



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.1 Fields Tab



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.2 Attributes Tab



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.3 Linked Data Tab



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.4 Related Citations Tab



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.5 Related Authorities Tab



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.6 Tracking Tab



[^ Up to Table of Contents](#table-of-contents)

---
###  2.2.2 Attaching Subjects and a Category



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.2.1 Attaching Existing Subjects



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.2.2 Creating New Subjects



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.2.3 Attaching Categories



[^ Up to Table of Contents](#table-of-contents)

---
# 3 The Datasets Management Interfaces

The Datasets Management interfaces can be accessed through the **Datasets** dropdown in the main menu at the top of the IsisCB backend

There are two Datasets Management interfaces
* [The Citatations Management interface](#31-the-citations-management-interface)
* [The Authorities Management interface](#32-the-authorities-management-interface)

These management interfaces are explained in detail below

##  3.1 The Citations Management Interface

![image of isis cb citations management interface](/media/citationsManagementInterface.png)

There are 6 things you can do from the Citations Management Interface
* [**search** for and filter citations](#311-searching-for-citations)
* [**create a new citation record**](#312-create-a-new-citation-record)
* [**bulk change** any set of citations](#313-bulk-change-citations)
* [**bulk select** citations](#314-bulk-select-citations)
* [**export** any set of citations](#315-export-citations)
* [group sets of citations into **collections**](#316-citations-collections)

These 6 functions are covered in detail below

[^ Up to Table of Contents](#table-of-contents)

---
###  3.1.1 Searching for Citations

![image of isis cb citations management search](/media/citationsManagementSearch.png)

To access the Citations Search Interface, **click** the blue **Show/hide filters** bar in the Citatations Management Interfaces

The search interface will expand revealing several search filter fields:
* `Combined`
  * for a compound search cross-referencing multiple filters separated by commas
  * using the format `Title, Author, Description, Abstract, Subject, Category`
* `Title`
* `Au./Ed.`
  * for filtering by citation author or editor
* `Periodical`
  * for filtering by **Serial Publication** for journal articles
* `Publisher`
  * for books
* `Pub date/Modified/Created after/before`
  * for filtering by the date a citation was published, modified, or created
  * dates may be typed using the format `yyyy-mm-dd` or selected from the calendar dropdown
* `Id`
  * each citation is assigned a unique ID on creation
  * use this field to search for individual citations by ID, or
  * use this field to search for any set of citations with a comma-separated list of IDs
* `Abstract`
  * for keyword searching the text of a citation's abstract
* `Descript`
  * for keyword searching the text of a citation's description
* `Subject`
  * for filtering by the authorities linked to a citation as subjects
* `Pub. date free`
  * a freehand textbox for filtering by date
  * enter `null` here to search for citations with empty date fields
* `Type`
  * filter by citation medium type
* `Status`
* `Tracking`
* `Modifier`
  * the Isis CB user who last made an edit to the citation
* `Database`
* `Collection`
  * a set of records can be [assigned to a collection](#316-citations-collections). You can search for those collections here
* `Zotero`
  * this filter is used to search for sets of citations that were uploaded and ingested together. This is equivalent to [searching for ingests and uploads in the Zotero Accessions Interface](#111-searching-for-ingests) and clicking the **view** button there
* `Creator`
  * the Isis CB user who originally created the citation, either through the [ingest process](#12-doing-a-new-ingest) or using the [Create a New Citation Record](#312-create-a-new-citation-record) function in the Citations Management Interface
* `Print`
  * filter by the print status of citations


[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.2 Create a New Citation Record

![image of isis cb create new citation record interface](/media/createNewCitationRecord.png)

The **Create a New Citation Record** interface can be accessed by clicking the blue **Create New Citation Record** button on the left side of the Citations Management Interface (below the Search/Filter Interface section of the page)

This is an alternative to [creating citations through the .rdf file ingest process](#12-doing-a-new-ingest). This function allows you to create only one citation at a time.

> When creating citations using this function, **Follow the [guidelines for creating the different citation types](#21-different-citation-types)**

Once you've filled out the necessary metadata of the citation, **click** the green **Creat & Continue** button

[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.3 Bulk Change Citations

![image for Isis CB bulk change interface](/media/bulkChangeInterface.png)

There are several changes you can make to citations in bulk as seen in the `Action` selection box of the Bulk Change Interface. Most of these types of changes are advanced functionality for database administrators that you can ignore. The two that you will need to use regularly are
* `Set Record Status`
* `Set Record Tracking Status`

> Note: you can select multiple bulk change functions to perform simultaneously by holding down `ctrl/cmd` (windows/mac) when selecting functions from the `Action` menu

Once you've selected the functions you want to run, the function options will appear in the right-hand column of the Bulk Change interface

**Click** the blue **Apply** button

You'll be taken to the Bulk Change Progress page

When the progress bar fills blue and reads **Done!**, **click** the green **Return to Search Interface** button at the bottom of the page to be redirected to the Citations Management Interface  

> Note: When you're redirected to the Citations Management Interface, you will be inside a search containing the same citations you've just made a bulk change to. This way you can make further changes to this set of citations as necessary

**Using the Bulk Change interface to finish curating citations:**
* set `Set Record Status` to **active**
* set `Set Record Tracking Status` to **Fully Entered**
* once the Bulk Change interface redirects you to the Citations Management interface after it finishes implementing the above changes, return to the Bulk Change interface
* set `Set Record Tracking Status` to **Proofed** and follow the steps to complete these changes. The records you've just curated are now publicly visible on the Isis Bibliography online and ready to be collated into next year's print version of the *Isis Current Bibliography*

[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.4 Bulk Select Citations

![image of the isis cb bulk select interface](/media/bulkSelectInterface.png)

You can access the Bulk Select interface by clicking the blue **Bulk Select** button between the **Bulk Change** and **Export** buttons in the Citations Management interface (underneath the Search/Filter section of the page)

The Bulk Select interface performs the same function as the `ID` field of the [Citations Management Search interface](#311-searching-for-citations), but if you need to grab a large number of citations by ID, then this interface is useful

Simply enter a comma-separated list of citation IDs and **click** the green **Select** button. You will be redirected to the Citations Management interface with your search results

[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.5 Export Citations

![image of isis cb export citations interface](/media/exportInterface.png)

To access the Export Citations interace, **click** the blue **Export** button between the **Bulk Select** and **Collections** buttons in the Citations Management interface (underneath the Search/Filter section of the page)

To export a set of citations:
* enter an `Export Name`
* select the `Export Format`
  * .csv by default
* check whether you want to
  * `Export linked records`
    * e.g., reviews linked to books
  * `Export metadata`
  * `Use "||" to separate related authority and citation fields`
* select which citation fields you'd like to include in the export from the `Fields` multiselection box
  * hold `ctrl/cmd` (window/mac) to select multiple fields
* **click** the green **Create** button to begin the download

[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.6 Citations Collections

From the **Collections** dropdown menu (between the **Export** and **Link Records** buttons in  the Citations Management interface) you can
* **Create a new collection** from the set of citations currently filtered in the view
* **Add to an existing collection** the set of citations currently filtered in the view
* or **view collections** you've made in the past

To **Create a new collection**
* select the first option from the **Collections** dropdown menu
* give the new collection a `Name`
* *(optional)* give the new collection a `Description`
* **click** the green **Create** button

[^ Up to Table of Contents](#table-of-contents)

---
##  3.2 The Authorities Management Interface

![image of isis cb authorities management interface](/media/authoritiesManagementInterface.png)

There are 7 things you can do from the Authorities Management Interface
* [**search** for and filter authorities](#321-searching-for-authorities)
* [**create a new authority record**](#322-create-a-new-authority-record)
* [**bulk change** any set of authorities](#323-bulk-change-authorities)
* [**bulk change (CSV)** any set of authorities](#324-bulk-change-csv-authorities)
* [**bulk select** authorities](#325-bulk-select-authorities)
* [**export** any set of authorities](#326-export-authorities)
* [group sets of authorities into **collections**](#327-authorities-collections)

These 7 functions are covered in detail below

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.1 Searching for Authorities

![image of isis cb authorities management search](/media/authoritiesManagementSearch.png)

To access the Citations Search Interface, **click** the blue **Show/hide filters** bar in the Authorities Management Interfaces

The search interface will expand revealing several search filter fields:
* `Name`
* `Class.Syst.`
  * authorities are assigned to different classification systems when created. Use this field to filter authorities by classification system
* `Clas.Code`
  * each category and category sub-component in the IsisCB classification system has a unique numerical code. Use this field to filter category authorities according to this code
* `Clas.Hier.`
  * use this field to filter authorities according to where the fall in the IsisCB classification system hierarchy
* `Id`
  * each authority is assigned a unique ID on creation
  * use this field to search for individual authorities by ID, or
  * use this field to search for any set of authorities with a comma-separated list of IDs
* `Descrip.`
  * for keyword searching the text of an authority's description
* `LD Type`
  * use this field to filter authorities by the types of **Linked Data** (e.g., URLs or ISSNs) attached to them
* `Att Typ.`
  * use this field to filter authorities by different **Attribute Types** attached to them
* `Type`
  * filter by authority type
* `Status`
* `Tracking`
* `Modifier`
  * the Isis CB user who last made an edit to the authority
* `Database`
* `Collection`
  * a set of authorities can be [assigned to a collection](#327-authorities-collections). You can search for those collections here
* `Zotero`
  * this filter is used to search for sets of authorities that were uploaded and ingested together through the [Zotero Accessions interface](#11-the-zotero-accessions-interface)
* `Creator`
  * the Isis CB user who originally created the citation, either through the [ingest process](#12-doing-a-new-ingest) or using the [Create a New Citation Record](#312-create-a-new-citation-record) function in the Citations Management Interface
* `Modified/Created after/before`
  * for filtering by the date an authority was modified, or created
  * dates may be typed using the format `yyyy-mm-dd` or selected from the calendar dropdown

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.2 Create a New Authority Record

See the [Creating New Authorities](#33-creating-new-authorities) section for help with creating authorities

[^ Up to Table of Contents](#table-of-contents)

---

###  3.2.3 Bulk Change Authorities

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.4 Bulk Change CSV Authorities

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.5 Bulk Select Authorities

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.6 Export Authorities

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.7 Authorities Collections

[^ Up to Table of Contents](#table-of-contents)

---
###  3.3 Creating New Authorities

Through
* the [authority resolution process](#122-resolving-attached-Authorities)
* the [citation curation interface](#22-the-citation-curation-interface)
* the [create new authority record]() function of the [Authorities Management interface](#32-the-authorities-management-interface)
* or, the [subjects and categories interface](#222-attaching-subjects-and-a-category)

. . . you may need to create a new authority. The following sections walk you through the specifics of creating each type of authority

[^ Up to Table of Contents](#table-of-contents)

---
####  3.3.1 Creating a New Person

![image of Isis CB person authority creation interface](/media/createPersonAuthority.png)

To create a new Person authority, first select **Person** from the dropdown menu in the `Type` field

Fill out the `Name` field using the format `[lastName, firstName]`
* once you fill out the `Name` field, the `Last` and `First` fields will auto-populate

> Note: if you are creating a new  authority from the authority resolution interface of the ingest process, the `Name` field will already be filled out for you

Click the blue **VIAF** button at the top of the authority creation interface
* this will open up a VIAF search for the authority name in a new tab
* you may have to adjust the VIAF search to find the person
* if the name is common and VIAF returns many results, the find `(ctrl/cmd+f)` function of your browser can help you more efficiently scan the results
* when you find a promising candidate, open its VIAF page (see image below)

[![image of virtual international authority file record page](/media/viafAuthorityPage.png)](http://viaf.org/viaf/22146457)

> Note: use the **Works** section of the VIAF authority page to help you decide whether this VIAF page represents the person or institution you're looking for

Once you've decided this is the correct VIAF page for the authority you're creating, copy the VIAF **permalink** (it's beneath the list of names an the VIAF ID at the top of the VIAF record)

Switch back to the authority creation tab and paste the VIAF permalink into the `URN (link to authority)` field
* make sure **VIAF** is selected in the `Linked Data Type` field dropdown menu

If the VIAF authority record for a person includes any of that person's **birth**, **death**, or **flourished** (represented by *fl.*) dates (found next to the authority name at the top of the record page in VIAF):
* select the appropriate date attribute from the `Attribute Type` field dropdown in the authority creation page
* fill out the `Start` and/or `End` fields that appear, as appropriate

If the person cannot be found in VIAF
* **find** the page for the person on Wikipedia, or find an official (through an institution) profile page for the person on the web
* **copy** the URL for that webpage and **paste** it into the `URN (link to authority)` field
* make sure **URL** is selected in the `Linked Data Type` field dropdown menu

Once you have a VIAF permalink or another URL for the Person, **Click** the green **Create & Continue** button at the top-right of the authority creation interface to finalize the creation of this Authority

> Note: if you initated the authority creation from the Subjects and Categories interface, this newly created authority will not automatically be linked as a subject to the citation. You will have to search for and select the newly created authority in the Subjects and Categories interface

[^ Up to Table of Contents](#table-of-contents)

---
####  3.3.2 Creating a New Institution

![image of Isis CB institution authority creation interface](/media/createInstitutionAuthority.png)

To create a new Institution authority, first select **Institution** from the dropdown menu in the `Type` field

Fill out the `Name` field

> Note: if you are creating a new  authority from the authority resolution interface of the ingest process, the `Name` field will already be filled out for you

Click the blue **VIAF** button at the top of the authority creation interface
* this will open up a VIAF search for the authority name in a new tab
* you may have to adjust the VIAF search to find the person
* if the name is common and VIAF returns many results, the find `(ctrl/cmd+f)` function of your browser can help you more efficiently scan the results
* for institutions, the `type` field of the VIAF search results will be listed as **Corporate**
* when you find a promising candidate, open its VIAF page (see image below)

[![image of virtual international authority file record page](/media/viafAuthorityPage.png)](http://viaf.org/viaf/22146457)

> Note: use the **Works** section of the VIAF authority page to help you decide whether this VIAF page represents the person or institution you're looking for

Once you've decided this is the correct VIAF page for the authority you're creating, copy the VIAF **permalink** (it's beneath the list of names an the VIAF ID at the top of the VIAF record)

Switch back to the authority creation tab and paste the VIAF permalink into the `URN (link to authority)` field
* make sure **VIAF** is selected in the `Linked Data Type` field dropdown menu

If the institution cannot be found in VIAF
* **find** the page for the institution on Wikipedia, or find the institution's homepage on the web
* **copy** the URL for that webpage and **paste** it into the `URN (link to authority)` field
* make sure **URL** is selected in the `Linked Data Type` field dropdown menu

Once you have a VIAF permalink or another URL for the Institution, **Click** the green **Create & Continue** button at the top-right of the authority creation interface to finalize the creation of this Authority

> Note: if you initated the authority creation from the Subjects and Categories interface, this newly created authority will not automatically be linked as a subject to the citation. You will have to search for and select the newly created authority in the Subjects and Categories interface

[^ Up to Table of Contents](#table-of-contents)

---
####  3.3.3 Creating a New Time Period

Do not create new time periods.

If you feel a new time period authority needs to be created, contact an IsisCB administrator with your recommendation

[^ Up to Table of Contents](#table-of-contents)

-----
####  3.3.4 Creating a New Geographic Term

![image of Isis CB geographic term authority creation interface](/media/createGeographicTermAuthority.png)

[^ Up to Table of Contents](#table-of-contents)

---
####  3.3.5 Creating a New Serial Publication

![image of Isis CB serial publication authority creation interface](/media/createSerialPublicationAuthority.png)

[^ Up to Table of Contents](#table-of-contents)

---
####  3.3.7 Creating a New Concept

![image of Isis CB concept authority creation interface](/media/createConceptAuthority.png)

[^ Up to Table of Contents](#table-of-contents)

---

###  3.4 Editing Authorities



[^ Up to Table of Contents](#table-of-contents)
