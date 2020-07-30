---

title: Power BI Return to worksite template
description: Use the Return to worksite dashboard to visualize different seat-allocation options in Power BI based on Workplace Analytics data
author: madehmer
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Power BI Return to worksites

You can use the Return to worksites is a Power BI template that’s populated by Workplace Analytics data to help you determine how to allocate seats for your organization’s worksites.

As worksites begin opening at limited capacity to address safety concerns, employee seats become a limited resource. This dashboard helps you make the most of the limited seats by optimizing for on-site collaboration. The two allocation plans identify teams or a subset of teams who will benefit the most by returning to work because of their high collaboration patterns with others in the same location.

While this dashboard can help with planning, you must consider it in combination with other key factors, such as the nature of the work and individual employee circumstances and preferences.

The dashboard includes the following reports to help you allocate worksite seating: 

* **Which teams collaborate the most with others in the worksite?** – Shows how teams have collaborated on-site as compared with off-site collaboration, where you can evaluate relationships across the organization or use a filter to evaluate a specific location. This view is the basis for the two alternative plans for seating allocation in the dashboard. With either plan, team leaders must account for personal circumstances of individual team members and their ability to return to work when determining how to allocate available workspaces.
* **Plan 1:  Allocate seats to the teams with the most on-site collaboration** – This allocation plan identifies which teams should return to work based on the selected location and limited-seating capacity. This plan simplifies a leader’s decision by making it an all-or-nothing seat allocation for each team. However, if on-site leadership requires all teams have some worksite presence during a limited-seat capacity opening, then Plan 2 is a better option.
* **Plan 2:  Allocate seats across teams in proportion to on-site collaboration** – This option provides each team with some presence in a limited-capacity worksite. It allocates each team a proportionate number of seats based on the team’s on-site collaboration patterns and the limited-seat capacity for the selected location. If leadership prefer the all-or-nothing approach, then Plan 1 is a better option.

To populate the dashboard in Power BI, you must set up and successfully run the predefined Return to worksites query in Workplace Analytics. After the query successfully runs, you can download the Power BI template for the Return to worksites query on the Results page. This template is required to create the dashboard in Power BI. After the template is downloaded, you need to connect the query data from Workplace Analytics to the dashboard in Power BI.
After the dashboard populates with data, you can evaluate which of the two seat-allocation plans will work for your organization’s teams.

## Prerequisites

Before you can run the queries and populate the dashboard in Power BI, you must:

* Be assigned the role of Analyst in Workplace Analytics.
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.
* Have the following organizational attributes already uploaded and processed in Workplace Analytics.

  * **Worksite location** - Represents the most recent worksite location (or projected location) for each employee.
  * **Team or Organization** - Each employee’s team assignment that reflects the organizational level at which worksite included in a limited-seat capacity opening for your organization.

## Set up the dashboard

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Queries**.
2. Under **Start from preselected filters and metrics**, select **Return to worksites** to open the predefined query.
3. Select or confirm the following query settings:

   * **Name** - Customize or keep the default name
   * **Group by** - Week
   * **Time period** - Last 3 months
   * **Auto-refresh** - Keep this setting disabled
   * **Meeting exclusions** - Select the preferred rule for your tenant

   > [!Important]
   > The dashboard is designed to allocate worksite seats by team based on the current organizational structure. For best results, select **Last 3 months** for the **Time period** to reflect the most current organizational structure.

4. In **Select filters**, keep **Collaboration hours** selected.
5. In **Time investors** > **Do you want to limit the analysis to only certain time investors?**, keep **All employees** selected. Optionally, you can further filter the employees in scope for the dashboard. For example, excluding contractors or essential workers already allocated seats at the worksite. For more details about filter and metric options, see [Create a Person Query](./person-queries.md).
6. In **Their Collaborators**, do not exclude any collaborators.  
7. For the **How do you want to group the people who collaborated with the time investor?** question, select the organizational attribute that represents the employee’s worksite location, such as **Office** or **Building**.

   > [!Important]
   > The dashboard is designed to allocate worksite seats based on the amount of on-site collaboration time. If the worksite location is not selected, you might disable one or more Power BI charts.

8. For the **Do you want to focus the analysis on a particular set of collaborators and group all others as Unclassified?** question, keep the preselected filter as **IsInternal** equal to **True**.
9. In **Organizational data**, keep the preselected **Organization** and **LevelDesignation** attributes, and add the organizational attributes that reflect the worksite locations and applicable Teams (or Organizations) requiring seat allocation.
10. Select **Run** to run the query, which can take a few minutes to complete.
11. In **Queries** > **Results**, after both queries successfully run, select the **Download** icon for the **Collaboration tracker** query results, select **PBI template**, and then select **OK** to download the template.
12. Open the downloaded **Collaboration tracker Power BI template**.
13. If prompted to select a program, select **Power BI**.
14.	When prompted by Power BI:

    * In the Workplace Analytics **Queries** > **Results** page, select the **Link** icon for the Collaboration tracker query, and then select to copy the generated OData URL link.
    * In Power BI, paste the copied link into its respective field.
    * Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Workplace Analytics data.
    * Select **Load** to import the query results into Power BI. Loading these large files may take some time to complete.

11. If you're already signed in to Power BI with your Workplace Analytics organizational account, the dashboard visualizations will populate with your data. You are done and can skip the following steps. If not, proceed to the next step.
12. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in**. See [Troubleshooting](#troubleshooting) for more details.

    ![Power BI sign in](../Images/WpA/Tutorials/pbi-sign-in.png)

13. Select and enter credentials for the organizational account that you use to sign in to Workplace Analytics, and then select **Save**.

     >[!Important]
     >You must sign in to Power BI with the same account you use to access Workplace Analytics.

14. Select **Connect** to prepare and load the data, which can take a few minutes to complete.

## Dashboard settings

After the Collaboration assessment dashboard is set up and populated with Workplace Analytics data in Power BI, as a first step to viewing data in the dashboard, view and set the following parameters on the **Settings** page.