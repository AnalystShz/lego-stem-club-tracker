## NHS Patient Records Database
Project Overview
The NHS Patient Records Database simulates a small-scale NHS-style patient database. It allows tracking of:
- Patient demographics (age, gender, ethnicity, postcode, IMD score)
- GP practice information
- Appointment attendance and status
This project demonstrates skills in SQL, database design, data retrieval, aggregation, and basic analytics. It’s built in MySQL and visualized using DBeaver.

## Skills Demonstrated

This project showcases SQL and data analytics skills, along with screenshots demonstrating each skill.
## 1. Database Design & Management
Created relational tables with primary and foreign keys: Patients, GP_Practices, Appointments
Defined relationships between patients, GP practices, and appointments

# Visuals:
- ER diagram showing tables and relationships
<img width="832" height="1148" alt="PatientRecordsDB" src="https://github.com/user-attachments/assets/93678e85-4b27-4f60-8010-e3dcd4a804e6" />
- Table view of Appointments table diagram & GP_Practices table diagram in DBeaver
<img width="668" height="391" alt="AppointmentsTable" src="https://github.com/user-attachments/assets/2f122822-1bd2-4cf1-9b8b-6986905ee499" />
<img width="724" height="421" alt="gpPractices" src="https://github.com/user-attachments/assets/c53494d1-e228-4459-a715-211de8a1beec" />

## 2. Data Retrieval & Querying

- SELECT statements with filtering (WHERE) and sorting (ORDER BY)
- 1: Patients older than 40, sorted by age descending
<img width="526" height="293" alt="select" src="https://github.com/user-attachments/assets/d79ab430-a67a-47fb-a679-396fc475a1c2" />
WHERE Age > 40 → only patients older than 40
ORDER BY Age DESC → highest age first


- Joins to combine data across multiple tables
- Aggregations using GROUP BY and functions like COUNT

## Visuals:

- Query showing most common gender among patients who attended appointments
- Query showing most common age group

Query showing most common ethnicity
