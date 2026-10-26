# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:
<img width="1358" height="922" alt="image" src="https://github.com/user-attachments/assets/3789b60f-b09a-4ee9-b4c8-2e679588a5ce" />

![ER Diagram](er_diagram_fitness.png)

### Entities and Attributes


| Member                  | MemberID (PK), Name, Phone, MembershipType                | Stores member personal and membership details |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------- |
| Program                 | ProgramID (PK), Type, Duration                            | Different fitness programs (Yoga, Zumba,etc.) |
| Trainers                | TrainerID (PK), Name, Phone, Specialization, Experience   | Trainers working in the gym                   |
| PersonalTrainingSession | SessionID (PK), MemberID (FK), TrainerID (FK), Date, Time | Personal training session booked by members   |
| Attendance              | ID (PK), MemberID (FK), ProgramID (FK), Date, Status      | Tracks which member attended which program    |
| Payment                 | ID (PK), MemberID (FK), Amount, Date, Mode                | Payment records of members                    |     |


### Relationships and Constraints


| **Relationship**                | **Cardinality** | **Participation**     | **Notes**                            |
| ------------------------------- | --------------- | --------------------- | ------------------------------------ |
| Member–Program                  | M\:N            | Partial on both sides | Attendance links Members to Programs |
| Program–Trainers                | M\:N            | Partial               | Trainers may run multiple programs   |
| Member–PersonalTrainingSession  | 1\:M            | Total on PTS side     | Each session must belong to a member |
| Trainer–PersonalTrainingSession | 1\:M            | Total on PTS side     | Each session requires one trainer    |
| Member–Attendance               | 1\:M            | Total on Attendance   | Attendance entry refer to a member   |
| Program–Attendance              | 1\:M            | Total                 | Attendance linked to programs        |
| Member–Payment                  | 1\:M            | Total on Payment      | Payment must be made by a member     |

### Assumptions
- A member can join multiple programs.
-Trainers can be assigned to multiple programs.
-Personal training sessions always involve one trainer and one member.

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_library.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_restaurant.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

---

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
