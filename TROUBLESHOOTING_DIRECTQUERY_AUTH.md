# Troubleshooting: "Access to the resource is forbidden" (DirectQuery)

When connecting to Viva Insights via DirectQuery, you may encounter the following error after entering your PartitionID and QueryID:

> ⚠ **Table — Access to the resource is forbidden.**

No sign-in prompt appears, and the report fails to load.

---

## Cause

Power BI Desktop has stale cached credentials for the Viva Insights data source. Instead of prompting for a fresh sign-in, it silently reuses the invalid credentials and returns a forbidden error.

---

## Fix

**1. Clear the Viva Insights data source credentials**

In Power BI Desktop, go to:

`File` → `Options and settings` → `Data source settings`

Find the Viva Insights entry in the list, select it, and click **Clear Permissions**.

**2. Close Power BI Desktop completely**

Do not just close the file — exit the application fully.

**3. Reopen the file and reconnect**

Reopen the `.pbip` or `.pbit` file. Enter your PartitionID and QueryID when prompted. This time an authentication prompt will appear — sign in with the organizational account that has **Viva Insights Analyst** access to the partition.

---

## Parameter Format

Make sure your IDs are raw GUIDs with no extra text or URLs:

| Parameter | Correct format |
|---|---|
| PartitionID | `38651f6f-836b-4bdf-9615-4e255c290fea` |
| QueryID | `b41356d5-b23d-4296-b6d0-46ff50cc305e` |

---

## Additional Notes

<details>
<summary><strong>Microsoft Fabric free signup page appears during authentication</strong></summary>

If you see a page titled **"You've selected Microsoft Fabric free"**, your IT department has blocked free Fabric signups. Click **Sign In** (not the signup flow) — your organizational account will authenticate via SSO without needing a Fabric license.

</details>

<details>
<summary><strong>Browser-based authentication is blocked by IT policy</strong></summary>

If the web OAuth flow is blocked by your organization, try switching to the embedded browser in Power BI Desktop:

`File` → `Options and settings` → `Options` → `Global` → `Security`

Disable **"Use my default web browser"** to use the embedded WebView2 instead, which operates within the app's existing authenticated session.

</details>

<details>
<summary><strong>Authentication succeeds but the error persists</strong></summary>

If you authenticated successfully but still see the forbidden error, verify:

- The account signed in has the **Viva Insights Analyst role** assigned for the specific partition
- The **PartitionID** matches a partition that account has access to
- The **QueryID** corresponds to a query that is in **Completed** or **Exported** status in Viva Insights Advanced Analysis

</details>
