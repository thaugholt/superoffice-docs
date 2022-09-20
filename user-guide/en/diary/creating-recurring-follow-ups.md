---
uid: help-en-creating-recurring-follow-ups
title: Creating recurring follow-ups
description: Creating recurring follow-ups
author: SuperOffice RnD
so.date: 06.29.2022
keywords: CRM
so.topic: help
language: en
---

# Create repeating follow-ups

It may happen that you want to create a series of appointments to occur at regular intervals, e.g. a weekly status meeting. Instead of recording these meetings one at a time, you can use the repeating follow-ups function. Do as follows:

1. Open the **Appointment**, **Task** or **Phone Call** dialog and enter the required information. [!include[See Appointment dialog](../includes/see-apt-dialog.md)]

2. Select the **Details** tab.

3. Click the word **Never** to the right of the **Recurrence** field. The **Repeating follow-ups** dialog opens.

4. At the top right of the dialog, the start date and time for the follow-up as well as the end time are displayed.

    ![icon][img1]<!-- Fix reuse ID=a3 -->

    Here you can only change the start date for the follow-up. If you want to change the time, you must first close the **Repeating follow-ups** dialog and then change the time in the **Appointment**, **Task** or **Phone call** dialog.

5. Under **Frequency** you specify whether the follow-up is to be repeated daily, weekly, monthly, yearly or at a user-defined interval. Then select further details for frequency in the field in the middle of the dialog. The options available here depend on what you select under **Frequency**:
    * If you select **Daily**, you can specify that the follow-up should repeat every working day, every day of the week, or at a user-defined interval, e.g. every other day. <!-- Fix reuse ID=a4 -->
        | Option | Description |
        |---|---|
        | Every workday (Mon-Fri) | Specifies that the follow-up will be repeated at the same time on each working day. |
        | Every weekday (Mon-Sun) | Specifies that the follow-up will be repeated at the same time on each day of the week, including the weekend. |
        | Every &lt;number&gt; day(s) | Here you enter a number to specify how many days should pass between each meeting, e.g. Every 6 days. |

    * If you select **Weekly**, you can specify that the follow-up should repeat at a user-defined weekly interval, e.g. every three weeks, and on which day of the week it should take place. <!-- Fix reuse ID=a5 -->

        | Option | Description |
        |---|---|
        | Every &lt;number&gt; week(s)| Here you enter a number to specify how many weeks should pass between each meeting, e.g. Every 3 weeks. |
        | &lt;weekday&gt;| Here you indicate on which weekday(s) the meeting should take place. |

    * If you select **Monthly**, you can specify on which day of the month the follow-up should repeat, e.g. on the 5th of the month, and a user-defined monthly interval, e.g. every 4th month. You can also specify that the follow-up should repeat, for example, on the fourth Wednesday of the month. <!-- Fix reuse ID=a6 -->

        | Option | Description |
        |---|---|
        | Day &lt;number&gt; **of every &lt;number&gt; month(s)** | Use this if you want the follow-up to take place on the same date each time. <br />For example: Day 20 of every 3 months. |
        | &lt;ordinal number&gt; &lt;weekday&gt; of every &lt;number&gt; month(s)| Use this if you want the follow-up to take place on the same weekday each time. <br />For example: The fourth Thursday of every 2 months. |

    * If you select **Yearly**, you can specify on which day and month the follow-up should repeat each year, e.g. every 23rd of September. <!-- Fix reuse ID=a2 -->

        | Option | Description |
        |---|---|
        | Day &lt;number&gt; **of &lt;month&gt;**| Use this if you want the follow-up to take place on the same date each time.<br />For example: Day 13 of April. |
        | &lt;ordinal number&gt; **&lt;weekday&gt; of &lt;month&gt;**| Use this if you want the follow-up to take place on the same weekday each time.<br/>For example: The fourth Thursday of August. |

    * If you select **Custom**, you can manually enter the dates you require. Select the day in the calendar and click the arrow (![icon][img2]) to add it to the list of selected dates. If you want to delete a date you have selected, select the date in the list and click **Delete**.

6. In the **Repeating follow-ups ends** field, choose whether the follow-up should stop after a specific number of times or after a specific date.

7. If you want to change one or more dates for a repeating follow-up manually, for example, if there is a conflict, you can do this in the list of selected dates at the far right of the dialog. You have the following options:
    * Move a date: Select the date you want to move, and click **Later** ( ![icon][img3] ) if you want to defer the follow-up by one day, or **Earlier** ( ![icon][img4] ) if you want to bring the follow-up one day forwards.
    * Add a date: Click the **Add** button below the list. The same calendar is then displayed as when you select **Custom**. Select the required date and click the arrow button ( ![icon][img2] ) to the right of the calendar to add the date to the list. Use the arrow buttons ( ![icon][img5] ![icon][img6] ) on either side of the month name in the calendar to display other months.
    * Delete a date: Select the date you want to delete, and click the **Delete** button below the list. The date will then be removed from the list of dates.

8. When you have finished entering dates for the follow-up, click **OK** to save the dates and close the dialog, or click **Cancel** to close the dialog without saving the dates.

9. Click **Save** in the **Appointment** dialog to save the changes you have made.

In the **Appointment**, **Task** or **Phone call** dialog, the text next to the **Recurrence** field will show what sort of repetition you have specified for the follow-up, e.g. **Monthly (23.09.2016 - 23.09.2017)**.

## What would you like to find out more about?

* [Edit repeating follow-ups][1]
* [Receive invitations][2]
* [Stop repeating follow-ups][3]

<!-- Referenced links -->
[1]: editing-recurring-follow-ups.md
[2]: receiving-invitations.md
[3]: stopping-recurring-follow-ups.md

<!-- Referenced images -->
[img1]: ../../media/icons/question.bmp
[img2]: ../../media/icons/pil-hoeyre.bmp
[img3]: ../../media/icons/pil-ned.bmp
[img4]: ../../media/icons/pil-opp.bmp
[img5]: ../../media/icons/kalender-pil-venstre.bmp
[img6]: ../../media/icons/kalender-pil-hoeyre.bmp