---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: office_365_set_up # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description: Setup - Office365 Cloud Office document Integration # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id} # Your GitHub alias.
keywords:
so.topic: howto # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
so.envir: cloud              # cloud or onsite
so.client: online             # online, web, win, pocket, or mobile
---

# Setup - Office365 Cloud Office document Integration

This article will help you set up the Microsoft 365 part of the integration between Microsoft 365 and SuperOffice CRM Online.

Setting up Office365 SharePoint Integration has 2 parts:

* How to setup Microsoft 365 to integrate into CRM Online:
  * Check if your SuperOffice CRM Online tenant is ready (pre-requisite step)
  * Configure the integration in your Office365 SharePoint (steps 1 - 3)
  * Enable the integration for your CRM Online site (step 4)
* Configure your templates in SuperOffice Admin (in [this article][1])

If you would like to get assistance configuring the integration, sign up for [Microsoft Office 365 Integration in the SuperOffic App Store][2]

## Before you begin

Ensure you meet the [prerequisites](requirements.md) and read the [security considerations](security.md).

* During set-up, some details must be collected. These details will be used as parameters for setting the new configurations for your SuperOffice CRM Online site.
  * Your SuperOffice Online customer-specific URL, Cust ID (found in the browser URL while logged into SuperOffice Online), for instance, `http://online.superoffice.com/cust8123/`
  * **Write down the number of the "cust"-part of the URL as “Cust ID”**

* To create new content types (see step 2), you need the SharePoint settings to "allow user to run custom scripts" activated < 24 h. before setup. You may perform the other steps in the meantime / create new content types at a later time.

* How to activate 'Custom Script':

1. Go to SharePoint admin center > settings tab > Custom Script section >
2. Set settings to "Allow users to run custom script on self-service created sites"

![x][3]

For more information:

* [New Microsoft 365 admin user interface][4]
* [Old Office365 admin user interface][5]

## Step 1 - Create a document library in your Microsoft 365 SharePoint library

> [!NOTE]
> The *SuperOffice Archive* folder needs to be a **document library**, and this document library needs to be located on the root of the SharePoint site, and not as a sub-site or a virtual site. See [troubleshooting tips](troubleshooting.md) for more information.

1. Open Microsoft 365 and log in as an admin user, go to Microsoft 365 “Admin”.

![x][6]

2. Go to SharePoint under “Microsoft 365 admin center” -> Admin centers

![image18cb.png][7]

3. Open the root area of your SharePoint tenant – by choosing 'Sites' -> 'Active sites' from the left-hand menu.

![imagesgm93.png][8]

**Write down this URL as “SharePoint domain name URL=”**

Example: `SharePoint domain name URL=https://[your_domain_name].sharepoint.com`

4. Click the root address (`https://[your_domain_name].sharepoint.com`) from the **Active sites** list.

![x][9]

5. Open **Site contents** from the menu

![imagetrxas.png][10]

6. Create a document library (used for SuperOffice documents) in the **root** area:
    1. Click **New** and choose **Document library**.
    1. Enter a name for your document library. **Example:** `SuperOffice_Archive`

    **Write down this name as "SO Archive Document Library Name="**

    This is the name of the document library. It will be the relative path of your document library to the root folder: `https://[your_domain_name].sharepoint.com _SuperOffice_Archive/`

Example: "SO Archive Document Library Name=/SuperOffice\_Archive/"

Make sure the document library exists on Root of SharePoint, and have correct access rights (minimum "Edit" ) for your users before continuing.

7. Create a 'template' folder (used for SuperOffice templates) in the SuperOffice Document library:
    1. Click **New** and choose **Folder**.
    1. Enter a name for your template folder. For example, *Template*

    **Write down this name as “Template Folder Name=”**

![imageujv6m.png][11]

Folder for templates, created inside the SuperOffice Document library For example, *Template Folder Name=Template*

Make sure the folder exists, and have correct access rights for your users before continuing.

## Step 2 – Setting up Document Content types in Microsoft 365 SharePoint

For creating new blank documents, spreadsheets, and presentations in SuperOffice CRM Admin (from a SharePoint template), we need to define several content types in SharePoint.

To create new content types, you need the SharePoint settings to "allow user to run custom scripts" activated < 24 h. before setup. You may perform the next steps in the meantime / create content types at a later time if you prefer.

This selection will fail if SuperOffice 'content types' are not set up in SharePoint:

![x][12]

1. Open Microsoft 365, and log in as an admin user, go to "Microsoft 365 admin center”
2. Go to Sharepoint under “Admin centers”
3. Open "Active sites", and open the root area – by clicking the link `https://[your_domain_name].sharepoint.com` from the list
4. Click the settings wheel-> Site Settings -> Site Content Types.

![imageu49ea.png][13]

![x][14]

5. Click Create

![x][15]

6. Set:
    1. Enter 'SuperOffice Blank Document' as name
    1. Choose “Documents Content Types” / “Content types for documents” under 'Select parent content type from:'
    1. Choose “Document” under 'Parent Content Type'
    1. Enter SuperOffice as Group (Create the group if it's non-existing).

![x][16]

7. Click OK

8. Navigate the list to your newly created content type and open it. Click Advanced settings

![x][17]

9. Select 'Upload a new document template:'. Choose a blank document from your computer. (Either download a pre-created blank [.docx][18] document or create a blank document from Office and stored locally)

10. Click OK

11. Repeat step 6 - 13 for

* SuperOffice Blank Spreadsheet ([.xlsx][19]
* SuperOffice Blank Presentation ([.pptx][20]

### If you get an access error

**For new UI:**

1. Read [New Microsoft 365 admin user interface][21]

2. Go to the [Settings page of the new SharePoint admin center][22], and sign in with an account that has [admin permissions][23] for your organization. At the bottom of the page, select **classic settings page**.
Confirm whether the settings are configured to "Allow users from running custom script".

**For old UI:**

1. Read [Office365 admin user interface][24]

2. Go to SharePoint admin center > settings tab > Custom Script section >
confirm whether the settings are configured to "Allow users from running custom script".

    * Set them to "Allow users to run custom script" to see the outcome. The SharePoint settings "Allow user to run custom scripts" can take < 24 h. before activated. You may perform the other steps in the meantime / create the content types at a later time.

## Step 3 – Adding the SuperOffice Integrator App in Office365 Sharepoint

### 1. Add or upload the app manually

Since we’re not in Office Store, we have to do this manually:

1. In “SharePoint admin center” - click “apps” from the menu
2. Open "Customer apps" from the “Active sites” page (click URL) or go via "Advanced" and choose “Apps” -> "Apps catalog"

![imagedtyeq.png][25]

![imagev7ojr.png][26]

![image69pt4.png][27]

If you don’t have an **App Catalog** from before – [choose to create a new one][28]

3. Download the SuperOffice SharePoint App [SuperOffice.Office365.Integrator.app][29] locally

4. Choose “Apps for SharePoint” in the menu. ![imagekoepi.png][30]
5. Click upload and choose the local file *SuperOffice.Office365.Integrator.app*

![imageydark.png][31]

6. Click ok. The App is now Uploaded – and available to be used on your SharePoint site within about 10 minutes.

![imagem7t19.png][31]

### To use the App on your SharePoint site - Add the App to the site

1. Go back to Grup Area: Open the Root area – by opening the link `https://[your_domain_name].sharepoint.com` from the **Sharepoint admin centre** menu by clicking the link `https://[your_domain_name].sharepoint.com` from the list

2. Click **Site contents** in the menu:

![image6e0ta.png][32]

3. Click **New** from the dropdown inside the Grup Area, and choose **App**

Inside “Your Apps” – Apps you can add – you should now see “SuperOffice Online Integration” (if it is not in the list yet - it might take a few minutes before it is available. Try again in a few minutes)

4. Click on it to open the app details

![imagebnc9j.png][33]

(if you are not able to add it yet - it might take a few minutes before it is available to add. Try again in a few minutes)

![imagezfo3m.png][34]

5. Add it by clicking **Trust It** to approve.

![image61nqk.png][35]

Once added - the SuperOffice Integration app should now be in the Group Area.

![x][36]

6. SharePoint users who will use this app for logging in to CRM Online will need "read" access to the root folder of SharePoint (see [Troubleshooting tips](troubleshooting.md) for more information and options on how to enable it)

## Step 4 – Notify SuperOffice to activate Microsoft 365 document integration

To turn on the Microsoft 365 SharePoint integration for your CRMOnline tenant, submit the following details:

* "Cust ID"
* “SharePoint domain name URL”
* “SO Archive Document Library Name”
* “SO Template Folder Name”

**NOTE!** Once we receive the form submission, we will activate the feature as soon as we are able to, and the feature will then be ready to use the following day. (Your site must be ‘recycled’ to get the new configurations)

**Use [this form][37] for submitting the details to us.**

You will get a notification from SuperOffice R&D Services when the Microsoft 365 SharePoint integration is activated.

When it is ready to use, you may continue to set up the templates, to make use of the Microsoft 365 SharePoint integration (as described in [this article](../configure-cloud-document-handling.md))

<!-- Referenced links -->
[1]: ../configure-cloud-document-handling.md
[2]: https://online.superoffice.com/AppStore/superoffice-as/office-365-integration
[3]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/o365customscripts.png
[4]: https://docs.microsoft.com/en-us/sharepointallow-or-prevent-custom-scriptredirectSourcePath=%252fen-us%252farticle%252fAllow-or-prevent-custom-script-1f2c515f-5d7e-44a-9fd7-835da935584f
[5]: https://social.technet.microsoft.com/wikicontents/articles/37533.sharepoint-online-how-to-enable-custom-script.aspx
[6]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imagebx1f.png
[7]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/image18cb.png
[8]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imagesgm93.png
[9]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/image4e5im.png
[10]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imagetrxas.png
[11]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imageujv6m.png
[12]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/o365createnewtemplate.png
[13]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imageu49ea.png
[14]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/o365sitecontenttypes.png
[15]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/o365sitesettingscreatecontenttypes.png
[16]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/o365createdocumentcontenttype.png
[17]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/o365contenttypeadvanced.png
[18]: https://community.superoffice.com/globalassets/technical-club/documentation/setup-cloud-office/blank.docx
[19]: https://community.superoffice.com/globalassets/technical-club/documentation/setup-cloud-office/blank.xlsx
[20]: https://community.superoffice.com/globalassets/technical-club/documentation/setup-cloud-office/blank.pptx
[21]: https://docs.microsoft.com/en-us/sharepoint/allow-or-prevent-custom-script?redirectSourcePath=%252fen-us%252farticle%252fAllow-or-prevent-custom-script-1f2c515f-5d7e-448a-9fd7-835da935584f
[22]: https://admin.microsoft.com/sharepoint?page=migrationCenter&modern=true
[23]: https://docs.microsoft.com/en-us/sharepoint/sharepoint-admin-role
[24]: https://social.technet.microsoft.com/wiki/contents/articles/37533.sharepoint-online-how-to-enable-custom-script.aspx
[25]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imagedtyeq.png
[26]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imagev7ojr.png
[27]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/image69pt4.png
[28]: https://community.superoffice.com/en/technical/documentation/prepare/crm-online/office-365-google-apps/setup---o365-integration/#accordion033
[29]: https://community.superoffice.com/globalassets/technical-club/documentation/setup-cloud-office/cloud-office-for-superoffice-crm-online---superoffice.app
[30]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imagekoepi.png
[31]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imageydark.png
[31]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imagem7t19.png
[32]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/image6e0ta.png
[33]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imagebnc9j.png
[34]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/imagezfo3m.png
[35]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/image61nqk.png
[36]: https://community.superoffice.com/contentassets/6172620ecdb4492292b5962b7c455735/o365appadded.png
[37]: https://crm.superoffice.com/scripts/customer.fcgi?action=formFrame&formId=20