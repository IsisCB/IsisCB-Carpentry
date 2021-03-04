[![isis bibliography logo](https://github.com/IsisCB/IsisCB-Carpentry/blob/main/media/isisCBLogoThumbnail.jpg)](https://data.isiscb.org/)
# Tutorial: Working with the IsisCB
### Covering the Citations Ingest Process and the Curation of Citation and Authority Records

---

## Table of Contents

* 1 [Ingesting Citations](#1-ingesting-citations)
  * 1.1 [The Zotero Accessions Interface](#11-the-zotero-accessions-interface)
    * 1.1.1 [Searching for Ingests](#111-searching-for-ingests)
  *  1.2 [Doing a New Ingest](#12-doing-a-new-ingest)
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
    * 3.1.3 [Bulk Change](#313-bulk-change)
    * 3.1.4 [Bulk Select](#314-bulk-select)
    * 3.1.5 [Export](#315-export)
    * 3.1.6 [Collections](#316-collections)
  * 3.2 [The Authorities Management Interface](#32-the-authorities-management-interface)
    * 3.2.1 [Searching for Authorities](#321-searching-for-authorities)
    * 3.2.2 [Editing Authorities in the Authority Curation Interface](#322-editing-authorities-in-the-authority-curation-interface)
  * 3.3 [Creating New Authorities](#33-creating-new-authorities)
    * 3.3.1 [Creating a New Person](#331-creating-a-new-person)
    * 3.3.2 [Creating a New Institution](#332-creating-a-new-institution)
    * 3.3.3 [Creating a New Time Period](#333-creating-a-new-time-period)
    * 3.3.4 [Creating a New Geographic Term](#334-creating-a-new-geographic-term)
    * 3.3.5 [Creating a New Serial Publication](#335-creating-a-new-serial-publication)
    * 3.3.7 [Creating a New Concept](#337-creating-a-new-concept)
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
##  3.1 The Citations Management Interface

![image of isis cb citations management interface](/media/citationsManagementInterface.png)

There are six things you can do from the Citations Management Interface
* [**search** for and filter citations](#311-searching-for-citations)
* [**create a new citation record**](#312-create-a-new-citation-record)
* [**bulk change** any set of citations](#313-bulk-change)
* [**bulk select** citations](#314-bulk-select)
* [**export** any set of citations](#315-export)
* [group sets of citations into **collections**](#316-collections)

These six functions are covered in detail below

[^ Up to Table of Contents](#table-of-contents)

---
###  3.1.1 Searching for Citations

![image of isis cb citations management search](/media/citationsManagementSearch.png)

[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.2 Create a New Citation Record



[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.3 Bulk Change



[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.4 Bulk Select



[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.5 Export



[^ Up to Table of Contents](#table-of-contents)

---

###  3.1.6 Collections



[^ Up to Table of Contents](#table-of-contents)

---
##  3.2 The Authorities Management Interface



[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.1 Searching for Authorities



[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.2 Editing Authorities in the Authority Curation Interface



[^ Up to Table of Contents](#table-of-contents)

---
###  3.3 Creating New Authorities

Through
* the [authority resolution process](#122-resolving-attached-Authorities)
* the [citation curation interface](#22-the-citation-curation-interface)
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

![image of Isis CB time period authority creation interface](/media/createTimePeriodAuthority.png)

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
