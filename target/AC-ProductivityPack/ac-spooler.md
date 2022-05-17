---
title: Spooler | Microsoft Docs
description: Spooler slouží pro komunikaci systému Business Central s externími systémy nebo datovými zdroji.
author: ACMartinKunes
ms.service: dynamics365-business-central
ms.topic: Spooler
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: klicova slova, 
ms.date: 05/05/2021
ms.author: AC MartinKunes
---
# Spooler

Spooler is used for communication of the Microsoft Dynamics Business Central system with external systems or data sources.

It has two basic functions:
- Repository of unprocessed tasks and as an archive of communication documents.
- A tool for various types of communications and for processing incoming documents.

Communication can take place both from Business Central to an external system or vice versa from an external system to Business Central. Spooler currently allows the use of a total of 5 communication protocols (this number is constantly growing).

This module has a multifaceted use – in data synchronization between systems (catalogues, system settings within holdings), in query communication with external systems (e.g. for B2B or B2C systems), for archiving and processing of automatic electronic documents (order systems, electronic deliveries, invoicing, confirmations).

In addition to the function of a general communication tool, in cooperation with the Electronic Invoicing module, it allows to provide fully paperless invoicing to customers, which is also recognized by state control authorities.

This module is built separately and does not interfere with other modules.

## In Buffer and Out Buffer

The main part of the spooler are two tables in which individual records of communication, including files, are stored.

The interface of both tables is almost the same. Each record in both the IN Buffer and OUT Buffer tables is assigned a unique **Document ID** number. It also displays **Process Type** and **Document Type**. In addition, the record shows what task is being processed – **Task ID** field and by which agent it is processed – **Agent ID** field. The status of the record is indicated by the **Processed** field. It takes the values No, Yes, Expired, and Delayed. **Source System ID** field in the IN Buffer shows us where (from which system) the given record comes.

### Not sending Out Buffer entry

Unlike IN Buffer, there is an outgoing **Send sequence** field on the OUT Buffer - here it is possible to exclude the Buffer item from the calculation of the sending sequence by code. When sending documents from OUT Buffer, the OUT Agent tries to keep the sending sequence as follows:


- If an entry fails to be sent, no other items heading to the same destination will be sent (according to **Destination System ID** and **Interaction Parameter** fields from the recipient settings, regardless of the task).
- The functionality of the sending sequence works in such a way that if the **Interaction Parameter** field is filled in in the OUT Buffer, it is processed according to that field.

- Holding the sending sequence in a spooler has 2 basic reasons:
   1. They shall keep the sequence of documents to be sent.
   2. It saves time for the application server in case of malfunction of the connection - if it is necessary to send a larger number of documents to one place (for example, TCP address / port) and the connection is not working, so the attempt to send may take several seconds and it is undesirable for this attempt to be repeated with each item - in extreme cases it can stop the Application Server for several hours. It's a good idea to use the **Do not force the send sequence** field after careful consideration.

### Communication of In and Out Buffer
To view the communication tasks between the Out Buffer and the In Buffer, proceed as follows:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **IN Buffer** and then choose the related link.
1. The **In Buffer** page opens, where the function in **the Related** section is used by **Entry** function, where you will find the following functions:
   - Electronic Document Entries
   - In Buffer - Response
   - In Buffer - Response (incl. Archive)
   - In Buffer - Query
   - In Buffer - Query (incl. Archiv)

1. For Out Buffer, the options are similar.
1. In the displayed rows, it is always sorted by **Document ID**.

### Export a communication document

It is possible to export a document, display the document and display it as HTML on the IN Buffer and OUT Buffer forms - if an XSL template is defined for the spooler task. There is also the option to expire the record, change the note or manually send it to the archive.

To export a document, follow these steps:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **OUT Buffer** and then choose the related link.
1. The **OUT Buffer** page opens, where you can use the **Document Export** feature.

Another feature under the **Export Document** banner is the Check Electronic Signature and View Signature Certificate option.

### Raw record

If the given record is in the state Processed = No, it is possible to run the task manually from the form. This function is only available for In Buffer.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **IN Buffer** and then choose the related link.
1. The **In Buffer** page opens, where you can use the **Run Task** function.

The program then allows you to view an error due to which the task did not process. If the task did not process after manual execution, there may be a problem with the application server (e.g. user rights). On the **IN Buffer** form, there is a **Send Task** function that allows you to send the job from the IN Buffer.

### Manually insert a task into the IN or OUT Buffer

To insert a task into an IN or OUT Buffer, do the following:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **IN Buffer** and then choose the related link.
1. **IN Buffer** page opens, where you select the **Actions** section, then **Functions**, and finally the **Insert Task** function.
1. On the **Insert In Buffer** page, fill in the following fields as needed:
   - **Document** where the assignment document is selected. If a spooler task is found according to the document header, the data in the form is automatically set, e.g. Agent ID, Process Type, Document Type. If not, it must be manually set.
   - **Non XML** informs us whether the assigned document is not or is XML.
   - **Electronically signed** – if this field is checked, the document is electronically signed. This can be checked in the Features section by selecting **View Signing Certificate**. Below the same section there is also an option **Show date of signature**
   - The **Priority** field has only a record-keeping character.

## Archive - In a Out Buffer

To view the In or Out Buffer archive items, do the following:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Archived IN Buffer** and then choose the related link.

Entry will be accessed to the archive automatically during processing if this is set in the spooler task (Do not archive during processing, Do not archive at expiration) or in the spooler settings (Archive IN Buffer during processing and Archive IN Buffer during expiration, Archive OUT Buffer during processing and Archive OUT Buffer during expiration).

Items can also be accessed manually from the IN Buffer or OUT Buffer form using the **Move to Archive** function.

Another way to get items into the archive is using  **reports R4002900 Move IN Buffer to Archive** and **R4002901 Move OUT Buffer to Archive**.

## See also
[Spooler - Setup](ac-spooler-setup.md)
[AC Productivity Pack](ac-productivity-pack.md)  
[AUTOCONT Solutions](../index.md)