# Fintrack_Agent
FinTrack AI Agent
Overview
Problem: Managing personal finances is challenging due to the difficulty of tracking and analyzing spending over time. Without automation, identifying trends or overspending in categories like Food or Rent is time-consuming and error-prone.
Solution: The FinTrack AI Agent is a Python-based tool that automates the analysis of 5 years of spending data (Sep 2020 - Aug 2025) from an Excel file. It calculates totals, categorizes expenses, detects trends, generates visualizations, and provides budget tips to help users save money.
Features

Loads Data: Reads monthly spending data from spending_data_5_years.xlsx (categories: Food, Transport, Entertainment, Utilities, Rent, Other).
Analyzes Spending: Computes total spending, per-category totals, yearly trends, and year-over-year percentage changes.
Visualizes Results: Generates three charts:
Bar chart of total spending by category.
Line chart of yearly spending trends.
Stacked bar chart of categories per year.


Provides Tips: Offers actionable budget advice based on spending patterns (e.g., "Food is 25% of total. Track daily to cut unnecessary eats.").
Automation Ready: Can be scheduled to run periodically (e.g., weekly) using the schedule library.

Setup Instructions

Install Python:

Download and install Python 3.12+ from python.org. Ensure "Add to PATH" is checked.
Verify by running python --version in a terminal (should show 3.12 or higher).


Install Dependencies:

Open a terminal in the project folder (e.g., VS Code Terminal: View > Terminal).
Run:pip install pandas matplotlib openpyxl




Prepare Files:

Ensure spending_data_5_years.xlsx and fintrack_agent.py are in the same folder.
The Excel file contains monthly spending data (Sep 2020 - Aug 2025) with columns: Month, Food, Transport, Entertainment, Utilities, Rent, Other.


Run the Agent:

In VS Code, open fintrack_agent.py.
Right-click and select Run Python File in Terminal, or run:python fintrack_agent.py


Output appears in the terminal, and charts are saved to a charts/ folder.



Files in This Repository

fintrack_agent.py: The main Python script for the AI agent.
spending_data_5_years.xlsx: Sample spending data (Sep 2020 - Aug 2025).
charts/: Folder created after running, containing:
category_total.png: Bar chart of total spending by category.
yearly_total.png: Line chart of yearly spending.
category_yearly.png: Stacked bar chart of categories per year.



Sample Output
Running the agent produces:
Total Spent (Sep 2020 - Aug 2025): $2,406,520.00

By Category (All Time):
Rent            1200000
Food             602790
Transport        298299
Utilities        251246
Other            141851
Entertainment    112334
Name: sum, dtype: int64

By Year:
Year
2020    473243
2021    473645
2022    475130
2023    479042
2024    479201
2025    326259
Name: Total, dtype: int64

Year-over-Year Change (%):
Year
2020     0.000000
2021     0.084948
2022     0.314043
2023     0.820198
2024     0.033196
2025   -31.896297
Name: Total, dtype: float64

Monthly Totals (First 5 for example):
MonthPeriod
2020-09    44210
2020-10    43629
2020-11    43802
2020-12    47532
2021-01    39579
Freq: M, Name: Total, dtype: int64

Charts saved to charts/ folder.

Budget Tips:
- Rent is 49.9% of total spending—it's fixed, but consider if relocation could help long-term.
- Food is 25.0% of total. Track daily to cut unnecessary eats.
- Average monthly spending: $40,108.67. Set a budget below this to save.

Agent run complete! Check 'charts' folder for visuals.

Results Interpretation

Total Spending: $2.4M over 5 years, with Rent (50%) and Food (~25%) as the largest categories.
Trends: Spending is stable (~$473K-$479K per year), with a drop in 2025 (partial year).
Charts: Visualize category dominance and yearly patterns.
Tips: Suggest reviewing high Rent and Food spending for savings opportunities.

Deployment

The agent is deployed locally and shared via this GitHub repository.
To make it autonomous, add the schedule library (pip install schedule) and uncomment the scheduling code in fintrack_agent.py to run weekly.

Future Improvements

Add budget goal setting (e.g., limit Food to $8,000/month).
Integrate email alerts for weekly summaries (using smtplib).
Deploy as a web app using Streamlit for interactive uploads.

Requirements

Python 3.12+
Libraries: pandas, matplotlib, openpyxl
Excel file: spending_data_5_years.xlsx

