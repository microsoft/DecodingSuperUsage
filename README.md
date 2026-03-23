# ℹ️ 🎉 **Power User Analysis is now in the Copilot Adoption PBI report in Viva Insights Analyst Workbench — prebuilt query included, simpler to light up.** 

&nbsp;






# Super Usage Analysis Template (Copilot + Viva Insights)

<div align="center">

![Current Version](https://img.shields.io/badge/version-4-blue)

**Insights into how super users of Microsoft Copilot emerge—and learn how to scale their success across your organization.**

### 📥 [Click Here to Download All Files](https://github.com/microsoft/DecodingSuperUsage/archive/refs/heads/main.zip)

**Related Templates & Tools:**

[![Super User Impact](https://img.shields.io/badge/Report-Super%20User%20Impact-003087)](https://aka.ms/superuserimpact)
[![AI-in-One Dashboard](https://img.shields.io/badge/Report-AI--in--One%20Dashboard-teal)](https://github.com/microsoft/AI-in-One-Dashboard)
[![GitHub Copilot Impact](https://img.shields.io/badge/Report-GitHub%20Copilot%20Impact-purple)](https://github.com/microsoft/GitHubCopilotImpact)
[![Chat Intelligence](https://img.shields.io/badge/Report-Chat%20Intelligence-orange)](https://github.com/microsoft/CopilotChatAnalytics)
[![PBI to Exec Deck](https://img.shields.io/badge/Tool-PBI%20to%20Exec%20Deck-red)](https://github.com/shailendrahegde/pbi-to-exec-deck)

**Additional Resources:**
[Viva Insights Python Library](https://microsoft.github.io/vivainsights-py/), [Viva Insights R Library](https://microsoft.github.io/vivainsights/)

⭐ **Star this repository** to receive notifications about new template versions
👀 **Watch** for updates and announcements

</div>

<details open>
  <summary>▶️ <b>Super User Adoption Dashboard Preview</b></summary>

  <br>

  <img src="https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/SuperUser.gif" alt="Super User Adoption Dashboard Preview" width="100%" />

</details>


---

<details open>
<summary><strong>✨ What's New</strong></summary>

<br>

- NEW 'Super User Impact' dashboard that explores the impact of Copilot on work patterns (& sentiment if available) and estimated value
- Static thresholds for usage tiers (clearer benchmarking)
- One click zoom into superusers
- Cross-team comparisons

</details>

---

<details open>
<summary><strong>📊 Why Study Super Usage & Insights You Can Explore</strong></summary>

<br>

Super usage patterns show how experimentation turns into durable habits. Identifying early signals and contextual attributes helps you:
- Replicate adoption paths
- Prioritize enablement
- Benchmark across teams
- Inspire the organization

**Super usage profile:**
What does super usage look like? What do super users use Copilot for? Are you seeing signs of workflow changes?

**Journey:**
How did some users turn into super users? What did super users do differently in the early days of license activation? How fast are you producing super users? Is super usage durable?

**Work patterns:**
What work patterns are associated with super users? Are you seeing any early impact?

**Change management:**
Where are the super users concentrated? Where might you focus enablement efforts?

</details>

---

<details open>
<summary><strong style="font-size:1.5em;">📋 Instructions</strong></summary>

<br>

![Viva Insights Query Setup Guide](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/viva_insights_setup.gif)

<details>
<summary><strong>Written Setup Guide</strong></summary>

<br>

### Step 1. Build the Person Query (Required for All Setups)

Open the [Viva Insights Analyst Workbench](https://analysis.insights.cloud.microsoft/) and follow this 5-step process to create your Person Query:

<details>
<summary><strong>Detailed step-by-step guide with screenshots</strong></summary>

<br>

![Detailed Query Setup Guide](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/viva_insights_query_setup_static.png)

### Quick Reference:

1. **Navigate to Analysis Results**
   - Go to [https://analysis.insights.cloud.microsoft/](https://analysis.insights.cloud.microsoft/)
   - Click on "Analysis results" in the left sidebar

2. **Create New Person Query**
   - Click "Create analysis"
   - Select "Person query" card
   - Click "Set up analysis"

3. **Configure Query Settings**
   - **Time period**: Last 6 months (rolling)
   - **Group by**: Week
   - **Filter**: Is Active = True
   - **Attributes**: Organization, FunctionType, TimeZone (minimum required)

4. **Select Required Metrics**
   - **Microsoft 365 Copilot**: Select "All metrics"
   - **Collaboration network**: Select "All metrics"
   - **Working hours collaboration**: Select "All metrics"
   - **Focus metrics**: Select "All metrics"
   - Missing even ONE metric will cause blank visuals in Power BI!

5. **Run and Wait for Completion**
   - Save & Run your query
   - Wait until **Status = Completed** (can take several hours for first run)
   - Do NOT export mid-processing
   - Once complete, copy your **Partition ID** and **Query ID** for Power BI

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

- Super Usage Interpretation Guide (PDF): [Interpretation Guide Super Usage Adoption](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Interpretation%20Guide%20Super%20Usage%20Adoption.pdf)
- Storyboard presentation template: [Storyboard PPTX - Super User Adoption](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Storyboard%20PPTX%20-%20Super%20User%20Adoption.pptx)  

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

</details>

</details>

---

<details>
<summary><strong>🤓 Nerd Corner</strong></summary>

<br>

If you're into automation and allergic to manual decks — try this:

👉 https://github.com/shailendrahegde/pbi-to-exec-deck

It turns raw outputs into **exec-ready PPTs** with insights pre-baked.
All you do: verify, tweak, ship.

</details>

---

<details>
<summary><strong>💬 Feedback</strong></summary>

<br>

We want to hear your feedback and suggestions. Please reach out to keithmcgrane@microsoft.com and jordanking@microsoft.com.

</details>

---

<details>
<summary><strong>🔔 Stay Updated</strong></summary>

<br>

- ⭐ **Star this repository** to receive notifications about new template versions
- 👀 **Watch** for updates and announcements
- 🔄 Check back regularly for new features and improvements

</details>

---
