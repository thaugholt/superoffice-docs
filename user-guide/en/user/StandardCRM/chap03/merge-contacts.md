---
uid: help-en-merge-contacts
title: Merge contacts
description: Merge contacts
author: SuperOffice RnD
so.date: 06.29.2022
keywords: CRM
so.topic: help
language: en
---

# Merge contacts

[!include[Requirement](../../includes/note-req-manage-entities.md)]

If a physical person is registered as two different contacts in SuperOffice CRM, you can merge these contacts together. This might be desirable if the person has been registered under two different names at the same company (e.g. "Jonathan Clark" and "Jonathon Clarke"), or if the person has been registered at both his old and his new employer.

Project membership and activities will be moved to the target contact, and the source contact can be deleted or marked as a former employee.

Proceed as follows:

1. In the **Company** screen: Go to the **Contacts** section tab, select and right-click one or two contacts you want to merge, select **Manage contacts** and **Merge contacts**.  
    In the **Contact** screen: Go to the required contact, click the **Task** button ( ![icon](../../media/btn-Menu.png) ) in the contact card, and select **Manage contacts** and **Merge contacts**.  
    The **Merge contacts** dialog opens.

2. If you have only selected one contact, you need to select a contact under **To** (to search for a contact, start typing). The two contacts you want to merge are now displayed under **From** and **To**.

    > [!TIP]
    > If you want to switch the **From** and **To** contacts, click the ![icon](../media/Slå-sammen-Bytte.bmp) button.

3. Select one of the following under **Action on \[contact/company\] after merge**:
    * **Delete...**: If you select this option, the source contact is deleted after the merge. This may be appropriate if you have registered the same contact twice under the same company.
    * **Mark as former employee**: If you select this option, the source contact is marked as a former employee after the merge. This may be appropriate if a person has changed jobs, but you still want them registered under the old company.

4. Select one of the following under **Action on all existing activities and sales**:

    * **Leave all on...**. If you select this option, no activities or sales are moved.
    * **Move all to...**. If you select this option, all activities and sales are moved.
    * **Move all activities starting after**. Select this option if you want to transfer activities and sales starting after a specific date.

    > [!NOTE]
    > If you want to see the results before you merge the contacts, click **Show results**: ![icon](../media/Vis-resultat.bmp).

5. Click **Merge**. The contacts are merged, and project memberships and memberships of static selections are moved.

> [!NOTE]
> You cannot merge contacts (SuperOffice users) in your own company, but you can merge a contact from another company with one in your own company.

## Related topics

[Merge companies](Merge-companies.md)