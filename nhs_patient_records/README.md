🏥 NHS Patient Records Database 


📌 Overview 

The NHS Patient Records Database is a simulated healthcare dataset designed to model how patient information, GP practices, and appointments are stored and analysed within an NHS-style system.

This project demonstrates practical skills in:
- SQL database design
- Data retrieval and filtering
- Joining relational tables
- Aggregation & basic analytics
- Visualisation using DBeaver

🌟 Key Features

- Relational database with Patients, GP Practices, and Appointments
- Queries demonstrating:
- Filtering (WHERE)
- Sorting (ORDER BY)
- Table joins (INNER JOIN)
- Aggregations (COUNT, GROUP BY)
- Visual screenshots of database structure and results


🛠️ 1️⃣ Database Design & Management 
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

🔍 2️⃣ Data Retrieval & Querying 
These examples demonstrate filtering and sorting in SQL.

🔹 Query 1 — Patients older than 40
Filters patients over age 40 and sorts by highest age.

SELECT * 
FROM Patients
WHERE Age > 40
ORDER BY Age DESC;



<img width="526" height="293" alt="select" src="https://github.com/user-attachments/assets/d79ab430-a67a-47fb-a679-396fc475a1c2" /> 


2: Female patients in postcode area 'LE5', sorted by IMD score ascending 

<img width="693" height="160" alt="SELECT2" src="https://github.com/user-attachments/assets/e03b12c6-97c8-40ac-a1ec-6ae649092aff" /> 


- Joins to combine data across multiple tables - Aggregations using GROUP BY and functions like COUNT ## Visuals: ## 3️⃣ Joins to Combine Tables 1: Show patients with their GP practice name - JOIN links patients to their GP - Shows demographic + GP name in one query <img width="577" height="479" alt="joins1" src="https://github.com/user-attachments/assets/ac515296-fde6-4252-bec7-b5b6a814f91e" /> 2: Show patients who attended appointments with date and GP <img width="665" height="575" alt="joins2" src="https://github.com/user-attachments/assets/eac4c64c-8123-4be7-8a93-791b21e5583f" /> ## 4️⃣ Aggregations with GROUP BY and COUNT 1: Count of patients per GP practice <img width="397" height="182" alt="aggr1" src="https://github.com/user-attachments/assets/19237716-2593-4a06-83c5-88795d849531" /> 2: Most common gender among patients who attended appointments <img width="341" height="125" alt="aggr2" src="https://github.com/user-attachments/assets/f1b1bf7f-0b63-4f2b-9c72-83ccd44cc429" />
