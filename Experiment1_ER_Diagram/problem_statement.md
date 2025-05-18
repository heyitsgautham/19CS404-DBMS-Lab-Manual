# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.



---

### 🔹 Scenario  Hospital Database
Design a database for patient management, appointments, medical records, and billing.

*User Requirements:*
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission 
# Name: HIRUTHIK SUDHAKAR
# Reg.no:212223240054
# Scenario Chosen:
HOSPITAL
## ER Diagram:
![image](https://github.com/user-attachments/assets/9498e45f-92bd-4812-a0ad-94d56445ce8c)


## Entities and Attributes:


1. Patient
   - patientID (PK)
   - FullName
   - DOB
   - Gender
   - Address
   - Phone number
   - Email
   - Insurance details

2. Doctor
   - DoctorID (PK)
   - FullName
   - Specialization
   - Phone
   - Email
   - Workschedule

3. Appointment
   - AppointmentID (PK)
   - AppointmentDate
   - Appointment Time
   - Reason
   - Notes
   - DoctorID (FK)
   - PatientID (FK)

4. Medical Record
   - RecordID (PK)
   - Diagnosis
   - Medications
   - Treatments
   - TestResults
   - Notes
   - DoctorID (FK)
   - PatientID (FK)

5. Department
   - DeptID (PK)
   - DeptName
   - DeptHead

6. Billing
   - BillID (PK)
   - TotalAmount
   - BillDate
   - appointmentID (FK)

7. Payment
   - paymentID (PK)
   - PaymentDate
   - amountPaid
   - paymentMethod
   - paymentStatus
   - BILLID (FK)


Relationships:

- Patient — books —> Appointment
- Patient — has record —> Medical Record
- Doctor — records for —> Medical Record
- Doctor — works in —> Department
- Doctor — consults —> Appointment
- Appointment — generates —> Billing
- Payment — pays for —> Billing

## Design Choices

- **Entity-Relationship Model**: We used an ER model to clearly represent entities like Patient, Doctor, Appointment, Medical Record, Billing, Payment, and Department, and to show how they interact.
- **Normalization**: Attributes are grouped logically into entities to minimize redundancy and maintain data integrity.
- **Primary & Foreign Keys**: Primary keys (PK) uniquely identify each entity, and foreign keys (FK) are used to establish relationships between them.
- **Scalability Consideration**: The model supports adding more departments, multiple appointments per patient, and billing history with linked payments.
- **Real-world Mapping**: Real-world healthcare workflow is reflected — from booking an appointment to payment after service.
- **Modularity**: Each entity encapsulates a specific responsibility to keep the system modular and maintainable.

## Pre-requisites

To use or extend this design into a functional application or database, the following are recommended:

- **Basic Knowledge Requirements**
  - Understanding of ER diagrams and database normalization
  - Familiarity with SQL or ORM (Object-Relational Mapping) tools

- **Software Requirements**
  - ERD Design Tool (e.g., dbdiagram.io, Lucidchart, Draw.io)
  - Database Management System (e.g., MySQL, PostgreSQL, SQLite)
  - Optional: Backend framework (e.g., Flask, Spring Boot) to implement logic

- **Development Environment**
  - Code editor (e.g., VS Code)
  - Git for version control (if working in a team)
  - Python/Java/Node.js runtime (if implementing the system)

- **Suggested Next Steps**
  - Convert ER model into relational schema
  - Generate SQL scripts for table creation
  - Build frontend/backend logic to interact with database


## RESULT
Thus, the Entity-Relationship (ER) Diagram have been created successfully.
