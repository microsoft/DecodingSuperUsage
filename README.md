**Attention returning users**
We have updated the template to include a few new analyses, requiring additional metrics. Please note that you need to select all metrics now in the Collaboration Activity grouping.

# Instructions
Disclaimer - this is an experimental template and on occasions you may see small deviations from metrics in the Copilot Dashboard. We will constantly update and iterate based on your valuable feedback. Currently, only English is supported. 

**Why should we study super users?**
Studying super users reveals how they've successfully navigated the adoption curve—from initial experimentation to habit formation —within the unique context and workflows of their organization. By understanding their specific journey and milestones, we can pinpoint critical moments that transform casual users into dedicated adopters, enabling us to replicate and scale this adoption across the company.

**You will be able to unpack:**
1. **Super usage profile:** What does super usage look like ? What do super users use Copilot for? Are you seeing signs of workflow changes?
2. **Journey:** How did some users turn into super users? What did super users do differently in the early days of license activation?  How fast are you producing super users ? Is super usage durable?
3. **Work patterns:** What work patterns are associated with super users? Are you seeing any early impact? 
4. **Change management:** Where are the super users concentrated? Where might you focus enablement efforts?
 
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

We want to hear your feedback and suggestions. Please reach out to shahegde@microsoft.com or jordanking@microsoft.com.

