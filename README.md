# Super Usage Analysis Template (Copilot + Viva Insights)
![Current Version](https://img.shields.io/badge/version-31-blue)

Insights into how super users of Microsoft Copilot emerge—and learn how to scale their success across your organization.

[Download Latest (ZIP)](https://github.com/microsoft/DecodingSuperUsage/archive/refs/heads/main.zip)  
[Archived Templates](https://github.com/microsoft/DecodingSuperUsage/tree/DecodingSuperUsage/Archived%20Templates)  
[Super Usage Interpretation Guide](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Super%20User%202.0%20-%20Interpretation%20Guide.pdf)  
[Super Usage Storyboard PPT Template](https://github.com/microsoft/DecodingSuperUsage/blob/224b5d8fa5742b9c405036c76691a783e0199b55/Superuser%20Analysis%20-%20Storyboard%20v3.pptx)  


---

## What’s New
- Static thresholds for usage tiers (clearer benchmarking)
- One click zoom into superusers
- Cross-team comparisons 
- Direct Query template using Viva Insights connector (enables near-automatic weekly updates)
- NEW v30+: Scatterplots for additional cross-team analysis and deeper insights

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
Where are the super users concentrated? Where might you focus enablement efforts?

---

<h1 style="margin-top:1.5em; font-size:2.1em;">Instructions</h1>

> ⚠️ **Disclaimer**  
> This is an experimental template. On occasion, you may notice small deviations from metrics in the Copilot Dashboard. We will continue to iterate based on your feedback. Interpretation guide included. English only currently.

---

<details>
<summary><strong>Option 1: CSV Upload (Import Mode) – One‑off or Occasional Updates</strong></summary>

### At a Glance
| When to choose | Effort | Refresh cadence | Pros | Cons |
|----------------|--------|-----------------|------|------|
| You just need a snapshot or will manually refresh monthly/quarterly | ~10–20 min initial | Manual (re-export) | Simple, works behind stricter firewalls | Manual work, risk of stale data |

---

### 0. Pre‑Flight Checklist (DO NOT SKIP)
You have:
- Viva Insights Analyst (or equivalent) access.
- Copilot usage signals enabled in the tenant.
- Power BI Desktop (latest version).
- A place to save the exported CSV (local or network drive).
If any are missing, resolve first.

---

### 1. Build / Open the Person Query
1. Open the Viva Insights Analysis landing page: https://analysis.insights.viva.office.com/Analysis/CreateAnalysis  
   ![Viva Insights analysis landing page showing navigation to Create analysis](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/VivaLanding.png)
2. Under Create analysis, locate the Person query card and click Set up analysis.  
   ![Person query tile with Set up analysis button highlighted](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/PersonQuery.png)
3. Set Time period: Last available 6 months (rolling).  
4. Set Group by: Week.  
5. (Optional but recommended) Filter Is Active = True (if available).

---

### 2. Select ALL Required Metrics
If you miss even one required metric, some visuals will be blank.

![Required Viva Insights Metrics (Groupings)](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/groupings.png)

Organizational attributes:  
Best Practice is to include Organization and Function Type.  
Optionally include others (Region, Supervisor flag, Country) only if you will use them. Fewer attributes = faster queries.  
If your tenant uses different field names (e.g., Department vs Organization, JobFamily vs Function Type), select them here and plan to replace in the Power BI report so visuals bind correctly.

---

### 3. Run & Verify the Query
1. Save the query.  
2. Run it (if it doesn’t auto-run).  
3. Wait until Status = Completed.  
   - IMPORTANT: Initial processing can take several hours depending on tenant size and query complexity (do not assume it is stuck for at least 4 hours; large tenants may exceed this).  
   - Do NOT export while the status is Processing; you will get partial data and missing weeks.  
4. After completion, spot-check row count > 0.

---

### 4. Export the Data (CSV)
1. Open the completed query results.  
2. Click Export > CSV.  
3. Save using a clear name, e.g., `SuperUsagePersonQuery_YYYY-MM-DD.csv`.  
4. Confirm file size > 0 KB.

Tip (Windows): If the path has spaces, Power BI may still handle it fine—just remove quotation marks when pasting later.

---

### 5. Open the Template (.pbit)
1. Double-click the standard template file: `Template Super Usage Analysis (CSV).pbit` (actual filename may vary).  
2. When prompted for the file path:  
   - Windows: In File Explorer, Shift + Right-click the CSV > Copy as path > Paste > remove quotes.  
   - Mac: Right-click file > Option key > Copy "filename" as Pathname.  
3. Click Load.

---

### 6. Validate Successful Load (Critical)
Validation checklist (all should be true):
- No error dialogs.  
- Fields pane lists expected tables (e.g., Users, CopilotUsage, Attributes).  
- At least one visual on Executive Summary page renders with data (not all blanks).  
If anything fails:  
- Re-check metrics (Option 1 requires same set as Direct Query).  
- Confirm 6-month rolling window was selected.  
- Ensure you did not accidentally choose Monthly grouping.

---

### 7. Save Your Working Report
- File > Save As > `SuperUsageSnapshot_YYYY-MM-DD.pbix`.  
- This PBIX is now a static snapshot unless you rebuild with a new CSV.

---

### 8. (Later) Refreshing the Snapshot
To update in the future:
1. Re-run the Person Query (allow several hours if it needs to reprocess).  
2. Export a fresh CSV after Status = Completed.  
3. In the PBIX: Transform Data > Data Source Settings > Change Source (if path or filename changed).  
4. Apply changes. Validate again.

---

### 9. Common Mistakes & Fast Fixes
| Mistake | Symptom | Fix |
|---------|---------|-----|
| Forgot a required metric | Blank visuals | Re-export with full metric set |
| Skipped Function Type or Organization | Missing slicer / mislabeled visuals | Re-run query including both |
| Used Monthly grouping | Broken trend calculations | Rebuild query with Week |
| Exported mid-processing | Partial / missing weeks | Wait for Status = Completed (can take hours) |
| Did not filter active users (if needed) | Distorted adoption rates | Add Is Active = True |
| CSV open in Excel while loading | Load error / locked file | Close file and retry |

</details>

---

<details>
<summary><strong>Option 2 (Recommended): Direct Query – Live / Near-Automatic Weekly Updates</strong></summary>

### At a Glance
| When to choose | Effort | Refresh cadence | Pros | Cons |
|----------------|--------|-----------------|------|------|
| You want always-current weekly data with minimal manual work | ~10–25 min initial | Automatic (weekly source processing) | No CSV handling; rolling window auto-updates | Requires stable permissions & correct IDs |

---

### 0. Pre‑Flight Checklist
You have:
- Viva Insights Analyst access (and Copilot signals enabled).  
- Power BI Desktop (latest).  
- Authentication method: Organizational account (OAuth2).  
- Confirm you can open the Person Query portal (not blocked by network).

---

### 1. Open the Person Queries Page
Open: https://analysis.insights.viva.office.com/Analysis/CreateAnalysis  
![Viva Insights analysis landing page showing navigation to Create analysis](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/VivaLanding.png)

---

### 2. Create / Configure the Person Query
1. Click the Person query card (Set up analysis).  
   ![Person query tile with Set up analysis button highlighted](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/PersonQuery.png)
2. Set Time period: Last available 6 months (rolling).  
3. Group by: Week.  
4. Turn Auto refresh ON (otherwise new weeks never appear).  
   ![Auto refresh toggle enabled](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/Auto%20Refresh%20On.png)
5. Add Is Active = True filter (if available).  
6. Organizational attributes:  
   - Best Practice is to include Organization and Function Type.  
   - Optionally include others (Region, Supervisor flag, Country) only if you will use them. Fewer attributes = faster queries.  
   - If your tenant uses different field names (e.g., Department vs Organization, JobFamily vs Function Type), select them here and plan to replace in the Power BI report so visuals bind correctly.

---

### 3. Select ALL Required Metrics
Missing one required metric = blank or partial visuals. Confirm everything is selected per the reference:

![Required Viva Insights Metrics (Groupings)](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/groupings.png)

Save the query.

---

### 4. Allow the Query to Finish Processing
- Wait until Status = Completed before collecting IDs.  
- IMPORTANT: First (or modified) runs can take several hours depending on tenant size; this is normal.  
- Do NOT proceed to Power BI until completed—loading early causes blank visuals and rework.

---

### 5. Copy the Direct Query Link (Query Row & Link Icon)
From the Person Queries list, locate your query and click the link icon to copy its URL (this exposes the IDs you need).  
![Query row with arrows pointing to the query name and link icon](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/AnalysisResultsLink.png)

(Opening the query and using the Copy link button also works.)

---

### 6. Extract partitionId and queryId
From the copied URL identify and copy the two GUIDs (no extra spaces):  
![Partition and Query IDs highlighted in URL](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/CopyIdentifiers.png)  
- partitionId=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx  
- queryId=yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy  

Double-check each is 36 characters (including hyphens).

---

### 7. Open the Direct Query Template
1. Launch `Template Super Usage Analysis (Direct Query).pbit`.  
2. When prompted, paste the Partition Id and Query Id exactly (no trailing spaces).  
3. Sign in with your work account (OAuth2).  
4. Initial load may take 1–3+ minutes (model & first query).  
![Loading the Direct Query template in Power BI](https://raw.githubusercontent.com/microsoft/DecodingSuperUsage/refs/heads/DecodingSuperUsage/images/LoadPBIT.png)

---

### 8. Validate Data Load
Checklist:
- No credential/privacy errors.  
- Expected tables appear in Fields pane (including Organization and Function Type columns).  
- Executive Summary visuals populate (allow a few seconds).  
If blank:
- Reconfirm required metrics.  
- Ensure Organization & Function Type are present (case/spacing consistent).  
- Re-check GUIDs for typos or spaces.  
- Ensure query status really is Completed.

---

### 9. Publish for Stakeholders
1. File > Save As > `SuperUsage_DirectQuery.pbix`.  
2. Publish to a Power BI workspace.  
3. In Power BI Service: Dataset > Settings > Data source credentials > OAuth2 Sign in.  
4. No scheduled refresh required (Direct Query).  

---

### 10. Weekly Update Mechanics
| Element | When it updates | Your action |
|---------|-----------------|-------------|
| Viva Insights underlying data | Weekly processing | None |
| Person Query (Auto refresh ON) | After processing | None |
| Report visuals | On view/refresh | Open/Refresh |
| New week visible? | Within 24h of processing | Verify only |

If a new week doesn’t appear: confirm Auto refresh still On; reopen query once; refresh report.

---

### 11. Troubleshooting Matrix
| Symptom | Likely Cause | Action |
|---------|--------------|--------|
| All visuals blank | Missing required metric(s) | Add metrics, wait for completion |
| Slicers missing expected labels | Organization or Function Type absent/renamed | Include &/or rename columns to expected names |
| Some visuals blank | Grouping set to Month | Change to Week, reprocess |
| No new week appears | Auto refresh Off / processing not done | Turn On; wait; recheck tomorrow |
| Access denied | Expired credentials | Re-authenticate in Service |
| Random failures | GUID typo | Re-copy IDs carefully |

</details>

---

## Next Steps

1. Follow instructions in Option 1 or Option 2.
2. Publish / distribute: Save PBIX, publish to workspace (if Direct Query, confirm credentials).
3. Share supporting guides (see Interpretation & Storytelling section below) to align stakeholders.
4. Monitor weekly: After each Viva Insights processing cycle, confirm a new week appears and track emerging super users.

---

## Interpretation & Storytelling

Leverage the guides below to frame your narrative and drive action:

- Super Usage Interpretation Guide (PDF): [Super Usage Interpretation Guide](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Super%20User%202.0%20-%20Interpretation%20Guide.pdf)  
- Storyboard presentation template: [Super Usage Storyboard PPT Template](https://github.com/microsoft/DecodingSuperUsage/blob/224b5d8fa5742b9c405036c76691a783e0199b55/Superuser%20Analysis%20-%20Storyboard%20v3.pptx)  

Use the included guides to:
- Create an executive ready presentation
- Define what constitutes super usage internally
- Highlight early activation behaviors
- Recommend enablement actions per org or cohort

---

## Feedback
We want to hear your feedback and suggestions. Please reach out to shahegde@microsoft.com or jordanking@microsoft.com.
