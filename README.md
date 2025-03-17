# INSTRUCTIONS

This page will guide you through the steps to run an analysis that explains Copilot super usage. With this analysis, you will be able to examine how you are using Copilot, drive adoption on the path to realizing ROI. 

**You will be able to unpack:**
1. **Habits:** determine how many daily/weekly/monthly Copilot actions lead to structural usage (e.g. norm = 11-16 actions per week tipping point after which usage accelerates quickly)
2. **Journey:** understand how some early adopters turn into super users, what they are using Copilot for, and if super usage is sustainable
3. **Confidence:** discover if super users are concentrating their actions in one app or multiple app
4. **Profiles:** learn what were the collaboration profiles of super users, what impact is it having on their work patterns
 
**We will take you through 3 steps:** 
1. Exporting data from Viva Insights.
2. Using a .xltm file to run several formulas to stage your data file (runtime ~10min).
3. Importing the data into a Power BI Template. 

### **To begin, please download the [DecodingSuperUsage GitHub Repo ZIP file](https://github.com/microsoft/DecodingSuperUsage/archive/refs/heads/DecodingSuperUsage.zip) and extract its contents to your local machine.**

## <h2>Part 1: Creating a Custom Query and Exporting Data from Viva Insights</h2>

### **Step 1: Creating the query**
1. Navigate to [Viva Insights](https://analysis.insights.viva.office.com/) -> Home -> Create customised query -> Person Query
2. Select Time period: Last 6 Months
3. Select metrics: Add metrics and select from the below groupings
<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/groupings.png" alt="groupings">

### **Step 2: Selecting Employees and Attributes to include**
1. Set "Is Active = True"
2. Select which employee attribute(s) you want to include
   -Note: The template works without any organizational/demographic data, but it is recommended to include a few such as organization, supervisor indicator, timezone, etc. 

### **Step 3: Download the csv.**
1. Do not modify the csv/xlsx. You will need to copy the raw data into the file included in Part 2.
2. When you do open the csv, and are asked to convert or don't convert, choose "Convert".


## <h2>Part 2: Using a .xltm File to Run the CalculateAll Macro</h2>

**NOTE: If you are running the macro and you are concerned the spreadsheet has frozen, look in the bottom right hand corner. If you see the image below, this means the macro is still processing. The macro slows down some when calculating the percentiles, but then it speeds back up.**

<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/calculating.png" alt="Calculating">

Please report any issues (where you are forced to debug the macro, or where the Office Script fails) to jordanking@microsoft.com.

**FOR BEST RESULTS, USE FRESHLY EXPORTED DATA OR ENSURE YOUR COPY/PASTE AREAS ARE CLEAN**

### **Step 1: If you haven't downloaded and extracted the .zip file, then download the .xltm File**
1. **[Click here to download the CalculateAll.xltm file](https://github.com/microsoft/DecodingSuperUsage/raw/DecodingSuperUsage/CalculateAll.xltm).**

### **Step 2: Open the Source File and Copy Data**
1. Open Excel.
2. Go to File > Open and navigate to the location of your source file containing the data.
3. Select the file and click Open (**Note**: If you are opening a .CSV file, and are prompted to Convert or Don't Convert...choose 'Convert'.)
5. Select all the data in the source file (you can use Ctrl + A to select all).
6. Copy the data (you can use Ctrl + C).

### **Step 3: Open the .xltm File**
1. Navigate to where you downloaded or extracted the .xltm file
2. Double-click on the Calculateall.xltm file to open it.

### **Step 4: Enable Macros and paste data into CalculateAll.xltm worksheet**
1. If you see the image below, [click here to troubleshoot](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Troubleshooting.md).
**If you don't see the warning below, proceed to step 2.**
<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/risk.png" alt="Security Risk">

2. If prompted, click Enable Content to allow macros to run.
<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/enablemacro.png" alt="Enable Macros">

3. Paste the copied data into the appropriate worksheet in the .xltm file (you can use Ctrl + V).


### **Step 5: Run the Macro**
1. Press Alt + F8 to open the Macro dialog box.
    - **Note: If your keyboard does not have function keys, you can access the Macro dialog box by going to the Developer tab (if enabled) and clicking on Macros. If the Developer tab is not visible, you can enable it by going to Excel Options> Customize Ribbon > Main Tabs > Checking Developer and clicking Apply.**

<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/macrobox.png" alt="Macro Dialog Box">

2. Select the macro you want to run (e.g., CalculateAll).
3. Click Run. Estimated run time: 10 minutes, but this may depend on local system resources.
4. **Save your file.**

## <h2> Part 3: Importing data into Power BI Desktop using the template</h2>

### **Step 1: Copy File Path**
1. Browse to the csv/xlsx file you saved in Part 2 using File Explorer
2. Right click on the file, select Copy As Path

### **Step 2: Download and Open the Power BI Template**
1. If you haven't downloaded the Power BI Template already through the ZIP file, [click here to download the Decoding Super Usage Template Power BI Template](https://github.com/microsoft/DecodingSuperUsage/raw/DecodingSuperUsage/Decoding%20Super%20Usage%20v9.pbit).
2. Browse to the download location and double click the .pbit file to open the file
    - You may also right click the file, and select Open.
4. Wait for Power BI Desktop to Load, where you will be prompted with a Query box for a file location.
5. Paste the location into the query box without quotations
    - Note: Copying as path will include quotations. 
5. Select Load.
<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/filepath.png" alt="File Path">

### **Step 3: Wait for Data to Load.**
1. Once loaded, you may begin expanding your visuals and dashboard.
