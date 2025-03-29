# INSTRUCTIONS

This page will guide you through the steps to run an analysis that explains Copilot super usage. With this analysis, you will be able to examine how your organization is using Copilot, what changes are taking place, and how to drive adoption on the path to realizing ROI. 

**You will be able to unpack:**
1. **Habits:** determine how many daily/weekly/monthly Copilot actions lead to structural usage (e.g. norm = 11-16 actions per week tipping point after which usage accelerates quickly)
2. **Journey:** understand how some early adopters turn into super users, what they are using Copilot for, and if super usage is sustainable
3. **Confidence:** discover if super users are concentrating their actions in one app or multiple app
4. **Profiles:** learn what were the collaboration profiles of super users, what impact is it having on their work patterns
 
**We will take you through 2 steps:** 
1. Exporting data from Viva Insights.
2. Importing the data into a Power BI Template. 

### **To begin, please download the [DecodingSuperUsage GitHub Repo ZIP file](https://github.com/microsoft/DecodingSuperUsage/archive/refs/heads/DecodingSuperUsage.zip) and extract its contents to your local machine.**

## <h2>Part 1: Creating a custom query and exporting data from Viva Insights </h2>

### **Step 1: Creating the query**
1. Navigate to [Viva Insights](https://analysis.insights.viva.office.com/) -> Home -> Create custom query -> Person Query
2. Select Time period: Last 6 Months
3. Select metrics: Add metrics and select from the below groupings
<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/groupings.png" alt="groupings">

### **Step 2: Selecting analysis population and attributes to include**
1. Set "Is Active = True"
2. Select which employee attribute(s) you want to include
   -Note: The template works without any organizational/demographic data, but it is recommended to include a few such as organization, supervisor indicator, timezone, etc. 

### **Step 3: Download the csv.**
1. Once the query finishes running, download the csv. 



## <h2> Part 2: Load the .pbit </h2>

### **Step 1: Copy file path**
1. Browse to the csv file you saved in Part 1 using File Explorer
2. Right click on the file, select Copy As Path

### **Step 2: Load the template**
1. Open the .pbit file. You will be prompted with a query box for a file location.
2. Paste the location into the query box without quotations
    - Note: Copying as path will include quotations. 
3. Select Load.
<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/filepath.png" alt="File Path">

Please report any issues to jordanking@microsoft.com.

