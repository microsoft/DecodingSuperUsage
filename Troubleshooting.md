## <h2>Unblocking Macros</h2>

### **Step 1: Unblock the Macros**
1. **Navigate to the location where you downloaded the .xltm file.**
2. **Right-click on the file and select Properties.**

<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/properties.png" alt="properties">

4. **In the Properties window, look for a section at the bottom about security with a warning that "This file came from another computer and might be blocked to help protect this computer."**
5. **Check the box labeled Unblock.**
6. **Click Apply and then OK to close the Properties window.**

<img src="https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/images/unblock.png" alt="unblock">

## <h2>Unblocking Macros</h2>

When Running the Macro, you may come across this error:

If you click Debug, Excel will Open Visual Basic and likely highlight a line of text that says ".DataBodyRange...etc.etc.etc"

While this doesn't make immediate sense, the highlight is actually referencing the formula above it. The formula in ths macro cannot find a value in the header row in excel.

To solve this, look at the formula above the highlighted section and compare it to row 1 (your header row) in your Viva Insights export. Do all of the values exist? Please keep in mind, the values are the formula are case sensitive. 

If a value does not exist, you will want to re-extract data from Viva Insights again, and then re-run the formula. 
