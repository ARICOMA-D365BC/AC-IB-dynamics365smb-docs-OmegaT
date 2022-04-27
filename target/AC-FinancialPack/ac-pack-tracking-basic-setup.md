---
title: Autocont - Pack Tracking Basic Setup | Microsoft Docs
description:  This section describes Autocont Pack Tracking Basic AddOn Setup
author: ACPJanousek
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Pack tracking, setup, rapidstart, item
ms.date: 01/31/2020 TODO
ms.author: v-pejano
---

# Pack Tracking Basic (EKOKOM) - Setup
To ensure the functioning of the add-on module **Pack Tracking Basic**, it is necessary to perform the necessary setup steps.

## Establish a Packaging Statement
The necessary number of different Packaging Statements can be created in the system. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Packing Statements** and then choose the related link.

> [!NOTE]  
> If you are going to import the provided EKO-KOM parameterization files, you must create a Packaging Report with the code **EKO-KOM**.

## Parameterization of the EKO-KOM Packaging Report
The add-on module Pack Tracking is supplied with excel files *ekokom_def.xlsx* and *ekokom.xlsx* containing the parameterization for **EKO-KOM Packaging Statements**.  
The parameterisation files can be uploaded to the system using the **RapidStart Service**.<s

## Packing Statement Element Definition
For each created report, it is necessary to define its elements. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Packing Statement Element Def.** and then choose the related link.
Elements in the report can be grouped into positions on the report. A total of 10 positions can be defined (grouping of elements). Elements within a position are further assigned a code.

Packing Statement Element Definition form fields:

| Field | Description |
|---------------|---------------|  
| **Statement Code** | The report code created in the previous step |
| **Position** | User-specified group of schedule elements |
| **Code** | Element code within a position |
| **Description** | Description of the schedule element |
| **Statement Placement** | Text descriptive information |


For example, you can create a table with the following values:

| Reporting code | Position | Code | Description |
|----------|----------|----------|----------|
| EKO-KOM | P1 | 1 | Single-use packaging |
| EKO-KOM | P1 | 2 | Reusable packaging |
| EKO-KOM | P2 | 1 | Charged |
| EKO-KOM | P2 | 2 | Prepaid |
| EKO-KOM | P2 | 3 | Unpaid |

## Creating Elements in a Packing Statements (Defining a Custom Statement)

Definice vlastního výkazu se provádí založením prvků Výkazu obalů. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter ** Packing Statement Elements** and then choose the related link. In the form, individual statement lines are defined by selecting from previously defined elements for each statement position. The *Description* field is then added by the system depending on the field on the **Packing Statement Element Definition**page.

For example **Packing Statement Elements** page might look like this:

| Reporting code | Code | Description |
|---------------|---------------|---------------|
| EKO-KOM | 13 | Single-use packaging free of charge |

## Creating exceptions in the Packaging Statements

In each **Packaging Statement** that you create, you can define exceptions, specified by the status of the lines in the Item journal, that will not be included in the report. Choose the **Lightbulb that opens the Tell Me feature.![Tell me what you want to do](media/ui-search/search_small.png ", icon, enter ")Packing Stat. El. Exceptions</g4> and then choose the related link.  The exception is defined by the data entered in the **Movement Type**, **Field no.**, **Field Value** and **Position** fields (in the report). You must also specify the **Element Code** to create an exception.

## See also
[Pack Tracking Basic (EKOKOM)](ac-pack-tracking-basic.md)  
[Financial Pack](ac-finance-pack.md)
