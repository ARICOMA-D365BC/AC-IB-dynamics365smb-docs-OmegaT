---
title: Spooler | Microsoft Docs
description: Spooler slouží pro komunikaci systému Business Central s externími systémy nebo datovými zdroji.
author: ACMartinKunes
ms.service: dynamics365-business-central
ms.topic: Spooler - Setup
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: klicova slova, 
ms.date: 05/05/2021
ms.author: AC MartinKunes
---
# Spooleru Setup

Spooler is used for communication of the Business Central system with external systems or data sources.

## Basic Spooler settings

To set up a spooler, follow these steps:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Spooler Setup** and then choose the related link.
1. The **Spooler Setup** page opens, where there are setting and information fields:
   - **Source System**, which refers to the source system - how the system is identified in communication.
   - **Unprocessed In Task** and **Unprocessed Out Task** number of pending taks in In Buffer or Out Buffer.
   - **Calculate IN Buffer Doc. Size** a **Calculate OUT Buffer Doc. Size** determine whether to count the sizes of documents displayed in IN and OUT Buffers.
   - **Archive IN Buffer on Process** and **Archive IN Buffer on Expirate** determine when and if IN Buffer entries should be archived.
   - **Archive OUT Buffer on Processg** and **Archive Iou Buffer on Expirate** determine when and if OUT Buffer entries should be archived.
   - **Dont Search IN Msg in Archiv** determines whether to search for incoming message by unique GUID (Document ID) in archived entries.
   - **Dont Search Resp. in Archive** determines whether to search for an answer by the unique GUID (Document ID) in the archived entries.
   - **Maximal Entries in Bufffer** limits the number of items. If 0 is entered, it is an unlimited number of entries in Buffers.
   - **Certificate Pfx** – if you enter *, the field shows that an electronic signature is stored there.
   - The **Pfx Certificate Path** field is used if the certificate is not stored directly in the database.
   - **Pfx certificate password** - filled in if used.
   - **Do not enable electronic signing** is used to turn the use of electronic signatures on or off. Unchecked means do not use an electronic signature.

![Spooleru Setup](media/spooler-setup.png)

3. To import an electronic signature, use **the Pfx Certificate** and the **Impote...** function.
1. You can also view, export or delete your signature using **Export, Delete and View** features.
1. You can then close the page.


## Spooler Agents

To set up spooler agents, follow these steps:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Agents** and then choose the related link.
   The **Agents** page opens, where you must fill in the following fields:
   - The **Agent ID and Description** fields are used to differentiate between agents.
   - **Type** distinguishes agents
      - IN - used for incoming communications. It receives messages from the surroundings and stores them in the IN Buffer.
      - OUT - passes through the OUT Buffer and sends messages to the surroundings.
      - Procesing - passes through task in IN Buffer, processes IN Buffer task and stores them in out buffer.
   - **CU Agent** is set automatically, but can be overridden to another.
   - **Interaction Interval (s)** is used for active agents. Specifies the time interval in which it activates and performs the activity.
   - **Additional Iteration Parameters** are basically used by active agents. Some agents may have multiple parameters. For example, a disk agent can collect data from multiple directories.
   - For IN Agents, the **Default Task ID** field is used. If the Spooler job is not found by XML header, the default job is taken.
   - **Switch Agent After Number of Errors** is only for OUT Agents and Process Agents. If the agent fails to process the task (eg 5 errors), the ID of the new agent that will try to process the task can be set in the Change to agent field.
   - **Log** specifies whether and how it is written to the application log. Values can be Never, By Task, and Always.
   - **Reply only to XML** is for IN TCP Agents and shows whether to reply only to XML
   - **Interaction Method and Interaction Parameter** is only for IN Agents. The communication parameter is set according to the selected type of communication:
      - TCP – port [comma] Timeout
      - MSMQ – Name MSMQ
      - Pipe – Name named PIPE
      - HTTP – address http
      - Disk – path [comma] filter file

For disk and HTTP (timer) In agent, it is possible to set the default task ID for each Interaction parameter in order to distinguish what type of task the received message will be subsequently processed.

All agents are either passive or active. The active agent activates itself and performs some activity. The passive agent waits for a stimulus from the outside, for some interruption of the system, and then reacts to this change.

The passive agent runs alone on the application server. IN Agent TCP and IN Agent MSMQ are passive agents.

2. After filling in the fields, the page can be closed.
3. If a user needs to run the agent manually, they can do so in the **Process** group with **Run Agent** feature.

## Spooler Tasks

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Spooler Tasks** and then choose the related link.
1. On the **Spooler Tasks** page, you can create a row for a new task that contains the following fields:

- The **Task ID** field indicates the spooler job.
- The **Type** field determines whether the job is for IN Buffer (In) or out Buffer (Out).
- **Interaction type** field is used only for OUT tasks. The type of communication is similar to that of agents, ie. Disk, MSMQ, Pipe, HTTP, TCP and E-mail.
- **Description** is used to describe the task.
- The **Default priority** field indicates the order in which tasks are processed.
- The **Agent ID** field determines which agent will handle the spooler task. For IN tasks it will be a Process Agent and for OUT jobs it will be an OUT agent.
- The **XDR** field shows the existence of the XML document schema (*).
- The **Processing codeunit ID** field indicates which codeunitu the agent runs over the Buffer entry. For OUT tasks, the field is filled in automatically when selecting the type of communication
- The **Process Type** and **Document Type** fields recognize the task. It is used to find the task according to the header of the XML document in Buffer.
- The **Destination System** field can be filled in only for OUT tasks if the target system is not specified directly from the XML document header.
- The **Last Document Number** field uses the system internally, is not set and is used only for OUT jobs.
- In the **Expirate After** field, a duration (Duration variable) is entered.
- The **Log** field determines whether and how it is written to the application log. Values can be Never, By Task, and Always.
- The **Answer Type** fields are used only by IN jobs.
   - Confirmation - the task is inserted into the IN Buffer.
   - Result – the job is inserted into the IN Buffer and processing starts immediately.
- The **XSL Template** field is used to display the document in HTML.
- Use **Wait after numbers of errors** and **Wait after Error** fields to specify how many errors to wait for how long to try to process again.
- **On Insert Codeunit ID** – allows you to run codeunita when inserted into buffer.
- **Do not force send order** field – If this field is checked, the job items do not participate in the calculation to enforce the sending sequence (check only on jobs where it is explicitly undesirable to enforce the sending sequence. For example, for sending documents by E-Mail (here it does not have to be true that if one document is not sent (for example, because of the size), then the sending of others will not pass).
- The **Electronically Sign** field is for OUT jobs only. Specifies whether the job is automatically signed when inserted into Buffer.
- The **XML Encoding** field specifies how the XML document will be encoded.
- The **Dont Archive on Expirate and Dont Archive on Process** fields determine when and whether Buffer entries should be archived. These fields have a higher priority than the fields in the spooler settings.
- Use the **Dont Search IN Msg in archive** and **Dont Search for a Response in Archive** fields to secure communications. See the description of spooler settings.

The spooler target tasks appear on the Spooler task form on the Task - Target Systems button. Applies only to OUT jobs.

Here it is filled in with whom I communicate (field ID of the target system) and with what parameter (field Interaction parameter).

According to the selected type of communication, they set the parameters:

- TCP – IP address [comma] port [comma] Timeout
- MSMQ – Name MSMQ
- Pipe – Name named PIPE
- Disk – path [comma] extension
- HTTP – address http
- E-mail – email address

For the E-mail communication type, the e-mail applies: When inserting a task into the OUT Buffer, it is possible to reconfigure (override) the communication parameter for a specific task in the OUT Buffer. It is also possible to fill in the table T4002916 OUT Buffer Document to send multiple attachment files in one e-mail from one OUT Buffer entry.

On the Spooler Tasks form, you can use the Function button to export, import, view, or delete XDR and XSL templates for individual tasks.

3. After filling in the fields, the page can be closed.

## See also
[Spooler](ac-spooler.md)
[AC Productivity Pack](ac-productivity-pack.md)  
[AUTOCONT Solutions](../index.md)