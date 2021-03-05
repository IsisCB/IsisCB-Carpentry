[![isis bibliography logo](https://github.com/IsisCB/IsisCB-Carpentry/blob/main/media/isisCBLogoThumbnail.jpg)](https://data.isiscb.org/)
# Tutorial: Working with the IsisCB
### Covering the Citations Ingest Process and the Curation of Citation and Authority Records

> Tutorial Author: Paul Kelley Vieth (pvieth@ou.edu)
>
> Tutorial Contributors: Kraig Bartel and Francesco Luzzini
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
* 2 [Curating Citations](#2-curating-citations)
  * 2.1 [Different Citation Types](#21-different-citation-types)
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
    * 2.2.3 [ACR Relations](#223-acr-relations)
    * 2.2.4 [CCR Relations](#224-ccr-relations)
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
    * 3.2.4 [Bulk Change (CSV) Authorities](#324-bulk-change-csv-authorities)
    * 3.2.5 [Bulk Select Authorities](#325-bulk-select-authorities)
    * 3.2.6 [Export Authorities](#326-export-authorities)
    * 3.2.7 [Authorities Collections](#327-authorities-collections)
  * 3.3 [Creating New Authorities](#33-creating-new-authorities)
    * 3.3.1 [Creating a New Person](#331-creating-a-new-person)
    * 3.3.2 [Creating a New Institution](#332-creating-a-new-institution)
    * 3.3.3 [Creating a New Time Period](#333-creating-a-new-time-period)
    * 3.3.4 [Creating a New Geographic Term](#334-creating-a-new-geographic-term)
    * 3.3.5 [Creating a New Serial Publication](#335-creating-a-new-serial-publication)
    * 3.3.6 [Creating a New Concept](#336-creating-a-new-concept)
  * 3.4 [Editing Authorities in the Authority Curation Interface](#34-editing-authorities)
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

> Note: if you have citations attached to other citations (e.g., reviews you're ingesting attached to the books they review), then those attachments will be verified at the bottom of the Authority Resolution interface ![image of isis cb authority resolution interface linked citations verification notification](/media/authorityResolutionCitationMatching.png)

* Once you have resolved all the authorities in the import, **click** the green **Ingest Citations** button at the top-left of the Authority Resolution interface to finalize the ingest
* You will be redirected to the [Citations Management interface](#31-the-citations-management-interface) where the citations you have just ingested with be listed out for you.
* **click** on the ID of the first citation in the list (e.g. `CBB123456789`) to begin [curating these citations](#2-curating-citations) in the [Citation Curation interface](#22-the-citation-curation-interface)

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

IsisCB uses many different citation types to characterize bibliographic records
* Most commonly used
  * **Book**
    * make sure to include
      * the **page length** in the `Extent` field
      * the **publisher** in the `Hosting body` section
  * **Article**
    * make sure to include
      * the **volume number** in the `Volume` field
      * the **issue number** in the `No./episode` field
      * the **page numbers** in the `Pages` field
        * if the item was published online and either lacks page numbers or has a code assigned by the journal instead of page numbers it is okay to leave this field blank or to just include the page code provided
      * the **journal** in which it was published in the `Hosting body` section
      * if the article is part of a series, include the [CCR link](#224-ccr-relations) to the series introduction article in the `Linked Citations` section
  * **Review**
    * make sure to include
    * the **volume number** in the `Volume` field
    * the **issue number** in the `No./episode` field
    * the **page numbers** in the `Pages` field
      * if the item was published online and either lacks page numbers or has a code assigned by the journal instead of page numbers it is okay to leave this field blank or to just include the page code provided
    * the **journal** in which it was published in the `Hosting body` section
    * a [CCR link](#224-ccr-relations) to the book that the item reviews in the `Linked Citations` section
  * **Chapter**
    * a [CCR link](#224-ccr-relations) to the book of which it is a part in the `Linked Citations` section
    * page numbers in the `Pages` field
  * **Thesis**
    * an [ACR link](#223-acr-relations) to the advisor of the thesis in the `Responsibility` section
  * **Essay Review**
    * a [CCR link](#224-ccr-relations) to the book that the item reviews in the `Linked Citations` section
* Less commonly used
  * Event
  * Web Object
  * Multimedia Object
  * Archive Object
  * Digital Resource
  * Personal Recognition

**All records should include**
* [ACR links](#223-acr-relations) in the `Responsibility` section representing any authors, editors, contributors, advisors, translators, etc., where applicable
* [ACR links](#223-acr-relations) in the `Hosting body` section representing any **Serial Publication** or **Publishing Institution**, where applicable
* a date attribute in the `Dates` section
* [ACR links](#223-acr-relations) in the `Categories and Subjects` section for [one (1) category and multiple subjects](#222-attaching-subjects-and-a-category)
  * not required for records of type **Review**
* a language selected from the `Language` input
* an abstract in the `Abstract` field, including, where possible, an English translation of the abstract where applicable
  * not required for records of type **Review**

All of these fields can be seen in the [Citation Curation interface](#22-the-citation-curation-interface) below

Many of these citation types also come with various **subtype** options with which to further characterize bibliographic records

[^ Up to Table of Contents](#table-of-contents)

---

##  2.2 The Citation Curation Interface

![image of isis cb citation curation interface](/media/citationCurationInterface.png)

The Citation Curation interface can be accessed through
* the ID of a citation in a set of citations in the [Citations Management Interface](#31-the-citations-managment-interface)
* the edit button on a citation's public page
* a link to a citation in an [ACR record](#223-acr-relations)
* a link to a citation in a [CCR record](#224-ccr-relations)

If you accessed the Citation Curation interface through the Citations Management interface and the citation is part of a set of citations in a list in the Citations Management interface, then you can use the navigation links (**Prev**, **Back to List**, **Next**) at the top of the Citation Curation interface to navigate through that list of citations
* When you [ingest a set of citations from an .rdf file](#12-doing-a-new-ingest), this is how you'll be curating that list of citations once you've finished [resolving authorities](#122-resolving-attached-authorities) and finalizing the ingest

If you make any changes to the textbox fields of the Citation Curation interface (e.g., `Title`, `Ed. det.`, `Volume`, `No./Episode`, `Pages`, `Extent`, `Abstract`, etc.), you must save these changes using the green **Save** button in the top-right of the Citation Curation interface


>Note: Fields to ignore:
>* the `Set` field refers to the dataset to which the citation has been ingested
>* the `Hist.` field details the citation's creation and ingest history and is auto-generated by the IsisCB system
>* the `Ed. det.` field contains information not part of the title, but important for locating the record
>* the `Status Expl.` field is auto-generated and need not be edited
[^ Up to Table of Contents](#table-of-contents)

---
###  2.2.1 Citation Curation Interface Views

---
####  2.2.1.1 Fields Tab

![image of isis cb citation curation interface](/media/citationCurationInterface.png)

The **Fields** tab contains the metadata most commonly used (much of which is required for each citation (see [Different Citation Types](#21-different-citation-types) for details))

The `Categories and Subjects` section lists color-coded tags of the attached subjects and category. [Subjects and categories can be edited](#222-attaching-subjects-and-a-category) using the pencil icon in the top-right corner of the section
* the topmost (light blue) tag represents the category assigned to the record
* the remaining tags below represent the various subjects assigned to the record
  * neon blue: time periods
  * peach: people
  * burnt orange: institutions
  * green-grey: geographic terms
  * pink: concepts

> *Why this peculiar combination of weird colors, I have no idea . . .*

[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.2 Attributes Tab

![image of isis cb citation curation interface attributes tab](/media/attributesTab.png)

The **Attributes** tab displays any attributes (e.g., dates) attached to a citation

[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.3 Linked Data Tab

![image of isis cb citation curation interface linked data tab](/media/linkedDataTab.png)

The **Linked Data** tab displays in data linked to a citation (e.g., a DOI or a URI)

[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.4 Related Citations Tab

![image of isis cb citation curation interface related citations tab](/media/relatedCitationsTab.png)

The **Related Citations** tab displays in [CCR relations](#224-ccr-relations) involving the citation, e.g.,
* a book it reviews
* a series it's part of
* a review it's reviewed by

[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.5 Related Authorities Tab

![image of isis cb citation curation interface related authorities tab](/media/relatedAuthoritiesTab.png)

The **Related Authorities** tab displays in [ACR relations](#223-acr-relations) involving the citation, e.g.,
* authors, editors, contributors, etc. responsible for it
* publishers, or journals hosting it
* subjects and categories tagged to it

[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.1.6 Tracking Tab

![image of isis cb citation curation interface tracking tab](/media/trackingTab.png)

The **Tracking** tab displays the tracking history of a citation, including whether the citation has been marked as **Fully Entered**, **Proofed**, or **Authorized**
* it also contains buttons in the top-right of the tab section where the citation can be manually marked as **Fully Entered**, **Proofed**, or **Authorized**
  * **do not** mark records as **Authorized**. This is the responsibility of the IsisCB editor admin

> Note: you can also manually change the tracking status to **Proofed** and the record status to **Active** using the orange **Proof and Activate** button next to the record status dropdown in the top left of the citation curation interface

> Note: though you can manually change the tracking status of a record in this tab it is more efficient to change the record tracking status in bulk using the [**Bulk Change**](#313-bulk-change-citations) functionality of the Citation Management Interface

[^ Up to Table of Contents](#table-of-contents)

---
###  2.2.2 Attaching Subjects and a Category

Attaching subjects and categories is perhaps the most important and most thoughtful part of the curation process. Subject tagging citations is what turns them from individual bibliographic references to materials into a richly interconnected conceptual network. And attaching categories creates the conceptual hierarchy for the print version of the bibliography.

[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.2.1 Attaching Existing Subjects

![image of isis cb subject and category tagging interface](/media/taggingInterface.png)

The Categories and Subjects interface is accessed through the pencil icon in the `Categories and Subjects` section of the Citation Curation interface. It is divided into 3 columns
* the contributor, title, and abstract are displayed for your reference in left column
  * we base the tags off of the information contained in the title and abstract
  * we may make inferences about tags from the abstract, for example, tagging the record with the concept `genetics` if it is about DNA, even though the word "genetics" isn't mentioned in the title or abstract
  * but we do not want to make extrapolated guesses about the record from the abstract
    * e.g., "I remember that in Denmark during this time period there was a lot of political upheaval so I'm going to add the tag `science and politics`"
* the currently linked subjects and category are displayed in the center column
* the authority search interface is in the right column

**Some notes about the subject and category authority search and guidelines for its use:**
* by default, searches in this interface include all kinds of authorities
  * but you can narrow the search by checking  
    * `C` for concepts
    * `P` for people
    * `I` for institutions
    * `G` for geographic terms
    * `T` for time periods
    * `All` for clearing the search filters
* the **magnifying glass icon** will force the search
  * this is useful when you're searching for an authority using only 2 characters (e.g., searching for `qi`), because the auto-search only initiates when 3 or more characters are entered
* the **Eras** tab is available for your convenience to scan the most commonly used time periods and save you from having to type them in
  * but it does not represent all of the time periods in the database
  * the numbered centuries go back to the `6th century, B.C.`
  * there are more general named time periods, e.g., `Ancient` and `Early Modern`
  * and there are time period authorities for various political epochs (e.g., `Edo period` Japan and `Song dynasty` China)
  * as well as other commonly used periodizations by historians, e.g. `Progressive era` for American history
* where applicable, **try to diversify the tags you apply across as many authority types as possible**
  * ideally, every record will be tagged with a **geographic term**, a **time period**, and several **concepts**
    * obviously don't force this, but if it's possible given then title and abstract information, then make sure to include it
* be tactical about including catch-all concepts like `Science and society`, `Science and religion`, or `Science and gender`. . . they can be a crutch for avoiding a more specific analysis of the conceptual model of the record. They can also be very useful, but try not to use too many of them on any given record. Adding too many basically says, "this citation is about everything"
* if you're struggling to find the authority you're looking for, or don't see one of the abstract's keywords in the search results, or simply looking for inspiration, use the **suggest feature**.
  * clicking the yellow `S` button to the right of each search result opens up the **Suggest** tab (to the right of the **Eras** tab)
  * the **Suggest** tab then displays a list of authorities that have been connected to the authority in question in other records in the database. This may help you find what you're looking for
* **Cross-references** help organize the bibliography by consolidating authorities and help guide our decisions when tagging
  * say you're looking for the tag `Ancient Greece` so you type that into the search box
  * the result is an authority called `Ancient Greece --> Use Ancient // Greece` of type **Cross-reference**
  * this means that, rather than having an additional authority for `Ancient Greece`, we use two tags, `Ancient` (**Time Period**) and `Greece` (**Geographic Term**) to capture this descriptor
* **Cross-references** also help with term ambiguity and synonymy
  * you may be looking for `Addiction` which seems fairly straightforward and common, but not finding that concept. The cross-reference authority will tell you that we use the concepts `Addictive behavior`, `Alcoholism`, and `Drug abuse` instead
* While on the topic of synonyms. You may want to wait until you are very familiar with the subject ontology of the IsisCB before creating new  authorities. For most ambiguous terms and synonyms we don't have cross-references to guide you.
  * you just have to slowly familiarize yourself with the usage of our ontology. For example, we don't have a concept for `Aliens`, we use `Extraterrestrial life` or `exobiology`
  * at first you may think, "Oh, there definitely needs to be a concept for `Aliens`" but try to check all possible synonyms first and consult with admins about terminology until you familiarize yourself with the ontology
  * some synonyms are pretty obvious and easy to intuit and check, like `Aliens` and `Extraterrestrial life`, others aren't so obvious, especially when they involve specialist jargon like `Teratology` or `Nosology`
  * we want to have a robust dictionary of descriptors so we can capture the nuance of the scholarship, but we don't want a cluttered disjointed mess of infinite particularity and no generalizability, so **use synonyms where you can**, **consult with admins** about synonyms you can't find, and then and only then [**create new authorities**](#33-creating-new-authorities)
* For **Geographic Terms**, only include the most specific descriptor possible. If a record takes place in Lagos, Nigeria (and not also in other places in Nigeria), use `Lagos` not `Nigeria`. Our geographic terms are organized into a hierarchical taxonomy, so our system knows that stories that take place in Lagos also take place in Nigeria and also take place in Africa, so we don't need to specify this through subject tagging
* **Concept/Serial Publication Confusion**
  * many concepts and serial publications are doppelgängers, especially for scientific and historical disciplines
  * e.g., `Ecology`, `Environmental history`
  * be mindful of the authority type in the blue box next to the authority name
  * it also helps to note that, as proper names, every word in the title of a serial publication is capitalized, but in concepts only the first word is capitalized
* **Gender** is a psychosocial construct and an historiographic analytic. Please do not tag every record that has anything to do with women with `Science and gender` or `Gender` just because it involves women. Would you tag every record that involves a man with `Gender`? No.



[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.2.2 Creating New Subjects

If you're sure that a new authority needs to be created to adequately tag a citation  and you're sure that that authority does not already exist in the database, then use the [Authority Creation interface](#33-creating-new-authorities) to add it to the database. You can access the Authority Creation interface from the Categories and Subjects interface by clicking the **+ Add new authority** link on the right-hand side of the interface.

[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.2.3 Attaching Categories

Attaching categories takes the longest to acquire of all the skills you'll use curating data in the IsisCB.

Consult the [Categories scheme](dummylink.com) for help choosing Categories

There are some guidelines that help with this process
* each citation is tagged with only one (1) category
* **Time Periods**
  * if a citation's time period spans two centuries, use the earlier century as part of the category
    * unless the citation spans only a very small portion of the earlier century relative to the later century, then use the later century
  * if a citation's time period spans 3 or more centuries, do **not** include a time period as part of the category
  * if the citation's time period involves the first half of the 20th century, or spans the first and second halves of the 20th century (and doesn't span any other century), use the time period **20th century** in the category
  * if the citation's time period involves the second half of the 20th century at all (and doesn't span the first half of the 20th century), use the time period **20th century late; 21st century** in the category
* **Disciplines**
  * If a citation can be placed in a scientific discipline (e.g., chemistry, physics, biological sciences, etc.) place it there, even if it bleeds into other categories
  * If a citation's categorical discipline is ambiguous, categorize it based on who you think will be hypothetically searching for that citation

[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.3 ACR Relations

**ACR (Authority-Citation Relationship) records** can be created from
* the [**Subjects and Categories interface**](#222-attaching-subjects-and-a-category) of the [**Citation Curation interface**](#22-the-citation-curation-interface)
* the **+ Create new relation** button of the **Related Authorities** tab of the Citation Curation interface
* the **+ Create new relation** button of the **Related Citations** tab of the [**Authority Curation interface**](#34-editing-authorities)
* the `Responsibility` section of the Citation Curation interface
* the `Hosting body` section of the Citation Curation interface

The **ACR records** attached to any **citation** can be found in the [**Related Authorities** tab](#2215-related-authorities-tab) of that citation's [**Citation Curation interface**](#22-the-citation-curation-interface)

The **ACR records** attached to any **authority** can be found in the **Related Citations** tab of that authority's [**Authority Curation interface**](#34-editing-authorities)
> Note: the [**Authority Curation interface**](#34-editing-authorities) is different from the [**Authority Creation interface**](#33-creating-new-authorities)

**ACR record** pages look like this:

![image of isis cb acr record interface](/media/acrRecordInterface.png)

The `Type controlled` field in the left-hand column of the ACR record interface establishes the kind of relation between the **citation** (top of the right-hand column) and the **authority** (bottom of the right-hand column), so you can read the above record as: "the **person** named `Marian Lydia Shorey` is a **subject** of the **article** titled `A New Season for Experimental Neuroembryology`"

[^ Up to Table of Contents](#table-of-contents)

---
####  2.2.4 CCR Relations

**CCR (Citation-Citation Relationship) records** can be created from
* the **+ Create new relation** button of the **Related Citations** tab of the [[**Citation Curation interface**](#22-the-citation-curation-interface)
* the `Containing Citation` section of the Citation Curation interface
* the `Linked Citation` section of the Citation Curation interface

The CCR records attached to any **citation** can be found in the [**Related Citations** tab](#2214-related-citations-tab) of that citation's [**Citation Curation interface**](#22-the-citation-curation-interface)

**CCR record** pages look like this:

![image of isis cb ccr record interface](/media/ccrRecordInterface.png)

The `Type controlled` field in the left-hand column of the CCR record interface establishes the kind of relation between the two citations. The `type`s of relationships specified in the `Type controlled` field of CCR records are all directional relationships, so you can read the above record as: "the **book** titled `Ether and Modernity: The Recalcitrance of an Epistemic Object in the Early Twentieth Century` **Is Reviewed By** the **review** titled `"The Ether Drag Show"`"

>Note: if you need to reverse the direction of the relationship described in a CCR record, simply click the **recycle arrows icon** between the two citations in the right-hand column of the **CCR Record interface**

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

To access the Export Citations interface, **click** the blue **Export** button between the **Bulk Select** and **Collections** buttons in the Citations Management interface (underneath the Search/Filter section of the page)

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
* **Create a new collection** of citations from the set of citations currently filtered in the view
* **Add to an existing collection** of citations the set of citations currently filtered in the view
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

![image of isis cb bulk edit authorities interface](/media/bulkEditAuthorities.png)

To access the Bulk Change Authorities interface, **click** the green **Bulk Change** button (between the **Export** and **Bulk Change (CSV)** buttons in the Authorities Management interface)

The Bulk Change Authorities interface allows you to
* Store creation data to citations
* Reindex authorities
* Delete duplicate Attributes

> Warning: The **Bulk Change Authorities** interface contains advanced functionality and should not be used without admin permission

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.4 Bulk Change CSV Authorities

![image of isis cb bulk change (csv) authorities interface](/media/bulkChangeCSVAuthorities.png)

To access the Bulk Change (CSV) Authorities interface, **click** the green **Bulk Change (CSV)** button (between the **Bulk Change** and **Bulk Select** buttons in the Authorities Management interface)

The Bulk Change (CSV) Authorities interface allows you to edit authority-related data in a spreadsheet or .csv file and then upload that (converted to .csv) spreadsheet or .csv file to amend several different data aspects, including
* Create Attributes
* Update Elements
* Create Linked Data
* Create AC Relations
* Create CC Relations
* Create Authorities
* Create Citations
* Duplicate Authority Merge and Redirect

> Warning: The **Bulk Change (CSV) Authorities** interface contains advanced functionality and should not be used without admin permission

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.5 Bulk Select Authorities

![image of the isis cb bulk select interface](/media/bulkSelectInterface.png)

You can access the Bulk Select Authorities interface by clicking the blue **Bulk Select** button between the **Bulk Change (CSV)** and **Authorities** buttons in the Authorities Management interface (underneath the Search/Filter section of the page)

The Bulk Select Authorities interface performs the same function as the `ID` field of the [Authorities Management Search interface](#321-searching-for-authorities), but if you need to grab a large number of citations by ID, then this interface is useful

Simply enter a comma-separated list of citation IDs and **click** the green **Select** button. You will be redirected to the Authorities Management interface with your search results

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.6 Export Authorities

![image of isis cb export authorities interface](/media/exportAuthoritiesInterface.png)

To access the Export Authorities interface, **click** the blue **Export** button between the **Create New Authority Record** and **Bulk Change** buttons in the Authorities Management interface (underneath the Search/Filter section of the page)

To export a set of authorities:
* enter an `Export Name`
* select the `Export Format`
  * .csv by default
* check whether you want to `Export metadata`
* select which authority fields you'd like to include in the export from the `Fields` multiselection box
  * hold `ctrl/cmd` (window/mac) to select multiple fields
* **click** the green **Create** button to begin the download

[^ Up to Table of Contents](#table-of-contents)

---
###  3.2.7 Authorities Collections

From the **Authorities** dropdown menu (to the right of the **Bulk Select** button in  the Authorities Management interface) you can
* **Create a new collection** of authorities from the set of authorities currently filtered in the view
* **Add to an existing collection** of authorities the set of authorities currently filtered in the view
* or **view collections** of authorities you've made in the past

To **Create a new collection**
* select the first option from the **Authorities** dropdown menu
* give the new collection a `Name`
* *(optional)* give the new collection a `Description`
* **click** the green **Create** button

[^ Up to Table of Contents](#table-of-contents)

---
##  3.3 Creating New Authorities

You may find yourself needing to create a new authority through
* the [authority resolution process](#122-resolving-attached-Authorities)
* the [citation curation interface](#22-the-citation-curation-interface)
* the [create new authority record]() function of the [Authorities Management interface](#32-the-authorities-management-interface)
* or, the [subjects and categories interface](#222-attaching-subjects-and-a-category)

The following sections walk you through the specifics of creating different types of authority with the [Authority Creation interface](https://data.isiscb.org/isis/curation/authority/add)

> Note: Unless they are proper names, we only capitalize the first word in authority names, e.g. a **serial publication** titled `Electron Microscopy` versus the **concept** of `Electron microscopy`

> Note: before creating any authority **make sure that authority doesn't already exist in the IsisCB authority system**. You can search for authorities by
>* clicking the blue **Explore, Authority Search** button (at the top of the Authorities Creation interface)
>* clicking the blue **Explore, Curation Authority Search** button (at the top of the Authorities Creation interface)
>* navigating to [the IsisCB Explorer](data.isiscb.org) and searching for the name of the authority

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

To create a new Geographic Term authority:
* select **Geographic Term** from the dropdown menu in the `Type` field
* **fill out** the `Name` field
* in a new browser tab, **navigate to** the [Geonames database](https://www.geonames.org/)
* **search** for the geographic entity you are creating an authority format (see image below)
  * be careful to **check** the `Feature class` and `Country` columns of the geonames search result to make sure you select the geonames record you're looking for
* **click** the linked name in the `Name` column of the geonames search to navigate to the geonames record you're looking for
* after geonames redirects you, **find** the geonames ID in the record URL
  * e.g., if the URL is `https://www.geonames.org/3932488/republic-of-peru.html`, the ID is `3932488`
* **copy** the geonames ID, **return** to the Authority Creation interface, and **paste** the geonames ID into the `URN (link to authority)` field
* **make sure** the `Linked Data Type` dropdown is set to **GeoNames**
* **set** the `Attribute Type` dropdown to **CountryCode**
* in a new broswer tab, **navigate to** the [country codes reference](https://www.iban.com/country-codes)
* **find** the two-letter country code for the country that either is, or contains, the geographic entity for which you are creating an authority
* **return** to the Authority Creation interface and **enter** that country code in the **CountryCode** attribute `Value` field
* **click** the green **Create & Continue** button in the upper-right corner to finalize the creation of the new Geographic Term authority

![image of geonames search interface](/media/geonamesSearchInterface.png)

[^ Up to Table of Contents](#table-of-contents)

---
####  3.3.5 Creating a New Serial Publication

![image of Isis CB serial publication authority creation interface](/media/createSerialPublicationAuthority.png)

To create a new Serial Publication authority:
* select **Serial Publication** from the dropdown menu in the `Type` field
* **fill out** the `Name` field
* **click** the blue **Google** button (between the **Wikipedia** and **VIAF** buttons at the top right of the interface)
* **locate** the official website for the journal (this will probably be through the journal's publishing company)
* **find** the ISSN of the journal
* **copy** the journal ISSN and **paste** it into the `URN (link to authority)` field
* **make sure** to set the `Linked Data Type` dropdown to **ISSN**
* **click** the green **Create & Continue** button in the upper-right corner to finalize the creation of the new Serial Publication authority

[^ Up to Table of Contents](#table-of-contents)

---
####  3.3.6 Creating a New Concept

![image of Isis CB concept authority creation interface](/media/createConceptAuthority.png)

To create a new Serial Publication authority:
* select **Serial Publication** from the dropdown menu in the `Type` field
* **fill out** the `Name` field
* **click** the blue **Wikipedia** button (between the **Explore, Curation Authority Search** and **Google** buttons at the top right of the interface)
* **copy** the URL of the concept's wikipedia page and **paste** it into the `URN (link to authority)` field
* **make sure** to set the `Linked Data Type` dropdown to **URL**
* **click** the green **Create & Continue** button in the upper-right corner to finalize the creation of the new Serial Publication authority

[^ Up to Table of Contents](#table-of-contents)

---

##  3.4 Editing Authorities

![image of the isis cb authority curation interface](/media/editAuthorityInterface.png)

You may access the Authority Curation interface
* by clicking the edit button on an authority's public page
* from the [ACR record interface](#223-acr-relations) where that authority is linked to a citation
* from the [Subjects and Categories interface](#222-attaching-subjects-and-a-category) of the [Citation Curation interface](#22-the-citation-curation-interface)

Even though the Authority Editing interface looks different than the Authority Creation interface, the functionality is basically the same.

In the Authority Editing interface, the different properties of the authority are nested under tabs:
* **Fields**
* **Attributes**
* **Linked Data**
* **Related Citations**
  * listing the citations connected to that authority through [ACR records](#223-acr-relations)
* **Related Authorities**
  * listing the authorities connected to that authority through AAR records
* **Tracking**

[^ Up to Table of Contents](#table-of-contents)
