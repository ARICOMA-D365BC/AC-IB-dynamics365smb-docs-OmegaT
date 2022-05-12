---
title: Centrální databáze | Microsoft Docs
description: Modul Centrální databáze umožňuje pomocí modulu Spooler synchronizovat číselníky mezi různými Business Cental databázemi a společnostmi. Způsob synchronizace (jaké tabulky, pole odkud a kam) je v Business Central parametrizovatelný.
author: ACMartinKunes
ms.service: dynamics365-business-central
ms.topic: Central database setup
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: klicova slova, 
ms.date: 05/05/2021
ms.author: AC MartinKunes
---
# Central Database

The **Central Database** module allows you to use the Spooler module to synchronize code lists between different Business Central databases and companies. The method of synchronization (what tables, fields, from where and where) is parameterizable.

The module is designed to synchronize data between different data sources – it can be two companies in one database as well as 2 companies in databases distant from each other. The setup is always a master-client between two data company.

The application allows you to synchronize in all directions and selectively (see setup). The application does not check possible data collisions (a special case is the validation of synchronized data) or possible cyclic synchronization (the setting is always only between two data sources).

The application can be used not only between individual Miscrosoft Business Solution – Business Central systems, but also for data synchronization with external systems (e.g. B2B applications, customer applications, specialized production software, etc.).

The synchronization process can take place online at the moment of data change (a change document is generated for the given record), according to the user's choice as a complex package of synchronized data or automatically as a data package at periodic intervals (using the Shareplan module).

Data communication about changes or synchronization takes place using structured XML documents.

Note: You cannot perform a rename operation (change the value of the
of the primary key fields).

## Using Celntral Database - Synchronization

The use itself consists in correctly setting up and starting the synchronization of tables. For more information on setting up Central database, see **[Setting Up Central Database](ac-centraldatabase-setup.md)**.

Synchronization either takes place automatically when changes are made to the defined data tables or you can start it manually.

To start manually, follow the procedure below:
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Central Database Tabble Setup** and then choose the related link.
1. The **Central Database Settings** page opens, where you can choose **Actions** and **Synchronize** feature.

When you synchronize manually, you can use filters to specify exactly what tables, where and where to sync them. This option is used mainly when synchronizing existing data into new systems (migration and parameterization).

## See also
[Central Database - Setup](ac-centraldatabase-setup.md)
[AC Productivity Pack](ac-productivity-pack.md)  
[AUTOCONT řešení](../index.md)