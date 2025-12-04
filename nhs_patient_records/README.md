## 🏥 NHS Patient Records Database 


# 📌 Overview 

The NHS Patient Records Database is a simulated healthcare dataset designed to model how patient information, GP practices, and appointments are stored and analysed within an NHS-style system.

This project demonstrates practical skills in:
- SQL database design
- Data retrieval and filtering
- Joining relational tables
- Aggregation & basic analytics
- Visualisation using DBeaver

# 🌟 Key Features

- Relational database with Patients, GP Practices, and Appointments
- Queries demonstrating:
- Filtering (WHERE)
- Sorting (ORDER BY)
- Table joins (INNER JOIN)
- Aggregations (COUNT, GROUP BY)
- Visual screenshots of database structure and results


# 🛠️ 1️⃣ Database Design & Management 
✔️ What I Did
- 3 relational tables:
  - Patients
  - GP_Practices
  - Appointments
- Added Primary Keys and Foreign Keys
- Ensured 1-to-many relationship:
   - One GP Practice → many Patients
   - One Patient → many Appointments

📸 Visuals
ER Diagram (Full Database Structure) 

<img width="832" height="1148" alt="PatientRecordsDB" src="https://github.com/user-attachments/assets/93678e85-4b27-4f60-8010-e3dcd4a804e6" /> 

# Table Views in DBeaver 

<img width="668" height="391" alt="AppointmentsTable" src="https://github.com/user-attachments/assets/2f122822-1bd2-4cf1-9b8b-6986905ee499" /> <img width="724" height="421" alt="gpPractices" src="https://github.com/user-attachments/assets/c53494d1-e228-4459-a715-211de8a1beec" /> 

# 🔍 2️⃣ Data Retrieval & Querying 
These examples demonstrate filtering and sorting in SQL.

🔹 Query 1 — Patients older than 40
Filters patients over age 40 and sorts by highest age.

SELECT * 
FROM Patients
WHERE Age > 40
ORDER BY Age DESC;



<img width="526" height="293" alt="select" src="https://github.com/user-attachments/assets/d79ab430-a67a-47fb-a679-396fc475a1c2" /> 


🔹 Query 2 — Female patients in postcode LE5
Retrieves female patients located in LE5, sorted by IMD score.

SELECT *
FROM Patients
WHERE Gender = 'Female'
  AND Postcode LIKE 'LE5%'
ORDER BY IMD_Score ASC;


<img width="693" height="160" alt="SELECT2" src="https://github.com/user-attachments/assets/e03b12c6-97c8-40ac-a1ec-6ae649092aff" /> 



# 🔗 3️⃣ Joins to Combine Tables 
🔹 Join Example 1 — Patients + GP Practice Names

SELECT Patients.PatientID, Patients.Name, GP_Practices.Practice_Name
FROM Patients
JOIN GP_Practices ON Patients.GP_ID = GP_Practices.GP_ID;


<img width="577" height="479" alt="joins1" src="https://github.com/user-attachments/assets/ac515296-fde6-4252-bec7-b5b6a814f91e" /> 

🔹 Join Example 2 — Patients with Appointment Attendance 

SELECT Patients.Name, Appointments.Appointment_Date, GP_Practices.Practice_Name
FROM Appointments
JOIN Patients ON Appointments.PatientID = Patients.PatientID
JOIN GP_Practices ON Patients.GP_ID = GP_Practices.GP_ID
WHERE Appointments.Attended = 'Yes';


<img width="665" height="575" alt="joins2" src="https://github.com/user-attachments/assets/eac4c64c-8123-4be7-8a93-791b21e5583f" />



# 📊 4️⃣ Aggregations (GROUP BY + COUNT)
🔹 Aggregation 1 — Patient Count per GP Practice
SELECT GP_Practices.Practice_Name, COUNT(Patients.PatientID) AS Patient_Count
FROM GP_Practices
LEFT JOIN Patients ON GP_Practices.GP_ID = Patients.GP_ID
GROUP BY GP_Practices.Practice_Name;


<img width="397" height="182" alt="aggr1" src="https://github.com/user-attachments/assets/19237716-2593-4a06-83c5-88795d849531" />


🔹 Aggregation 2 — Most Common Gender of Attending Patients
SELECT Gender, COUNT(*) AS Count
FROM Patients
JOIN Appointments ON Patients.PatientID = Appointments.PatientID
WHERE Appointments.Attended = 'Yes'
GROUP BY Gender
ORDER BY Count DESC;


<img width="341" height="125" alt="aggr2" src="https://github.com/user-attachments/assets/f1b1bf7f-0b63-4f2b-9c72-83ccd44cc429" />


## ▶️ How to Run This Project
Requirements
- MySQL Server
- DBeaver / MySQL Workbench
- SQL file containing table creation & insert statements (optional if you want me to generate it)

Steps
1. Create a new MySQL database:

CREATE DATABASE NHS_Records;


2. Import or run the table creation script
3. Insert sample data
4. Run queries shown in this project
5. View results in DBeaver

## 📝 Summary


This project demonstrates the full lifecycle of SQL analytics:
- Designing relational tables
- Querying and filtering real-world style patient data
- Performing JOINs for multi-table analysis
- Using aggregation to produce insights
- Visualising results inside DBeaver

It represents how SQL is used in healthcare data roles such as:
  - Data Analyst
  - NHS Reporting Officer
  - Health Informatics Technician
