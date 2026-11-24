
# WORKSHEET 2
## Identify Objects, Classes, and Relationships

**Instructions:** Use the process and proposed system from Worksheet 1 to complete this worksheet.

---

## Part 1. Identify the Objects

Identify the important people, things, records, transactions, or concepts that your proposed system needs to represent.

**Guide Question:**

If you were going to create a program for this process, what things would the program need to represent?

| No.| Object | Description |
| 1  |Adviser/Teacher | Assign roles, assign group, rate (overall)|
| 2  |Student|A student can be a student cleaner (update status, encode if absent/present) student leader (rate members, feedback)| 
| 3 |Cleanliness Sheet |Helps adviser make groups and give feedback|
| 4 |Tracker System|helps student leader rate/give feedback|
| 5 | | |
| 6 | | |
| 7 | | |
| 8 | | |
| 9 | | |
| 10 | | |

### Object Evaluation

For each identified object, ask:

- Does it play an important role in the process?
- Does it contain information?
- Does it perform an action?
- Does it interact with another object?
- Does the proposed system need to keep track of it?

**Reminder:** Remove objects that are not necessary for your proposed system.

---

## Part 2. Analyze Object Interactions

Determine how your identified objects interact with one another.

**Example:** `Student → submits → Request`

| No. | Object 1 | Interacts | Object 2 |
|:---:|---|---|---|
| 1 | Leader | assigns | Cleaning Task |
| 2 | Cleaner | views | Cleaning Schedule |
| 3 | Cleaner | cleans | Classroom |
| 4 | Cleaner | updates | Attendance |
| 5 | Cleaner | Cleaner | Evaluation |
| 6 | Leader | inspects | Classroom |
| 7 | Leader | records | Evaluation / Feedback |
| 8 | Teacher | monitors | Attendance |

---

## Part 3. Identify Possible Classes

Determine which objects can become classes in your proposed system.

Not every object needs to become a class. Choose only the objects that are important to your proposed system.

| No. | Class | What does it represent? |
|:---:|---|---|
| 1 | Teacher | Represents the class adviser who oversees overall cleanliness reports and student compliance. |
| 2 | Student | The parent class representing any student in the class, holding shared info and attendance/cleaning status. |
| 3 | Cleaner | A child class of Student representing regular cleaners who perform duties and rate their own work. |
| 4 | Leader | A child class of Student representing the class officer/leader who assigns tasks, rates quality/time, and gives feedback. |
| 5 | CleaningTask | Represents an individual cleaning assignment, including the area to clean, completion status, and ratings. |

---

## Part 4. Class Analysis

Analyze the attributes and methods of each identified class.

### Class No. 1

**Class Name: Teacher** 

**Purpose: Supervises the classroom cleaning system, reviews cleaning records, and monitors student participation and feedback.**  
__________________________________________________

#### Attributes

| Attribute | Description |
|---|---|
|teacherID|Unique identifier for the teacher.|
|name|Full name of the teacher.|
|advisorySection |The class section supervised by the teacher.|
|remarks|General notes or approval comments on classroom cleanliness.|

#### Methods

| Method Name | What does it do? |
|---|---|
|viewSchedule()|Displays the daily or weekly cleaning assignments for the section.|
|viewRecords()|Checks student attendance, task completion statuses, and leader ratings.|
|addRemarks()|Records overall feedback or disciplinary notes regarding classroom cleanliness.|
|approveReport()|Verifies and approves the weekly or daily cleaning log.|

---

### Class No. 2

**Class Name:** Student (parent class)

**Purpose:**  
Base class that stores basic student information, attendance, and cleaning status.

#### Attributes

| Attribute | Description |
|---|---|
|name|Name of the student.|
|section|Section of the student.|
|status|Status if present, absent, cleaned, or still working.|


#### Methods

| Method Name | What does it do? |
|---|---|
|UpdateStatus()|Marks if they cleaned or missed duty, and records their attendance.|

---

### Class No. 3

**Class Name:** Cleaner(Student)

**Purpose:**  
Regular student assigned to perform cleaning duties and updates their tracking/cleaning sheets.

#### Attributes

| Attribute | Description |
|---|---|
|(Inherited)|Inherits name, section, and status from Student.|
|assignedTask|Their assigned task or duty.|


#### Methods

| Method Name | What does it do? |
|---|---|
|(Inherited)|Uses updateStatus() from Student.|
|rateSelf()|Cleaners can evaluate their own work.|


---

### Class No. 4

**Class Name:** Leader(Student)

**Purpose:**  
A student leader who oversees the group, evaluates the members' work, and provides feedback.
#### Attributes

| Attribute | Description |
|---|---|
|(Inherited)|Inherits name, section, and status from Student.|
|assignedTask|Their assigned task or duty.|


#### Methods

| Method Name | What does it do? |
|---|---|
|(Inherited)|Uses updateStatus() from Student.|
|rateQuality()|Scores the cleanliness of a member's job. (out of 10)|
|rateTime()|Scores efficiency and time spent cleaning. (out of 10)|
|giveFeedback()|Write comments for group members.|


---

## Part 5. Identify Class Relationships

Determine how your identified classes are related to one another.

| No. | Class 1 | Relationship | Class 2 | Why are they related? |
|:---:|---|---|---|---|
| 1 | Teacher | association | cleaner leader | teacher selects leader and assigns them to cleaner leader |
| 2 | Teacher | association | cleaner member | teacher selects member into groups and gives ratings |
| 3 | Cleaner leader | association | cleaner member | leader rates work quality and time for each member |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |

### Relationship Types

| Relationship | Description |
|---|---|
| **Association** | Two classes interact with one another. |
| **Aggregation** | One class groups or contains objects that can exist independently. |
| **Composition** | One class strongly owns another object. |
| **Inheritance** | One class is a specialized version of another class. |

**Reminder:** Use only the relationship types that make sense for your proposed system. Not all relationship types are required.
