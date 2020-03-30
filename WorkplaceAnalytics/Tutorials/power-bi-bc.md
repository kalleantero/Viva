---

ROBOTS: NOINDEX,NOFOLLOW
title: Power BI Business Continuity Dashboard
description: Use the Power BI Business Continuity Dashboard to visualize predefined query data from Workplace Analytics in Power BI
author: madehmer
ms.author: 
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Power BI Business Continuity Dashboard

You can use the Power BI Business Continuity Dashboard populated by Workplace Analytics data to gain insights into how your organization is adapting to business disruptions, such as a switch to 100 percent remote work.

This dashboard directionally highlights where disruption to ways of working might be having the largest impacts, offering a measurable starting point for helping leaders understand where they might use tools and processes to support and sustain new ways of working.

The following are a few of the top-level business questions asked by leaders that this dashboard enables you to visualize and explore.

|Business question |Analysis |
|-------------|------------------|
|How is business as usual changing? |<ul><li>How are activity levels changing in response to a disruption? </li><li>Which lines of business are more impacted? </li></ul>|
|How are employees adapting to the disruption?  |<ul><li>How many employees are experiencing significant shifts in workweek span and collaboration demand? </li><li>How are employees shifting their work patterns across the collaboration activities, such as calls and chats? </li></ul>|
|Are we maintaining external relationships? |<ul><li>How much has changed with customer, partner, and vendor collaboration? </li><li>Which lines of business are experiencing the largest increases and decreases in external demand? </li></ul>|
|How do you foster employee community and engagement? |<ul><li>Are your managers regularly checking in with their employees about their wellbeing and health? </li><li>Are employees managing to stay engaged while in an all-remote work environment? </li></ul>|

To populate the Business Continuity Dashboard in Power BI, you must set up and successfully run the predefined **Business Continuity** and **Hourly Collaboration** queries in Workplace Analytics. The results of these queries will refresh your downloaded Power BI dashboard on a weekly basis.  

After you successfully run these required queries, you'll see the Power BI template as an available download option for the Business Continuity query. This template is required to create the dashboard in Power BI. After you download the Power BI template, you can then connect the query data from Workplace Analytics to the dashboard in Power BI.

When the Business Continuity Dashboard is populated with data, you can use it to visualize, explore, and report about your organization's workplace patterns and trends.

## Prerequisites  

Before you can run the queries and populate the dashboard in Power BI, you must:

* Be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics.
* Have Power BI Desktop installed. See [Install and run Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-getting-started#install-and-run-power-bi-desktop) for details.

## Setting up the dashboard

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Queries**.
2. Under **Start from preselected filters and metrics**, select **Business Continuity** to open this predefined query, which contains the first set of required metrics to populate the dashboard.
3. Select or confirm the following query settings:

   * **Query Name** - Business Continuity
   * **Group by** - Week
   * **Time period** - Last 6 months
   * **Auto-refresh** - Enable the setting
   * **Meeting exclusions** - Select the preferred rule for your tenant

   > [!Important]
   > * The dashboard is designed to show you how a disruption can change your organization's work patterns. For best results, select **Last 6 months** for the **Time period** to include time before and after the disruption.
   > * If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize collaboration patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all of the possible charts. You can select **Cancel** to retain the metric.

4. In **Select filters**, select **Active only** for "**Which measured employees do you want to include?**" Optionally, you can further filter the employees in scope for the dashboard. For more details about filter and metric options, see [Create a Person Query](./person-queries.md).
5. In **Organizational data**, keep the preselected **Organization**, **LevelDesignation**, and **TimeZone** attributes that the dashboard requires. You can then select any other attributes (columns) to include in the dashboard.

   > [!Important]
   > If you remove the required, preselected Organizational data attributes, you might disable one or more Power BI charts.

6. Select **Run** to run the query, which might take several minutes to complete.
7. Repeat the previous steps and select the **Hourly Collaboration** query in Step 2, which requires the same filters and **Organizational data** attributes as the **Business Continuity** query. And then in Step 3, name the query **Hourly Collaboration**.
8. In **Queries** > **Results**, after the queries successfully run, select the **download** icon for the **Business Continuity** query results, and then select **PBI template**, which downloads the template and copies the OData link to the clipboard.
9. Select **OK**, and then open the downloaded **Business Continuity Power BI template**.
10. If prompted to select a program, select **Power BI**.
11. When prompted, you must paste the OData links for both queries into their respective input boxes.

    * In the Workplace Analytics **Queries** > **Results** page, select the **link** icon for each query, and copy the generated OData URL link.
    * In Power BI, paste each link into its respective input field.

12. In Power BI, set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Workplace Analytics data.  
13. Select **Load** to import the query results into Power BI.
14. If you're already logged in to Power BI with your Workplace Analytics organizational account, your will data load and the dashboard visualizations will populate with your data. You are done and can skip the following steps. If not, proceed to the next step.
15. If you're not logged in to Power BI, or if an error occurs when updating the data, you need to log in to your organizational account again.

    * In Power BI, open the **Transform Data** menu, and then select **Data source settings**.
    * For each data source, select **Edit Permissions**, and then select **Organizational account**.

    >[!Important]
    >You must sign in to Power BI with the same account you use to access Workplace Analytics.

16. If prompted, select **Sign in**.
17. In the **Office 365** dialog box, select the organizational account that you use to log in to Workplace Analytics. The OData feed dialog box will then show that "you are currently signed in" to Power BI.
18. Select **Connect** to begin data preparation, which can take several minutes (up to two hours) to complete.

## Using the dashboard

After the Business Continuity Dashboard is set up and populated with Workplace Analytics data, the following guidelines help you set up and use the Power BI visualization charts to analyze your organization's collaboration patterns.

### Settings and scope

As a first step to viewing data in the dashboard, view and set the following parameters in the **Settings & Scope** tab.

* **Baseline time frame** - This is the baseline for your analysis and all changes will be compared with this time frame.

    >[!Note]
    >The **Baseline time frame** must precede and not overlap with the **Selected time frame**. If the two time frames overlap, you'll get a "Warning: Baseline and Current Timelines overlap" message.

* **Selected time frame** - This is the time frame you want to compare to the baseline time frame.
* **Scope** - Select the **Organizations** and **Time zones** you want to analyze in the report. These filters are applied across all the pages in the Power BI report.
* **Minimum group size** - This displays the minimum group size that has been configured for this report.
    >[!Important]
    >Make sure this adheres to your organization's policies around minimum aggregation requirements for displaying Workplace Analytics data.

After changing one or more of these settings, confirm the number of scoped employees are what you want to analyze.

> [!Note]
> As additional data is processed on a weekly basis, you'll need to adjust the **Selected Time Frame** if you want to view the most recent data.

### Power BI tips

A few tips to help you use the Business Continuity Dashboard in Power BI:  

* **Cross-filter and cross-highlight** - All visuals on a report page are interconnected. If you select a data point on one of the visuals, all the others on the page that contain that data will change, based on that selection.
* **Drillsown into a visual that has a hierarchy** - When a visual has a hierarchy, you can drill down to reveal additional details. Any chart in the dashboard labeled with "By Organization and Level Designation" supports the Power BI drill down capability.

For more details about using Power BI, see [Interact with visuals in reports, dashboards, and apps](https://docs.microsoft.com/power-bi/consumer/end-user-visualizations).

## Sharing the dashboard

Like other products that work with sensitive data, such as HR systems, Workplace Analytics is not meant for the general workforce. Rather, its users are expected to have training regarding how to handle sensitive information. Training should be specific to your organization. See [Data-protection considerations](../privacy/data-protection-considerations.md) when using data generated by Workplace Analytics.

You can share the Business Continuity Dashboard in a few different ways in Power BI. To learn more, see [Ways to share your work in Power BI](https://docs.microsoft.com/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

**Best ways to share**

* **Share insights in an app** - This option allows users to navigate the dashboard without access to the underlying data. See [Publish an app in Power BI](https://docs.microsoft.com/power-bi/service-create-distribute-apps) for details.
* **Share as a PDF or other static file** - This option is not interactive. See [Printing from the Power BI service](https://docs.microsoft.com/power-bi/consumer/end-user-print).

## Frequently asked questions

#### Q1 Who can create the dashboard in Power BI?

You must be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics to create the dashboard. You must also have a Power BI license and have the desktop version installed. See [Install and run Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-getting-started#install-and-run-power-bi-desktop) for details.

#### Q2 How frequently is data refreshed in the dashboard?

The dashboard gets repopulated once a week after Workplace Analytics finishes its weekend processing. **Note**: You must manually adjust the **Selected time frame** setting in the dashboard's **Settings & Scope** report to view the most recently processed data.

#### Q3 How do I share the dashboard with others in my organization?

You can share the dashboard with others in your organization *without sharing the underlying data* by publishing the insights in an app or as PDF or static file. See [Sharing the dashboard](#sharing-the-dashboard) for details.

#### Q4 Can I share the underlying dashboard dataset with others in my organization?

To maintain data privacy, only employees assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics should have access to the underlying dataset in the Power BI dashboard.

#### Q5 How do I set up and run a Workplace Analytics query?

See [Create a Person Query](./person-queries.md) for details.

#### Q6 How do I change the axis of a chart to use a different Organizational data attribute?

Only the required Organizational attributes are used when setting up the Power BI file. If you selected more organizational attributes when setting up your queries, you can use those additional attributes in your visuals. To use a different organizational attribute, search within the Fields pane for the Organizational attribute you want to use. Then, click on the visual you want to modify to select it. Finally, drag the Organizational attribute from the Fields pane to the Axis section in the Visualizations pane.

#### Q7 How do I integrate additional metrics or data sources with this dashboard?

See [Connect to data in Power BI](https://docs.microsoft.com/power-bi/connect-data/) to learn more about how to connect data in Power BI. See [Prepare organizational data](../setup/prepare-organizational-data.md) to learn about what organizational data you can analyze in Workplace Analytics and see [Data sources](../use/data-sourcesv2.md) to see what data sources you can connect to and analyze from within Workplace Analytics.

#### Q8 How do I use Power BI?

See [Power BI documentation](https://docs.microsoft.com/power-bi/) for details on how to use Power BI.

#### Q9 What languages is the dashboard available in?

The dashboard is currently only available in English.

## Support

* **Dashboard support** - Contact the Workplace Analytics team member that referred you to this page for support about onboarding, usage, and interpretation of the data contained within the dashboard.
* **Workplace Analytics support** - Refer to [Workplace Analytics documentation](../index.md) or [Workplace Analytics Support](../overview/getting-support.md) for additional help.
* **Support with other Microsoft products and tools** - Support for Power BI and other tools used in the context of this dashboard can be found through each product's associated support channels.

## Related topics

* [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)