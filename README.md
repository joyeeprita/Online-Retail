# Online-Retail
Online Retail Sales Analysis

# Project Overview
This project analyzes an online retail transaction dataset using Python and Power BI. It covers data inspection, cleaning, exploratory data analysis, visualizations, KPI definitions, business insights, and recommendations.

# Project Objective
- Inspect and clean transaction-level retail data.
- Analyze sales revenue, orders, units, products, countries, and customer activity.
- Explore descriptive statistics, correlation, and outliers.
- Present key performance indicators and trends in a Power BI dashboard.
- Translate the analysis into practical business recommendations.
  
# Dataset

- source link : httpsarchive.ics.uci.edudataset352online+retail
- Source file: Online Retail.xlsx (provided dataset)

# The dataset contains these fields:

- InvoiceNo — invoice identifier; values beginning with C indicate cancellation records.
- StockCode — product/stock identifier.
- Description — product description.
- Quantity — number of units on a transaction line.
- InvoiceDate — invoice date and time.
- UnitPrice — price per unit in pounds sterling (£).
- CustomerID — customer identifier, sometimes missing.
- Country — country associated with the transaction.
The date range in the supplied file is 1 December 2010 to 9 December 2011.
Tools Used
- Python
- pandas and NumPy for data preparation and analysis
- Matplotlib for visualizations
- Jupyter Notebook for coding and analysis
- Power BI Desktop for KPI cards, charts, and interactive filtering
- Microsoft Word for the project report
  
# Data Cleaning Methodology
1. Load the Excel workbook and parse InvoiceDate as a date/time field.
2. Preserve InvoiceNo and StockCode as text identifiers.
3. Remove exact duplicate rows.
4. Exclude cancellation invoices where InvoiceNo begins with C.
5. Exclude records with missing dates, non-positive quantities, or non-positive unit prices from positive-sales analysis.
6. Calculate line revenue using Revenue = Quantity × UnitPrice.
7. Create a YearMonth field for monthly revenue analysis.
8. Keep rows with missing CustomerID for overall sales totals, but exclude them from unique-customer and repeat-customer counts.
Important: The analysis reports positive-sales line revenue, not net accounting revenue after returns and cancellations. December 2011 is incomplete in the supplied data.
Key Analysis and Visualizations
The project report includes:
1. Monthly revenue trend.
2. Top 10 product descriptions by revenue.
3. Top 10 countries by revenue.
4. Quantity versus revenue scatter plot.
5. Revenue distribution boxplot.
6. A supplementary correlation heatmap.

# KPI Definitions
- Total Revenue: Sum of revenue from included positive-sales lines.
- Total Orders: Count of distinct invoice numbers among included positive-sales lines.
- Unique Customers: Count of distinct non-missing customer IDs among included positive-sales lines.
- Total Units Sold: Sum of positive quantities among included sales lines.
- Average Order Value: Total Revenue divided by Total Orders.
  
Use the same cleaning rules in Python and Power BI to keep figures comparable.

# Main Findings
- Total positive-sales line revenue in the analyzed dataset is approximately £10.64 million.
- The cleaned dataset contains 524,878 transaction lines.
- November 2011 is the highest-revenue month in the observed period.
- The United Kingdom is the dominant market by revenue.
- DOTCOM POSTAGE appears among the highest-revenue descriptions and should be interpreted as a postage-related item rather than ordinary merchandise.
- Missing customer IDs limit customer-level analysis.
  
# Recommendations
- Improve the capture and validation of customer IDs.
- Review unusual transaction quantities and revenue values instead of automatically deleting statistical outliers.
- Use observed monthly trends as planning signals, validating seasonality with multiple years of data.
- Separate postage-related descriptions from merchandise when reporting best-selling products.
  
# Project Files
- reports/Online_Retail_Project_Report.docx — project report.
- reports/charts/ — chart images generated for the report.
- Online_Retail_Reports_Package.zip — packaged report and chart assets.
- README.md — project guide.
  
# How to Reproduce the Analysis
1. Place Online Retail.xlsx in your project data folder.
2. Install the required Python packages:pip install pandas numpy matplotlib openpyxl jupyter
3. Open Jupyter Notebook and run the notebook cells in order, starting with imports and data loading.
4. Apply the documented cleaning rules before calculating revenue and analysis measures.
5. Create the visualizations and save them under reports/charts/.
6. Open Power BI Desktop, import the cleaned data, create the KPI measures, and build the report visuals.
7. Capture a screenshot of the completed Power BI dashboard and insert it into Section 10 of the Word report before submission.
   
# Limitations
- Only the period available in the supplied dataset is analyzed.
- December 2011 contains data only through December 9.
- Cancellations and non-positive quantities/prices are excluded from positive-sales analysis.
- Missing customer IDs reduce the reliability and coverage of customer-level findings.
- IQR outlier flags do not prove that a record is erroneous.
- Correlation does not establish causation.
- Insert a genuine Power BI dashboard screenshot into the report before final submission.
