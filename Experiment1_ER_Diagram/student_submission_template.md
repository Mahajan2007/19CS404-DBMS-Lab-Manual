## ER DIAGRAM SUBMISSION 
## NAME - 
## REGISTER NUMBER - 

## SCENARIO CHOSEN:
Hospital ER Diagram

## ER DIAGRAM:
![WhatsApp Image 2025-03-06 at 16 59 45_fea08594](https://github.com/user-attachments/assets/2af6ff0b-07af-45e2-a8dd-4d098165f658)

## ENTITIES AND ATTRIBUTES:
~~~
Patient - Patient_ID (PK), Name, Gender, Date of Birth (DoB), Address, Phone No., Email, Insurance

Doctor - ID (PK), Name, Specialization, Phone No., Email, Work Schedule

Appointment - Appointment_ID (PK), Date, Time

Medical Records - ID (PK), Diagnosis

Billing - Billing_ID (PK), Patient_ID (FK), Amount, Billing Date, Payment Status

Department - Dept_ID (PK), Dept_Name, Dept_Head, Room No.
~~~
## RELATIONSHIPS AND CONSTRAINS:

## Book (Patient → Appointment)
Cardinality: Many-to-Many
Participation: Total (Every appointment must involve at least one patient)

## Assign (Appointment → Doctor)
Cardinality: Many-to-One
Participation: Total (Each appointment must be assigned to a doctor)

## Associate (Patient → Medical Records)
Cardinality: One-to-Many
Participation: Partial (A patient may or may not have medical records)

## Maintain (Doctor → Medical Records)
Cardinality: One-to-Many
Participation: Partial (Doctors maintain multiple records)

## Receive (Patient → Billing)
Cardinality: One-to-Many
Participation: Partial (Patients may have multiple billing records)

## Specialization (Doctor → Department)
Cardinality: Many-to-One
Participation: Partial (Doctor specializes in a department)

## EXTENSION (Prerequisite / Billing):

Billing was modeled by connecting Patient to Billing through the "Receive" relationship, where billing entries are generated for each patient based on services received. The Billing entity includes attributes like Billing_ID, Amount, Billing Date, and Payment Status to track financial transactions independently but linked via Patient_ID.

## DESIGN CHOICES:

Entities like Patient, Doctor, and Appointment are core in any healthcare system, so they were naturally included.
Medical Records are associated separately for flexibility — allowing multiple diagnoses per patient and doctor.
Billing is separated to maintain financial records cleanly, keeping healthcare service records independent from financial operations.
Departments were created for Doctors to properly map organizational hierarchy and specialization.
Many-to-Many relationships like Book and Assign are handled with associative entities (like Appointment) to simplify complex scheduling scenarios.

## RESULT:
Thus, the ER diagram for the hospital management system was successfully designed, and the entities, relationships, and constraints were clearly represented.
