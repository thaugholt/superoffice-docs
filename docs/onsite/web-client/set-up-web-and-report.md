---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: set_up_web_and_report    # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description:                    # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id}             # Your GitHub alias.
keywords:
so.topic: howto               # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
so.envir: onsite                # cloud or onsite
so.client: web              # online, web, win, pocket, or mobile
---

# Setup Web and Reports

If you are running Web with remote Netserver web services, this must be set up on the server running Netserver web services.

When you have completed the SuperOffice Web installation, the SuperOffice Product Configuration program is launched automatically, provided you selected I would like to launch SuperOffice Web Configuration in the final step of the installation. Otherwise, you can start it manually by selecting Start > All Programs > SuperOffice > SuperOffice Web > Product Configuration (instance name), where "instance name" is the name of the instance you want to configure (also referred to as the application title).

## Configure Reporter

After the configuration of the application, the Reporter configuration should start automatically.

![x][1]

In the Reporter dialog, do the following:

![x][2]

1. Add an ODBC data source and type the name in the ODBC field
2. Enter the table prefix of the database
3. The impersonate user can either be:
    * a domain user with read/write access to the document archive and rights to log on to the web server or
    * a local user on both the web server and the archive server with the same user name and password, and with read/write access to the document archive.

The latter will be the case for workgroups or other situations where a domain controller is not available to the server running Web or the server holding the document archive.

In the Domain field, specify the name of the domain if a domain user has been specified, or the name of the local computer Web is installed on if you have specified a local user. The User and Password fields should contain the user name and password for the user being impersonated. Click the Validate button to verify that you have entered the password correctly.

 ![x][3]

In the SuperOffice Product Configuration Complete dialog, you get a summary of the installation settings you have selected. You may click Back to go back and make any necessary changes. When you are done, click Finish.

## Troubleshooting

### We get "Error code: 3, Error: System.ApplicationException: Failed to impersonate user 'xxx'. Error message:, Last error; 87 at SuperOffice.Security.Util.WindowsIdentityHelper.LogonUser(String userName, String domain, String password, LogonType logonType"

Reporter will use the Impersonate User from Archive domain, archive user and archive password (web.config), and this user must have access to log on to the server where the web client is running. This user or the group he belongs to must be members of the list "Log on locally" in security policy. If this right is missing we will receive error 87 from Windows.

![x][4]

### All users receive a _Error message: Unable to get file stream._ when they try to preview a report

Check the rights on the Web temporary path folder (location is found in the [web.config][5] file under the Documents section).

```xml
< !-- Location of temporary folder for streaming files.
This path must resolve to the same location for farms/clusters. -- >

< add key="TemporaryPath" value="C:\\temp-path" / >
```

[1]: https://community.superoffice.com/contentassets/7aeedd2a7deb4b7b826a9c5f97fb2d3e/sixwebreportconfig1.jpg
[2]: https://community.superoffice.com/contentassets/7aeedd2a7deb4b7b826a9c5f97fb2d3e/sixwebreportconfig2.jpg
[3]: https://community.superoffice.com/contentassets/7aeedd2a7deb4b7b826a9c5f97fb2d3e/sixwebreportconfig3.jpg
[4]: https://community.superoffice.com/contentassets/7aeedd2a7deb4b7b826a9c5f97fb2d3e/allow-log-on-locally.png
[5]: https://community.superoffice.com/en/technical/documentation/administration/config-ini/webconfig/