# Backend Project: ELT Anomaly Detection

[Link to ELT Anomaly Detection Design Document](https://docs.google.com/document/d/13g6_KoIllvLP1QVaUJkUU7qoHKVrtWjMEuZ9IvUMzQs/edit?usp=sharing)

## Overview of the Project

The ELT Anomaly Detection project is designed to enhance the monitoring capabilities of our existing ELT framework within AWS CloudWatch. The primary focus is on validating data integrity and identifying anomalies in data row counts from various data providers by comparing current data against historical trends. This project moves beyond the binary success/failure approach and provides a more nuanced and insightful monitoring solution to ensure data quality.

### Purpose and Users

- **Users:** The primary users are data engineers and operations teams responsible for maintaining the integrity and quality of data in our ELT framework.
- **Job:** The system aims to monitor data row counts loaded into Snowflake Warehouse, detect anomalies based on historical patterns, and notify the team of any discrepancies.
- **Inspiration:** The need for this system arose from the limitations of the existing ELT process, which only tracked the success or failure of data loads without accounting for data quality. This project was inspired by the desire to create a more reliable and responsive monitoring solution.
- **Key Features:** The key features include anomaly detection in row counts, integration with AWS CloudWatch, and automated alarm creation for over 200 jobs, ensuring scalable and flexible monitoring.

### STAR Interview Questions

- **Situation:** The ELT framework initially lacked the capability to detect significant discrepancies in data volume, which could indicate issues even when a job was marked as ‘successful.’ I proposed and designed an anomaly detection system within AWS CloudWatch to address this gap.
- **Task:** The task involved designing a system that could monitor row counts post-ELT process, detect anomalies by comparing current data against historical trends, and notify the team through alarm notifications. This included creating metric filters, configuring CloudWatch alarms, and automating the alarm creation process.
- **Action:** I developed the detailed design for logging key metrics, integrating them with CloudWatch, and configuring alarms based on dynamic thresholds. I also created a script to automate the creation of CloudWatch alarms for each job metric, ensuring scalability. One of the main challenges was configuring the CloudWatch alarms to accurately detect anomalies without generating too many false positives, which required careful tuning of the thresholds and filters.
- **Result:** The final implementation provided a robust monitoring solution that detects anomalies in data loads, ensuring that data quality is maintained even when jobs are marked as successful. The automated alarm system allows the team to respond quickly to any issues, significantly improving data reliability. Through this project, I gained a deeper understanding of AWS CloudWatch’s capabilities and became more proficient in setting up automated monitoring solutions within our existing ELT framework.

<img width="650" alt="Anomaly Detection Alarm" src="https://github.com/user-attachments/assets/4a03ce07-909f-4f47-b993-146e3f73f9dc">

## Technologies

- **Cloud Platform:** AWS CloudWatch, AWS SNS, AWS Lambda, AWS ECS
- **Data Warehouse:** Snowflake
- **Programming Language:** Python
- **Libraries:** Boto3 (AWS SDK for Python)
- **CI/CD Tool:** Jenkins

## Architecture

<img width="650" alt="Anomaly Detection Flow Chart" src="https://github.com/user-attachments/assets/46c655ed-3d3a-4628-9aab-9f4255c749ce">


## Competencies

### JF 1.6: Can follow software designs and functional/technical specifications

- **Situation:** The ELT Anomaly Detection project required a comprehensive design to ensure all aspects of the system were covered, from data logging to anomaly detection.
- **Action:** I followed the design specifications laid out in the project documentation to implement the metric logging, CloudWatch integration, and alarm configuration. This ensured that each component of the system functioned as intended.
- **Result:** The system was implemented successfully according to the design, providing a reliable and scalable solution for anomaly detection in the ELT framework.

### JF 4.3: Is able to build, manage, and deploy code into the relevant environment

- **Situation:** Deploying the anomaly detection system involved ensuring that all components, from metric logging to alarm configuration, were correctly integrated and deployed within AWS.
- **Action:** I used Jenkins for the continuous integration and deployment of the ELT tasks, ensuring that the updated containers with the new logging functionalities were correctly deployed to AWS ECS. I also configured CloudWatch and SNS for monitoring and notifications.
- **Result:** The deployment process was streamlined, allowing for consistent and reliable monitoring of the ELT process. The automated alarm creation process further ensured that the system could scale with new jobs.

### JF 5.6: Understands how to follow testing frameworks and methodologies

- **Situation:** It was crucial to ensure that the anomaly detection system worked as intended before full deployment.
- **Action:** I implemented a testing strategy that included introducing controlled anomalies into the data to verify the responsiveness and accuracy of the anomaly detection models. This involved testing both the logging process and the alarm triggers.
- **Result:** The testing process validated the effectiveness of the anomaly detection system, ensuring that it correctly identified and alerted the team to discrepancies, thereby enhancing data quality assurance.
