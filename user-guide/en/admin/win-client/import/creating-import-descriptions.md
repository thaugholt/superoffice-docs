---
uid: help-en-creating-import-descriptions
title: Creating import descriptions
description: Creating import descriptions
author: SuperOffice RnD
so.date: 06.29.2022
keywords: Windows Client settings
so.topic: help
language: en
so.client: win
so.envir: onsite
---

# Create import descriptions

> [!NOTE]
> If you have already uploaded the import file and configured all the fields and settings, you should click **Save**. Clicking **New** will REMOVE all settings you have made for the import file.

To create an import description:

1. [!include[How to open import](../../includes/open-import.md)]

2. Click the **New** button at the top right of the screen. The **Import** screen is cleared.

3. Specify a data file in the **Import file** field.

4. Under **Field mapping**, specify which fields in the import file will be mapped to which fields in the SuperOffice database. (See [Field mapping][1].)

5. Under **Import settings**, the following options are available:

    * **File has header row**: check here if the file begins with a header row, i.e. a row not containing data.
    * **Add unknown list items to list**: check here if you want any unknown items to be included in existing lists in the SuperOffice database. If this option is unchecked, the unknown item will not be imported and the relevant field in the SuperOffice database will be left empty.
    * **Add as members to new selection**: check here if you are importing the company or contact data type and want the companies/contacts you are importing to be included in a separate selection. In this case you must also specify a name for the selection in the **Name** field.

    > [!NOTE]
    > If you choose **Add as members to new selection**, companies and contacts, as appropriate, which are included in the import, will be added to a new selection with the name you have specified. Companies and contacts which are not included (i.e. if you have chosen **Skip record** in the **Handle Duplicates** dialog) will not be added to the selection even if they exist in the import file.

6. To specify more advanced settings for the import, click the **Advanced** button. For more details, see [Specify advanced import settings][2].

7. Under **Handling of duplicates** you specify rules to cater for the existence of duplicates, i.e. if the same record exists in both the file you are importing and the database you are importing into. For more details, see [Duplicates][3].

8. When you have specified the required options, click the **Save** button.

    > [!NOTE]
    > You can perform an import without clicking the **Save** button, but your changes will then not be saved for later use.

9. Type the name for the new file in the dialog which opens, choose the folder you want to save it in and click **Save**.

> [!NOTE]
> You can also create a new import description by changing an existing description (see [Edit import descriptions][4]) and saving it with a new name.

<!-- Referenced links -->
[1]: field-mapping.md
[2]: specifying-advanced-import-settings.md
[3]: duplicates-import.md
[4]: editing-import-descriptions.md

<!-- Referenced images -->