---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: set_up_spf    # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description: How to set up SPF Record # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id}             # Your GitHub alias.
keywords:
so.topic: howto              # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
so.envir: cloud              # cloud or onsite
so.client: online              # online, web, win, pocket, or mobile
---

# How to set up SPF Record

Before creating the SPF record for your domain, it is important to find out what the server address for the mail service to be authorized (which is going to be permitted to send emails on your behalf).

[!include[ALT](../includes/envir-google.md)]

[!include[ALT](../includes/hosted-by-enom.md)]

**How to create DNS records for Office 365 when you manage your DNS records:**

You can follow the [general instructions from Microsoft for creating DNS records for Office 365][1].

## Open the domain settings for the Google domain

[!include[ALT](../includes/open-google-domain-settings.md)]

## Add the SPF record

1. Go to **Host Records** in the DNS console. The existing SPF record for your Google account is there by default.

![x][8]

2. We want to add **\_spf.online.superoffice.com** which contains correct records for both Mailgun clusters (EU and US). Since there only should be one SPF record - we need to combine the existing one with the new. The actual TXT record to add is **"v=spf1 include:\_spf.online.superoffice.com ~all"**.

  1. Click **Edit.** Update the existing record (text field) with the new combined record.

![x][9]

  2. Click **Save** to update the information.

![x][10]

[!include[ALT](../includes/note-dns-propagation-time.md)]

## Test a new SPF record

There are several tools online to use - to test your SPF record. Here we use [MX Toolbox][11].

1. Open the SPF tool:

![x][12]

2. Add your domain (the one that you are going to send our mailings as) and click **SPF Record Lookup**.

![x][13]

3. The result should show that **\_spf.online.superoffice.com** is included and pass the test for 'allow'.

### What’s the difference between ~all and -all?

Given many receivers are not actively bouncing mail based on SPF pass/fail, there isn’t a strong argument for either -all or ~all in SPF records. For a while, Hotmail was advising that senders who published a -all record would have better delivery. This led to -all became a de-facto standard for a lot of ESPs and bulk senders. More recently, there does not seem to be any benefit to publishing -all even at Hotmail (Outlook.com, live.com, etc).

What should I publish?

We recommend "~all" (soft fail if no matches) vs "-all" (hard fail if no matches) as a conservative measure. A soft mail means that the message will be tagged with a header documenting the failure, but will still be accepted. If you prefer a hard failure, ie "-all", then feel free to use that instead. There’s not a huge benefit to publishing -all and sometimes mail gets forwarded around. The one time we recommend a -all record is when a domain is getting forged into spam. Domain forgery can cause a lot of bounces. The number of bounces can be bad enough to take down a mail server, particularly those with a small userbase. Many ISPs will check SPF before sending back a bounce and so a -all record can decrease the amount of blowback the domain owner has to deal with.

<!-- Referenced links -->
[1]: https://support.office.com/en-us/article/general-instructions-for-creating-dns-records-for-office-365-e21a9a4a-7b14-42cb-b39b-03aee92da95f
2886048-0ziPiPMBJl50dyrE4AuUcfWmuAGb4WexjzApsYr6iF3OwywNJfNLX7Eg1xRWTH76-0/image.png
[8]: https://cs.superoffice.com/scripts/customer.fcgi/getAttachment/2886053-ncCTgbK1y6kOJ6PG3GwI1D1y8xytXfFKaQRaMiFs44xnHusWwW2ILezw7cYUIWPx-0/image.png
[9]: https://community.superoffice.com/contentassets/339951e0b8a14eaea7bac5de6befb518/2a906f41-12d9-450b-b38f-9c6b62ed18ec.png
[10]: https://community.superoffice.com/contentassets/339951e0b8a14eaea7bac5de6befb518/8e28749e-be90-498f-ad22-584bff9d37b5.png
[11]: https://mxtoolbox.com/
[12]: https://cs.superoffice.com/scripts/customer.fcgi/getAttachment/2889513-ZzjOj0KqPoGaGqNGhsjJdNdCfIQeCTrqEjOMQMDutyCbRyTohiOPZSRMQQN2xy1Y-0/image.png
[13]: https://community.superoffice.com/contentassets/339951e0b8a14eaea7bac5de6befb518/image7mle8.png