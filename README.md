# Fraud-Anomaly-Detection

## Overview

The **Fraud Anomaly Detection** project aims to build an automated system to detect and mitigate emerging fraud patterns within warranty programs. As fraud prevention efforts successfully reduce in-warranty fraud, bad actors are evolving their tactics and migrating to other warranties, requiring a proactive and dynamic response.

This project leverages advanced data science techniques such as time series forecasting and anomaly detection algorithms to safeguard the integrity of warranty services, ensuring fraudulent activities are identified before they escalate.

## Objective

The goal of this project is to **develop an automated anomaly detection system** that can:

- Detect emerging fraud patterns within warranty programs.
- Ensure the continued integrity of warranty services by proactively identifying and addressing potential fraudulent activities.
- Enhance security through a sophisticated, data-driven framework.

## Technical Approach

The approach to anomaly detection is multi-layered, with the following key steps:

### Level 1: Prophet Model
- **Goal**: Forecasting claim rates across various product categories, contract countries, and weeks.
- **Technique**: The **Prophet Model** is used for anomaly detection in time series data. This model helps us identify any claim rate patterns that deviate significantly from expected trends.

### Level 2: Isolation Forest Model
- **Goal**: Granular analysis of coverage programs and sales channels to detect fraud anomalies.
- **Technique**: The **Isolation Forest Model** is employed for anomaly detection, helping to identify patterns within subsets of the data such as specific coverage programs and sales channels.

### Level 3: Fraud Opportunity Rates
- **Goal**: Integrating fraud opportunity rates into the analysis to enhance anomaly detection.
- **Technique**: This level builds upon the insights from the previous models and incorporates **Fraud Opportunity Rates** to better understand where potential fraud is most likely to occur.

### Level 4: Fraud 360 Integration
- **Goal**: Enhance anomaly detection by integrating findings with a **Fraud 360** system for deeper insights and prioritization of anomalies.
- **Technique**: The final layer integrates findings with Fraud 360, allowing for the visualization and prioritization of anomalies through a custom-built dashboard. This ensures that high-risk fraud opportunities are flagged promptly for further investigation.

## Key Metrics

The following key metrics are tracked to monitor and understand the evolving fraud landscape:

- **Claim Rate**: The rate of claims processed across different product categories, regions, and time periods.
- **Fraud Opportunity Rate**: The rate at which fraudulent opportunities are detected, indicating the likelihood of fraud within different segments.
- **Risk Score**: A metric that quantifies the likelihood of fraud based on various input factors like country, product, and coverage program.

These metrics are monitored across different levels of the system (country, product, coverage program) to provide a comprehensive view of fraud activity and its evolution.

## Key Findings

The preliminary results have shown promising signs of progress:

- **Fraud Reduction**: The reduction of in-warranty fraud has continued, indicating the success of the existing fraud detection measures.
- **Emerging Fraud Patterns**: New fraud patterns have been successfully identified, enabling the team to address these issues before they escalate.
- **Powerful Automated Detection System**: The automated system is already proving effective in detecting emerging fraud, offering a valuable tool in the ongoing fight against fraudulent activities in warranty services.

## Installation and Usage

To use the anomaly detection system, you need to follow the steps outlined below:

### Prerequisites

1. **Python 3.x**: Ensure you have Python 3.x installed.
2. **Required Libraries**: Install the necessary libraries by running the following command:
    ```bash
    pip install -r requirements.txt
    ```
3. **Data**: Ensure you have access to the relevant fraud and claims data.


### Running SQL Queries

Some components of the project require running SQL queries to fetch fraud-related data. Use the provided SQL file `ac_anomalies_sql.sql` to fetch the necessary data for anomaly detection:

```bash
mysql -u username -p < ac_anomalies_sql.sql
```

### Visualizing the Results

- After running the Jupyter notebooks, visualize the anomalies and key metrics in the custom-built **Fraud 360 Dashboard**, which helps prioritize and track fraud cases.
  
Please ensure that all contributions are well-documented, tested, and adhere to the project's structure.

## License

This project is proprietary and code not available.
