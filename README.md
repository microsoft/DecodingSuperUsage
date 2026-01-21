# Super Usage Analysis Template (Copilot + Viva Insights)
![Current Version](https://img.shields.io/badge/version-31-blue)

Insights into how super users of Microsoft Copilot emerge—and learn how to scale their success across your organization.

[Download Latest (ZIP)](https://github.com/microsoft/DecodingSuperUsage/archive/refs/heads/main.zip)  
[Archived Templates](https://github.com/microsoft/DecodingSuperUsage/tree/DecodingSuperUsage/Archived%20Templates)  
[Super Usage Interpretation Guide](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Super%20User%202.0%20-%20Interpretation%20Guide.pdf)  
[Super Usage Storyboard PPT Template](https://github.com/microsoft/DecodingSuperUsage/blob/f6634a07ff4c9d754620e981082206032d47d9ca/Superuser%20Impact%20-%20Storyboard%20v4.pptx)  
[Viva Insights Python Library](https://microsoft.github.io/vivainsights-py/)  
[Viva Insights R Library](https://microsoft.github.io/vivainsights/)

<details>
  <summary><span style="font-size:1.15em;">🎬 <b>See the Report in Action (Video)</b></span></summary>
  <br>
  <a href="https://www.youtube.com/watch?v=40hsLAIiiD8" target="_blank">
    <img src="https://img.youtube.com/vi/40hsLAIiiD8/0.jpg" alt="Copilot Super Usage Report Video Thumbnail" width="100%" />
  </a>
</details>

<details open>
  <summary>▶️ <b>Super User Adoption Dashboard Preview</b></summary>

  <br>

  <img src="https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/SuperUser.gif" alt="Super User Adoption Dashboard Preview" width="100%" />

</details>

<details open>
  <summary>▶️ <b>Super User Impact Dashboard Preview</b></summary>

  <br>

  <img src="https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/Super%20User%20Impact%20Gif.gif" alt="Super User Impact Dashboard Preview" width="100%" />

</details>

---

## What's New
- NEW 'Super User Impact' dashboard that explores the impact of Copilot on work patterns (& sentiment if available) and estimated value
- Static thresholds for usage tiers (clearer benchmarking)
- One click zoom into superusers
- Cross-team comparisons 

---

## Why Study Super Usage
Super usage patterns show how experimentation turns into durable habits. Identifying early signals and contextual attributes helps you:
- Replicate adoption paths
- Prioritize enablement
- Benchmark across teams
- Inspire the organization

---

## Insights you can Explore

**Super usage profile:**  
What does super usage look like? What do super users use Copilot for? Are you seeing signs of workflow changes?

**Journey:**  
How did some users turn into super users? What did super users do differently in the early days of license activation? How fast are you producing super users? Is super usage durable?

**Work patterns:**  
What work patterns are associated with super users? Are you seeing any early impact?

**Change management:**  
Where are the super users concentrated? Where migh t you focus enablement efforts?

---

## Templates

This repository includes four Power BI templates in two categories:

**Super User Adoption Templates**
- **Template - Super User Adoption (CSV Input).pbit**: Analyzes Copilot adoption patterns and super user emergence using CSV exports. Best for one-time analysis or sharing with external stakeholders.
- **Template - Super User Adoption - (Viva Insights).pbit**: Same analytics with direct Viva Insights connection. Enables automatic refresh for ongoing monitoring.

**Super User Impact Templates**  
- **Template - Super User Impact - (CSV Input).pbit**: Measures Copilot's impact on work patterns and productivity using CSV data. Includes estimated value and sentiment analysis.
- **Template - Super User Impact - (Viva Insights Input).pbit**: Same analytics with direct Viva Insights connection for continuous impact tracking.

**Choosing Your Setup:**  
Use **CSV templates** for ad-hoc analysis, simpler setup, or easier sharing. Use **Viva Insights templates** for automatic refresh, real-time data, and ongoing executive dashboards.

---

## Related Tools

**For Python Users:** If you prefer programmatic analysis or need custom workflows beyond these Power BI templates, check out the [Viva Insights Python Library](https://microsoft.github.io/vivainsights-py/) for direct API access, advanced data manipulation, and integration with your Python data science stack.

**For R Users:** Explore the [Viva Insights R Library](https://microsoft.github.io/vivainsights/) for statistical analysis, custom visualizations, and seamless integration with R-based data science workflows.

**Sample Code & Examples:** Browse the [Viva Insights Sample Code Repository](https://github.com/microsoft/viva-insights-sample-code) for ready-to-use code examples, API integration patterns, and reference implementations across multiple programming languages.

These tools enable you to build custom super usage analyses, automate reporting pipelines, and extend the insights beyond what's available in the Power BI templates.

---

<h1 style="margin-top:1.5em; font-size:2.1em;">Instructions</h1>

> ⚠️ **Disclaimer**  
> This is an experimental template. On occasion, you may notice small deviations from metrics in the Copilot Dashboard. We will continue to iterate based on your feedback. Currently available in English only.

---

## Step 1. Build the Person Query (Required for All Setups)

1. Open: [https://analysis.insights.cloud.microsoft/](https://analysis.insights.cloud.microsoft/) and go to Create Analysis.
   
   ![Landing page showing Create Analysis](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/VivaLanding1.png)
3. Select **Person Query** → *Set up analysis*.
   
   ![Person query card highlighted](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/PersonQuery.png)
   
5. Configure:
   - **Time period**: Last 6 months (rolling)
   - **Group by**: Week
   - **Metrics**: See sub-step 4 for required attribute selection.
   - **Filter**: Is Active = True (if available) - You can validate the number of employees here. 
   - **Attributes**: Include Organization and Function Type (others optional) - this is the last box on this page. 
6. Select **ALL required metrics** (missing one will cause blank visuals).  
   ![Required metrics screenshot](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/groupings.png)
7. Save & Run query. Wait until **Status = Completed** (first runs can take several hours). Do not export mid-processing.

---

## Step 2. Choose Your Power BI Setup Path

<details>
<summary><strong>Import a CSV File</strong></summary>

- Export results as CSV → Save clearly (e.g., `SuperUsagePersonQuery_YYYY-MM-DD.csv`).
- Open `Template Super Usage Analysis (CSV).pbit` → point to CSV file path.
- Save working PBIX and publish to Power BI service for sharing (manual refresh required for updates).

</details>

<details>
<summary><strong>Setup Direct Query to Viva Insights</strong></summary>

- From Person Queries page, copy link (row/link icon).  
  ![Query row showing link icon](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/AnalysisResultsLink.png)
- Extract **partitionId** and **queryId** from URL. Confirm 36 characters each.  
  ![Partition and Query IDs highlighted](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/CopyIdentifiers.png)
- Open `Template Super Usage Analysis (Direct Query).pbit` → paste IDs when prompted.
- Sign in with your work account. Initial load may take 1–3 minutes.
- Save PBIX and publish to Power BI workspace. No scheduled refresh required (Direct Query auto-refreshes weekly).

</details>

---

## Next Steps

<details>
<summary><strong>Validation & Troubleshooting</strong></summary>

**Checklist for success:**
- No errors on load  
- Fields pane includes expected tables  
- Executive Summary visuals populate (not all blank)  

**Common Mistakes & Fixes**  
| Symptom | Cause | Fix |
|---------|-------|-----|
| Blank visuals | Missing required metric(s) | Re-export/re-run query with full set |
| Missing slicers/labels | Skipped Org/Function Type | Add both attributes and reprocess |
| Trend calcs broken | Grouped by Month | Use Week grouping |
| Partial weeks | Exported mid-processing | Wait until Status = Completed |
| Distorted adoption rates | Didn't filter active users | Add Is Active = True |
| Load error | CSV open in Excel (Option 1) | Close file and retry |
| Direct Query blank | Wrong GUIDs or status not complete | Re-check IDs and query status |

</details>

<details>
<summary><strong>Publish / Distribute</strong></summary>

- Save your PBIX file after setup.  
- If using Direct Query, publish to a Power BI workspace and configure credentials (OAuth2).  
- If using CSV Import, publish the PBIX file but note that refreshes are manual.  

</details>

<details>
<summary><strong>Interpretation & Storytelling</strong></summary>

Leverage the guides below to frame your narrative and drive action:

- Super Usage Interpretation Guide (PDF): [Super Usage Interpretation Guide](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Super%20User%202.0%20-%20Interpretation%20Guide.pdf)
- Storyboard presentation template: [Super Usage Storyboard PPT Template](https://github.com/microsoft/DecodingSuperUsage/blob/224b5d8fa5742b9c405036c76691a783e0199b55/Superuser%20Analysis%20-%20Storyboard%20v3.pptx)  

Use the included guides to:
- Create an executive-ready presentation  
- Define what constitutes super usage internally  
- Highlight early activation behaviors  
- Recommend enablement actions per org or cohort  

</details>

<details>
<summary><strong>Monitor with Automatic Refresh</strong></summary>

- Configure Published Report Refresh settings
- Navigate to [Power BI Web](https://msit.powerbi.com/home?experience=power-bi) (you may need to login)
- Find the Report and Semantic Model you just published.
- Hover over the Semantic Model and click on the icon as seen below:
![Refresh1](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/Refresh1.png)
- On this page, from the list of options available, click on Refresh and then configure your report as seen below in the screenshot, or as you best fits your needs.
  
![refresh](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/refresh.png)

  
- For Direct Query: Reports update automatically with each weekly Viva Insights refresh, but you will still need to update the published report refresh settings as seen above. 
- For CSV Import: Re-run your query, export a new CSV, and repoint the PBIX to the updated file.  
- Verify weekly that a new week of data appears.  
- Track emerging super users and adoption trends regularly.  

</details>

---

## Feedback
We want to hear your feedback and suggestions. Please reach out to keithmcgrane@microsoft.com.

---

<table align="center" width="100%" style="margin-top:2.2em; margin-bottom:1.7em;">
  <tr>
    <!-- Copilot Impact Banner (Left)-->
    <td style="vertical-align:top; text-align:center; width:50%;">
      <div style="
        display:block;
        margin:0 auto;
        width:340px;
        max-width:95vw;
        background: linear-gradient(94deg, #f9f6ff 0%, #e6f0fd 100%);
        border: 2px solid #b38cff;
        border-radius: 15px;
        box-shadow: 0 2px 16px #9a7fff20;
        padding: 1.1em 1.1em 1.05em 1.1em;
        ">
        <span style="color:#2a237a; font-size:1.13em; font-weight:600;">
          ✨ This report <b>wouldn't have been possible without the magic of GitHub Copilot.</b><br/>
          <span style="font-weight:500;">
            As a tribute, we have built this GitHub Copilot analytics report.<br/>
            <a href="https://github.com/microsoft/GitHubCopilotImpact" style="color:#29009f; font-weight:600; text-decoration:underline;" target="_blank">@microsoft/GitHubCopilotImpact</a> &mdash; try it out and give us feedback!
          </span>
        </span>
      </div>
    </td>
    <!-- AI-in-One Banner (Right)-->
    <td style="vertical-align:top; text-align:center; width:50%;">
      <div style="
        display:block;
        margin:0 auto;
        width:340px;
        max-width:95vw;
        background: linear-gradient(93deg, #eefcf5 0%, #e1edff 100%);
        border: 2px solid #17bcb8;
        border-radius: 15px;
        box-shadow: 0 2px 16px #24d6cd14;
        padding: 1.1em 1.1em 1.05em 1.1em;
        ">
        <span style="color:#086b65; font-size:1.13em; font-weight:600;">
          🤔 Curious how <b>free chat, M365 Copilot, and agent usage all connect?</b><br>
          <span style="font-weight:500;">
            Check out the companion report at<br>
            <a href="https://github.com/microsoft/AI-in-One-Dashboard" style="color:#005782; font-weight:600; text-decoration:underline;" target="_blank">@microsoft/AI-in-One-Dashboard</a>
          </span>
        </span>
      </div>
    </td>
  </tr>
</table>
