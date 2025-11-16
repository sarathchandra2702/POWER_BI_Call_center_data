📞 Call Centre Analytics Dashboard – Power BI

    A complete analytics solution built in Power BI to analyze call centre operations, agent performance, customer satisfaction, and operational efficiency.

📌 Project Overview
    This project visualizes and analyzes call centre performance using an interactive Power BI dashboard.
    It helps stakeholders understand:
    Customer satisfaction trends
    Agent efficiency and handling performance
    Call abandonment & resolution patterns
    Hourly workload distribution
    Overall call centre effectiveness
    The dashboard is designed with clean KPIs, slicers, and interactive visualizations for better decision-making.

🗂️ Dataset Description
The project is based on a call-centre dataset containing:
ColumnDescriptionCall IDUnique identifier for each callAgentName of the agent handling the callDate & TimeTimestamp of each callTopicIssue categorySpeed of Answer (sec)Time taken to answer the callCall Duration (sec)Handling timeCall ResolutionWhether the issue was resolvedSatisfaction RateCustomer feedback scoreAbandonedWhether caller dropped before resolution

📊 Dashboard Features
1. KPI Summary
These cards provide a snapshot of performance:
    5000 Total Call Volume
    68.07% CSAT (Customer Satisfaction Score)
    89.94% Call Resolved %
    18.92% Call Abandoned %
    67.52 sec Average Speed of Answer
    224.92 sec Average Call Handling Time

🔎 Key Insights & Findings
📞 1. Call Volume Insights
The call centre handled 5000 calls in the given time period.
Call volume peaks between 9 AM – 5 PM, with a noticeable drop by 6 PM.
High activity hours provide opportunities to optimize staffing.

😀 2. Customer Satisfaction Analysis
Overall CSAT = 68.07%, indicating a moderate satisfaction level.
The highest count of calls came from:
    Satisfied (1.2K)
    Normal (1.2K)
    Around 0.9K customers gave no satisfaction rating, which may indicate system or user drop-off.

🎧 3. Agent Performance
The agent table gives a detailed breakdown of:
    Total Calls Handled
    Call Abandonment %
    Speed of Answer
    Call Resolved %
    CSAT
    
Key Observations:
Top-performing agents demonstrated:
    Higher call resolution rates
    Lower abandonment levels
    Faster answer times


Example insights (from dashboard):
Stewart handled 582 calls with an 88.89% resolution rate.
Joe & Greg show strong performance with >90% resolution.
Agents with higher call volume tend to have slightly higher abandonment %.


⛔ 4. Call Abandonment Trends
The abandonment rate sits at 18.92%, higher than ideal (<10%).
High abandonment could be due to:
    Longer wait times during peak hours
    Insufficient staffing
    Inefficient call routing


⚡ 5. Operational Efficiency
Average Speed of Answer: 67.52 seconds
This is reasonable, but reducing it can increase CSAT.

Average Call Handling Time: 224.92 seconds
Indicates moderate complexity in customer issues.

Lower handling times correlate with higher satisfaction.


📅 6. Day-Wise Call Pattern
Weekday analysis shows:
Monday has the highest call volume.
Calls gradually decrease from Monday → Friday → Tuesday.
Insights suggest adjusting staffing on high-volume days.



📈 Visualizations Used

  KPI Cards
  Bar Charts
  Area Charts
  Slicers (Agent, Topic, Month, Weekday)
  Tables with conditional formatting
  DAX measures for key performance metrics

🧮 DAX Measures Used (Examples)
  CSAT % = AVERAGE(CallData[Satisfaction Rate])
  
  Call Resolved % = 
  DIVIDE(
      CALCULATE(COUNTROWS(CallData), CallData[Call Resolution] = "Yes"),
      COUNTROWS(CallData)
  )
  
  Call Abandoned % =
  DIVIDE(
      CALCULATE(COUNTROWS(CallData), CallData[Abandoned] = "Yes"),
      COUNTROWS(CallData)
  )
  
  Average Speed of Answer = AVERAGE(CallData[Speed of Answer])
  Average Handling Time = AVERAGE(CallData[Call Duration])


🛠️ Tools & Technologies
ToolPurposePower BI DesktopDashboard creationPower QueryData transformationDAXCalculations & KPIsCSV DatasetSource data

📁 Repository Structure
├── README.md
├── call_center_dashboard.pbix
├── Call-Center-Dataset.csv
└── images/
     └── dashboard_preview.png


🚀 How to Use
Download the repository.
Open call_center_dashboard.pbix using Power BI Desktop.
Load the dataset if required.
Use slicers to explore insights by:
    Agent
    Topic
    Date
    Weekday

📢 Conclusion
This Power BI dashboard provides a complete insight into call centre operations, giving management a clear view of:
    Agent productivity
    Customer satisfaction trends
    Performance bottlenecks
    Operational workload
It is a powerful tool for improving staffing efficiency, enhancing customer experience, and reducing operational bottlenecks.
