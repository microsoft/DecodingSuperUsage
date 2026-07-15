> [!IMPORTANT]
> **v13 is here** — this release adds compatibility with Viva Insights' newly consolidated Copilot Chat metrics (the old metrics are automatically rebuilt from the new merged ones, so every visual keeps working), and fixes a false "some Copilot Chat metrics are missing" warning plus a Power BI refresh error caused by a missing DisplayName column.
>
> **Download v13:** [CSV template](https://github.com/microsoft/DecodingSuperUsage/raw/DecodingSuperUsage/Template%20-%20Super%20User%20Adoption%20CSV%20-v13.pbit) &nbsp;&middot;&nbsp; [Direct Query template](https://github.com/microsoft/DecodingSuperUsage/raw/DecodingSuperUsage/Template%20-%20Super%20User%20Adoption%20Direct%20Query%20-v13.pbit)
>
> **Then update your Viva Insights query:** edit the query, open the **Microsoft 365 Copilot** metric selection, and re-check **Select all** so the newly consolidated Copilot Chat metrics are included in your export.

<div align="center">

<br>

# Super User Adoption

### Discover how Copilot super users emerge, surface use cases and scale their patterns across your organization.

<br>

[![Built by Microsoft](https://img.shields.io/badge/Built%20by-Microsoft-0078d4?style=for-the-badge&logo=microsoft&logoColor=white)](https://microsoft.github.io/Analytics-Hub/team/)
[![Analytics Hub](https://img.shields.io/badge/Analytics%20Hub-11%20Repositories-8661c5?style=for-the-badge&logo=github&logoColor=white)](https://microsoft.github.io/Analytics-Hub/)

**All Reports:** [https://microsoft.github.io/Analytics-Hub/](https://microsoft.github.io/Analytics-Hub/)

**Cowork Billing:** [https://microsoft.github.io/Analytics-Hub/cowork-billing/](https://microsoft.github.io/Analytics-Hub/cowork-billing/)

<br>

**Found this useful? ⭐ Star this repo to help others discover it!**

<br>

**[Dashboard Preview ↓](#dashboard-preview)** &nbsp;·&nbsp; **[Instructions ↓](#instructions)** &nbsp;·&nbsp; **[Related Resources ↓](#related-resources)** &nbsp;·&nbsp; **[Email your Admin ↓](#email-your-admin)**

<br>

</div>

---

<a id="dashboard-preview"></a>

<details open>
  <summary>▶️ <b>Super User Adoption Dashboard Preview</b></summary>

  <br>

  <img src="https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/SuperUser.gif" alt="Super User Adoption Dashboard Preview" width="100%" />

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

<a id="instructions"></a>

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

<details>
<summary><strong>Row Level Security (RLS) — Restrict Who Sees What</strong></summary>

Row Level Security (RLS) lets you control which rows of data each viewer can see — for example, showing a Finance lead only Finance data. Setup happens in two places: **Power BI Desktop** (define roles) and **Microsoft Fabric** (assign members).

### Step 1 — Define roles in Power BI Desktop

1. Open the report in **Power BI Desktop**.
2. Go to the **Modeling** tab → click **Manage roles**.
3. Click **+ New** and give the role a descriptive name (e.g. `Finance`, `EMEA`, `Manager View`).
4. Select the **Table** table on the left, then enter a DAX filter in the box on the right. The filter returns `TRUE` for rows this role is allowed to see.

   **Common filters:**

   | Goal | DAX filter |
   |------|-----------|
   | Filter by Organization | `'Table'[Organization] = "Finance"` |
   | Filter by FunctionType | `'Table'[FunctionType] = "Sales"` |
   | Show only the viewer's own data | `'Table'[PersonId] = USERPRINCIPALNAME()` |

   > The `USERPRINCIPALNAME()` approach works when PersonId values are work email addresses. Each person will only see their own rows.

5. Click **Save**. Repeat for each role you need.
6. **Test (recommended):** In the **Modeling** tab, click **View as**, select a role, and confirm the report filters correctly. Click **Stop viewing** when done.

### Step 2 — Publish the report

Publish as normal: **File → Publish → Publish to Power BI** and select your workspace. The roles you defined are included automatically.

### Step 3 — Assign members to roles in Microsoft Fabric

1. Go to [app.fabric.microsoft.com](https://app.fabric.microsoft.com) and open your workspace.
2. Find the **semantic model** (dataset icon — not the report itself).
3. Click the **three-dot menu (...)** next to it and select **Security**.
4. On the left, click a role name. On the right, search for a person's name, email address, or Azure AD security group, then click **Add**.
5. Repeat for all roles, then click **Save**.

> **Tip:** Use Azure AD security groups rather than individual emails. When someone joins or leaves a team, you update access in Azure AD instead of returning to Fabric.

**Important notes:**
- Workspace admins and report owners always see all data — RLS does not apply to them.
- A viewer with no role assigned sees no data at all. Make sure every intended viewer is in at least one role.
- A viewer assigned to multiple roles sees the union of access from all roles (OR logic, not AND).
- RLS applies to all reports built on the same semantic model.
- Works with both CSV and Direct Query setups.

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

<a id="related-resources"></a>

## 🔗 Related Templates & Tools

**Additional Resources:**
[Viva Insights Python Library](https://microsoft.github.io/vivainsights-py/), [Viva Insights R Library](https://microsoft.github.io/vivainsights/)

📥 **[Click Here to Download All Files](https://github.com/microsoft/DecodingSuperUsage/archive/refs/heads/main.zip)**

---

<a id="email-your-admin"></a>

## 📧 Email Your Admin

> 📧 **Before you begin, your Viva Insights admin needs to set up a Person Query.**
> This pre-written email covers all required metric groups, query settings, attributes, admin roles, and connection options — everything your admin needs in one click.

> **[📨 Email Prerequisites to Your IT Admin](mailto:?subject=Action%20Required%3A%20Viva%20Insights%20Query%20Setup%20Needed%20for%20Super%20User%20Adoption%20Report%20%28Power%20BI%29&body=To%3A%20IT%20Admin%20%2F%20Global%20Admin%20%2F%20Viva%20Insights%20Administrator%0ARe%3A%20Super%20User%20Adoption%20%28DecodingSuperUsage%29%20%E2%80%93%20Power%20BI%20Report%20Setup%0A%0A%0AWHAT%20THIS%20REPORT%20DOES%0A%0AThe%20Super%20User%20Adoption%20Report%20is%20a%20Power%20BI%20report%20powered%20by%20Viva%20Insights%20data.%20It%20identifies%20how%20Copilot%20super%20users%20emerge%20in%20your%20organization%20%E2%80%94%20tracking%20the%20journey%20from%20activation%20to%20habitual%20use%20%E2%80%94%20and%20helps%20you%20understand%20what%20work%20patterns%2C%20collaboration%20behaviors%2C%20and%20surfaces%20distinguish%20super%20users%20from%20the%20rest.%20Used%20to%20replicate%20adoption%20paths%20and%20focus%20enablement%20on%20the%20right%20cohorts.%0A%0A%0ADATA%20SOURCE%20REQUIRED%0A%0AViva%20Insights%20%E2%80%93%20Person%20Query%0AExport%3A%20analysis.insights.cloud.microsoft%20-%3E%20Create%20analysis%20-%3E%20Person%20query%0AFormat%3A%20CSV%20or%20Direct%20Query%20%28via%20Partition%20ID%20%2B%20Query%20ID%29%0A%0A%0AREQUIRED%20FIELDS%20%E2%80%94%20DO%20NOT%20REMOVE%0A%0AIMPORTANT%3A%20The%20Viva%20Insights%20Person%20Query%20must%20include%20ALL%20metrics%20listed%20below.%20Missing%20even%20one%20metric%20group%20will%20cause%20blank%20visuals%20in%20Power%20BI%20with%20no%20error.%20Do%20not%20export%20a%20partial%20query%20or%20remove%20columns%20from%20the%20CSV%20after%20export.%0A%0APerson%20Query%20%E2%80%94%20Required%20Metric%20Groups%20%28select%20%22All%20metrics%22%20for%20each%29%3A%0AMicrosoft%20365%20Copilot%20%28all%20metrics%29%2C%20Collaboration%20network%20%28all%20metrics%29%2C%20Working%20hours%20collaboration%20%28all%20metrics%29%2C%20Focus%20metrics%20%28all%20metrics%29.%0A%0ASpecific%20fields%20the%20report%20depends%20on%3A%0ACopilot_Active_Use_Days_per_week%2C%20Copilot_Total_Actions%2C%20Copilot_Total_Chats%2C%20Copilot_Total_Emails_with_Copilot%2C%20Copilot_Total_Documents_with_Copilot%2C%20Copilot_Total_Meeting_Summaries%2C%20Copilot_Total_Pages_with_Copilot%2C%20Copilot_Total_Teams_Chat_Copilot_Interactions%2C%20Copilot_Total_Word_Copilot_Interactions%2C%20Copilot_Total_Excel_Copilot_Interactions%2C%20Copilot_Total_PowerPoint_Copilot_Interactions%2C%20Copilot_Total_Outlook_Copilot_Interactions%2C%20Collaboration_hours%2C%20Meeting_hours%2C%20After_hours_collaboration_hours%2C%20Email_hours%2C%20Focus_hours%2C%20Uninterrupted_focus_hours%2C%20Internal_network_size%2C%20Strong_ties%2C%20Diverse_ties.%0A%0APerson%20Query%20%E2%80%94%20Required%20Attributes%20%28Dimensions%29%3A%0APersonId%2C%20Organization%2C%20FunctionType%2C%20TimeZone%2C%20IsActive.%0A%0AQuery%20Configuration%20%E2%80%94%20Required%20Settings%3A%0A-%20Time%20period%3A%20Last%206%20months%20%28rolling%29%0A-%20Group%20by%3A%20Week%20%28not%20Month%20%E2%80%94%20month%20grouping%20breaks%20trend%20calculations%29%0A-%20Filter%3A%20Is%20Active%20%3D%20True%0A%0A%0AINSIGHTS%20YOU%20WILL%20GAIN%0A%0A-%20Super%20user%20identification%20and%20tier%20classification%20%28light%20to%20super%20user%29%0A-%20Activation-to-habit%20journey%3A%20how%20fast%20users%20become%20super%20users%20and%20whether%20the%20behavior%20is%20durable%0A-%20Surface%20breakdown%3A%20which%20Copilot%20apps%20%28Word%2C%20Excel%2C%20Teams%2C%20Outlook%2C%20Chat%29%20super%20users%20engage%20with%20most%0A-%20Work%20pattern%20comparison%3A%20collaboration%20hours%2C%20meeting%20hours%2C%20focus%20time%2C%20and%20network%20size%20for%20super%20users%20vs.%20peers%0A-%20Team%20concentration%3A%20where%20super%20users%20are%20clustered%2C%20to%20focus%20enablement%20where%20momentum%20already%20exists%0A%0A%0AROLES%20%26%20PERMISSIONS%20REQUIRED%0A%0ACreate%20and%20run%20Person%20Query%20in%20Viva%20Insights%3A%20Insights%20Analyst%20%28assigned%20in%20Viva%20Insights%20Admin%29%0AAccess%20Viva%20Insights%20Analyst%20Workbench%3A%20Insights%20Analyst%20or%20Insights%20Administrator%0AExport%20query%20results%20as%20CSV%3A%20Insights%20Analyst%0A%0A%0ASOFTWARE%20REQUIREMENTS%0A%0A-%20Power%20BI%20Desktop%20%E2%80%94%20required%20to%20open%20the%20.pbit%20template%20file%0A-%20Access%20to%3A%20analysis.insights.cloud.microsoft%20%28Viva%20Insights%20Analyst%20Workbench%29%0A-%20Microsoft%20365%20Viva%20Insights%20license%20%E2%80%94%20required%20for%20the%20organization%20to%20generate%20Person%20Query%20data%0A%0A%0ATWO%20CONNECTION%20OPTIONS%0A%0ACSV%20Import%20%28.pbit%29%3A%20Run%20query%20-%3E%20export%20CSV%20-%3E%20point%20Power%20BI%20template%20to%20the%20CSV%20file%20path%0ADirect%20Query%20%28.pbit%29%3A%20Copy%20the%20Partition%20ID%20and%20Query%20ID%20from%20the%20completed%20query%20and%20enter%20them%20into%20the%20Power%20BI%20template%20%E2%80%94%20no%20CSV%20download%20needed%3B%20report%20refreshes%20automatically%20with%20each%20weekly%20Viva%20Insights%20update%0A%0AQuery%20must%20show%20Status%20%3D%20Completed%20before%20export%20or%20Direct%20Query%20connection.%20Do%20not%20export%20mid-processing.)**

---

**Found this useful? ⭐ Star this repo to help others discover it!**

That's it! 🚀
