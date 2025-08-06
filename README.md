## **Attention returning users:**

Now available: a **Viva Insights Connector–based template** with automated weekly refresh.

### 🔄 What's New in the Report:
- 📊 **Usage tiers now use Static Thresholds** for clearer benchmarking  
- 🎨 **Improved visuals** make it easier to read, interpret, and act on key insights  
- 📈 **Built-in cross-team comparisons** added to each slide for quick benchmarking  
- 🧭 **Overview and Executive Summary slides added and moved up front** for easier sharing of topline results  

---

### 📁 Looking for previous versions?
You can find archived report templates in the [**Archived Templates** folder](https://github.com/microsoft/DecodingSuperUsage/tree/DecodingSuperUsage/Archived%20Templates).



---

# Instructions

> ⚠️ **Disclaimer**  
> This is an experimental template. On occasion, you may notice small deviations from metrics in the Copilot Dashboard. We will continue to iterate based on your valuable feedback. An interpretation guide is included to assist with analysis. Currently, only English is supported.

---

### **Why should we study super users?**

Studying super users reveals how they've successfully navigated the adoption curve—from initial experimentation to habit formation—within the unique context and workflows of their organization. By understanding their specific journey and milestones, we can pinpoint critical moments that transform casual users into dedicated adopters, enabling us to replicate and scale this adoption across the company.

---

### **You will be able to unpack:**

1. **Super usage profile:**  
   What does super usage look like? What do super users use Copilot for? Are you seeing signs of workflow changes?

2. **Journey:**  
   How did some users turn into super users? What did super users do differently in the early days of license activation? How fast are you producing super users? Is super usage durable?

3. **Work patterns:**  
   What work patterns are associated with super users? Are you seeing any early impact?

4. **Change management:**  
   Where are the super users concentrated? Where might you focus enablement efforts?

---

### **We will take you through 3 steps:**

1. Exporting data from Viva Insights  
2. Importing the data into a Power BI Template  
3. Analyzing and building a story

---

### **To begin, please download the [DecodingSuperUsage GitHub Repo ZIP file](https://github.com/microsoft/DecodingSuperUsage/archive/refs/heads/main.zip)

### **Step 1: Creating the query**
1. Navigate to [Viva Insights](https://analysis.insights.viva.office.com/analyst/analysis) **Person Query**
2. Select **Time period: Last 6 Months**. Enable **Auto Refresh** to populate the template automatically, if needed.
3. Select metrics: Click **Add metrics** and choose from the groupings below:  
   <img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/groupings.png" alt="groupings">

### **Step 2: Selecting analysis population and attributes to include**
1. Set **Is Active = True**
2. Select which employee attribute(s) you want to include  
   > 💡 *Note: The template works without any organizational/demographic data, but it is recommended to include a few such as organization, supervisor indicator, timezone, etc.*
3. Run the query

---

## <h2> Part 2: Load the .pbit </h2>

Depending on your data access method, you can load the Power BI template in one of two ways: **CSV Upload** or **Direct Query**.

---

### 🔹 **Option 1: CSV Upload**

#### **Step 1: Copy file path**
1. Save the CSV and browse to the CSV file using File Explorer
2. Right-click on the file and select **Copy as Path**.

#### **Step 2: Load the template**
1. Open the `.pbit` file. You will be prompted with a query box for a file location.
2. Paste the file path into the query box **without quotations**.  
   > ⚠️ Note: Copying as path will include quotation marks—be sure to remove them.
3. Click **Load**.

<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/filepath.png" alt="File Path">

---

### 🔹 **Option 2: Direct Query Mode**

This method allows you to connect directly to Viva Insights without downloading a CSV.

#### **Step 1: Retrieve Query Details**
1. In Viva Insights, copy the link to your query. This link contains both the **Partition Id** and **Query Id**.

 <img src = "https://github.com/microsoft/DecodingSuperUsage/blob/8e3da74cf12cee29c7a62ffacb4f7c94a47eb122/images/Direct%20Query%20Link.png">

#### **Step 2: Launch the Direct Query Template**
1. Open the **Template Super User Analysis v (Direct Query)** `.pbit` file.
2. When prompted, enter the **Partition Id** and **Query Id** from the Viva Insights link.

> 💡 This method is ideal for users who want to avoid manual file handling and setup auto-refresh. Note that only those with Analyst access can use this method. 

---

### ✅ **Step 3: Analyze and Tell the Story**
1. Use the [interpretation guide](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Super%20User%202.0%20-%20Interpretation%20Guide.pdf) to analyze and further extend the analysis.
2. Use the [story board](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Superuser%20Analysis%202.0%20-%20Storyboard.pptx) to craft and tell your story!

We want to hear your feedback and suggestions. Please reach out to shahegde@microsoft.com or jordanking@microsoft.com.

