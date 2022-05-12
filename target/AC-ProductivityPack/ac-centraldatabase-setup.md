---
title: Centrální databáze | Microsoft Docs
description: Modul Centrální databáze umožňuje pomocí modulu Spooler synchronizovat číselníky mezi různými Business Cental databázemi a společnostmi. Způsob synchronizace (jaké tabulky, pole odkud a kam) je v Business Central parametrizovatelný.
author: ACMartinKunes
ms.service: dynamics365-business-central
ms.topic: Central database
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: klicova slova, 
ms.date: 05/05/2021
ms.author: AC MartinKunes
---
# Settings - Central Database

## Central Database Settings


For basic setup of the central database, proceed as follows:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Central Database Setup** and then choose the related link.
1. The **Central Database Setup** page opens, where you set the following fields:
   - **System ID** – used to identify the system - the name of the company as it will be used in the field of communications (it is important to set this name correctly in other cooperating companies).
   - **Central Database System ID** – the name of the company that serves as the controller for the communication-synchronization process. This company sets settings for "subordinate" companies. One company can receive settings from the central database and at the same time be the central database for other companies = there can be multiple central databases in the system.
   - **Central Database** – an internally used field that determines whether the company is itself a central databas The setting is crucial for decisions about sending synchronized data and about checks.
   - **Process type** set up the code that corresponds to the code specified in the spooler task settings in the Process Type field (*see Spooler Setup*). This code is part of the XML document and is used to determine whether the document can wait for processing.
   - **Process Type - setting of the code that corresponds to the code specified in the spooler task settings in the Process Type field (*see Spooler settings*). This code is part of the XML document and uses it to identify whether the document must be processed immediately and a response sent.
1. After you fill in the fields, close the page.


## Set up Destination Systems

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Destination Systems** and then choose the related link.
1. The **Destination Systems** page opens, where you fill in the following fields:
   - **ID** – company code for communication (must be identical in the whole communication chain)
   - **Description** – an indicative description of the company
   - **Database name** – the name of the database in which the company is located
   - **Company name** – the correct company name listed as the company name in its database (may be different from the codename)
1. After you fill in the fields, close the page.

## Central Database Table Setup

The application allows you to synchronize individual tables and their selected fields, you can also synchronize only the data falling into a particular filter. Synchronization can be independent and different for several companies.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Central Database Table Setup** and then choose the related link.
1. The **Central Database Table Setup** page opens, where you fill in the following fields:
   - **Disabled** – his field allows you to temporarily turn off sync while leaving the settings. It is mainly used for collision resolution or mass processing of centralized data (imports, renaming, etc.).
   - **Priority** – you can set the order for sending to sync.
   - **Central DB ID** – The ID of the system that controls the synchronization of the table. If this ID does not equal the system ID of the company in which we are located, the record cannot be changed.
   - **Table No.** – The number of the data table object in the system. The table can be selected from the code list of all tables. Synchronizing some tables is meaningless from the point of view of the system or may cause a collision.
   - **Table Caption** – is field is filled in automatically according to the table number field setting.
   - **ID** – independent code that is part of the primary key and allows you to set different synchronizations for one table (eg if I want to have a difference in the settings for 2 companies, where I want to allow some data to change and the other not). This code has no other link in the system and the user can set it as he wants (company name, group of companies, type of synchronization, etc.).
   - **Synchronization type** – this option takes two values – Push and Pull. The importance of this option is when creating new data into the system (changing data and deleting data are always sent automatically).
   - **Push** – option means that in the event of a change in the data, this data is immediately sent to the subordinate systems and updated there (the data is "pushed").
   - **Pull** – this option means that the newly created data is not sent immediately to subordinate systems, but the user can "reach" into the central database and choose which data from the headquarters he wants in his system (the data is "pulled").
   - **Fields** – this option determines whether some or all fields are synchronized (this field is related to the functionality of setting synchronized fields, see below).
   - **Allow Modify** – The field determines whether the user in the child database can change the value of the fields in the given record (checking on synchronized fields).
   - **Allow Insert** – the field determines whether the user in the child database can create a new record in the synchronized table.
   - **Synchronize By** – the field is used to optimize data transfer and system load; can be selected from the Limited number of records and All records values.
   - **Records limit** – the field is used to optimize data transfer and system load.
   - **Max Query Answer Records** – the field is used to optimize data transfer and system load; the system limits the number of records sent in response from the central database when querying synchronized data.
1. After you fill in the fields, close the page.

## Other settings
After the basic setting of the Central Database addon, it is necessary to set up additional areas. These are specific field settings for the central database tables.

### Set up Central Database Fields

The settings are used to define which specific fields of a given table and how we want to synchronize.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Central Database Table Setup** and then choose the related link.
1. The **Central Database Table Setup** page opens, where you select the row with the corresponding table.
1. Select **Related**, then **Setup** and select **Fields**, feature to fill in the following fields as needed:
   - **Field No.** – the number is selected from the object of the given table and is a unique identification of the field throughout the system (together with the table number). When changing in the system, the field numbers do not change.
   - **Field Caption** – This field is filled in automatically according to the field number field setting.
   - **Allow Modify** – The field determines whether a user in a child business can change the value of this particular field.
   - **Primary Key Field** – the field is used internally, the system sets the value itself. A field with this designation is always required to be synchronized
   - **Do Not Validate** – field determines whether the so-called validation process (execution of functions related to changing the value of the field) occurs after the synchronization of this field. This field must be set by a very experienced user of the system, the wrong setting will cause collision situations.
1. After the fields are filled out, close the page.

### Set up central database Receivers

The settings are used in defining communication for a specific record from the table synchronization settings (as described above, one table can be synchronized for different companies in different ways).

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Central Database Table Setup** and then choose the related link.
1. The **Central Database Table Setup** page opens, where you select the row with the corresponding table.
1. Select **Related**, then **Setup** and select **Receivers**, feature to fill in the following fields as needed:

   - **Disabled** – his field allows you to temporarily turn off sync while leaving the settings. It is mainly used for collision resolution or mass processing of centralized data (imports, renaming, etc.).
   - **Destination System ID** – binding to the settings of the target systems. The code determines which company will be the recipient of the synchronized data at the event.
   - **Table Synchronization Filter** – in the field (and auxiliary child form) you can set a general filter that determines which data will be synchronized (only data belonging to the filter).
   - **Table Permissions Filter** – In the field (and the auxiliary child form), you can set a generic filter that determines which data the user in the child company will be able to modify or create.
1. After the fields are filled out, close the page.

### Relations settings

Use the settings to specify relational bindings that ensure that related records (e.g., goods + item unit of measure) are synchronized when records from a particular table are synchronized.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Central Database Table Setup** and then choose the related link.
1. The **Central Database Table Setup** page opens, where you select the row with the corresponding table.
1. Select **Related**, then **Setup** and select **Relations**, feature to fill in the following fields as needed:

   - **Disabled** – his field allows you to temporarily turn off sync while leaving the settings. It is mainly used for collision resolution or mass processing of centralized data (imports, renaming, etc.)
   - **Related Table No.** – The number of the data table object in the system. The table can be selected from the dial list of already synchronized tables. This table is relationally or logically subordinate and its data is bound to the parent table
   - **Table Relations name** – this field is filled in automatically according to the setting of the Session table number field
   - **Table Filter** – A generic filter can be set in a field (and an auxiliary child form) to determine which data is synchronized as part of a relational synchronization
   - **Relation Exist** – a field that determines whether a relational binding is already defined
   - **Relation** – only the displayed form field, in the child form of which a relational binding can be defined

## See also

[Central Database](ac-centraldatabase.md)`  
[AC Productivity Pack](ac-productivity-pack.md)  
[AUTOCONT Solutions](../index.md)