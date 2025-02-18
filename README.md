Project Title: Expense Data Standardization & Reimbursement Analytics in Power BI

🔹 Overview:
I recently worked on a Power BI project where I transformed and analyzed expense data to ensure data accuracy, consistency, and insightful reporting. The project involved data cleaning, transformation, and visualization to provide meaningful insights into reimbursements and expenses.

✅ Key Tasks & Solutions
📌 1. Data Cleaning & Transformation in Power Query
🔹 Corrected spelling and punctuation errors in the "Expense Type" column using Replace Values
🔹 Standardized project names by applying Trim & Lowercase functions
🔹 Handled missing currency values based on the amount:

Amount ≥ 1000 → INR
Amount < 1000 → USD
Else → EURO
🔹 Converted all expense amounts to INR using predefined exchange rates:

USD to INR = 83
EURO to INR = 87
💡 Tools Used: Power Query (M Language)

📌 2. Data Modeling & DAX Measures
🔹 Created a DAX measure to calculate the total reimbursed amount in INR:

DAX
Copy
Edit
Total_Reimbursed_INR = SUM('Table'[Amount in INR])
🔹 Used CALCULATE to filter the total reimbursement for a specific project (Project_B):

DAX
Copy
Edit
Reimbursed_Project_B = 
CALCULATE(SUM('Table'[Amount in INR]), 'Table'[Project Name] = "Project_B")
🔹 Created a DAX measure to count declined requests:

DAX
Copy
Edit
Count_Declined_Requests = 
COUNTROWS(FILTER('Table', 'Table'[Status] = "Declined"))
💡 Key Learning: Using DAX functions (SUM, CALCULATE, COUNTROWS, FILTER) to derive business insights efficiently.

📌 3. Interactive Dashboard & Visualizations
🔹 Slicer for dynamic filtering:

Project Name
Employee Name
🔹 Column Chart: Employees vs. Reimbursement Amount
🔹 Pie Chart: Project vs. Reimbursement Amount
💡 Outcome: Created an interactive and user-friendly dashboard that enables stakeholders to analyze reimbursements across projects and employees efficiently.

🎯 Key Takeaways & Learnings
✅ Data Cleaning & Transformation: Ensuring accuracy in reporting
✅ DAX Functions: Advanced calculations for insightful reporting
✅ Data Visualization: Effective storytelling with Power BI
✅ Interactive Reports: Slicers and dynamic visualizations for better decision-making

🚀 This project enhanced my expertise in Power BI, Power Query, and DAX, making data-driven decision-making more accessible and efficient!

