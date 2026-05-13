# Day 3 - Data Modeling

## 1. Difference Between App, Object, Record, and Field

| Term | Description | Example |
|------|-------------|----------|
| App | A collection of related functionalities used for a specific purpose | College Management App |
| Object | A database table that stores related data | Student Object |
| Record | A single row of data inside an object | One student's details |
| Field | A column that stores specific information | Student Name, Age |

---

# 2. Standard vs Custom Objects

| Standard Objects | Custom Objects |
|------------------|----------------|
| Pre-built by Salesforce | Created by users |
| Already available in Salesforce | Designed based on business needs |
| Example: Account, Contact | Example: Student__c, Course__c |

### Examples

#### Standard Object
- Contact
- Account

#### Custom Object
- Student__c
- Faculty__c
- Course__c

---

# 3. College Data Model

## Objects Used

### Student__c
Stores student information.

Fields:
- First_Name__c
- Last_Name__c
- Age__c
- Email__c
- Department__c

### Faculty__c
Stores faculty details.

Fields:
- Faculty_Name__c
- Subject__c
- Email__c

### Course__c
Stores course information.

Fields:
- Course_Name__c
- Course_Code__c
- Credits__c

### Enrollment__c
Used to connect students and courses.

Fields:
- Student__c
- Course__c
- Enrollment_Date__c

---

## Relationships

| Object 1 | Relationship | Object 2 |
|----------|--------------|-----------|
| Student__c | Enrolls In | Course__c |
| Faculty__c | Teaches | Course__c |
| Enrollment__c | Connects | Student and Course |

### Relationship Types

- Lookup Relationship
- Master-Detail Relationship

---

## Data Model Diagram

![College Data Model](college-data-model.png)

---

# 4. Formula Fields

## Example 1: Full Name Formula

### Formula
```salesforce
First_Name__c & " " & Last_Name__c
```

### Explanation
This formula combines first name and last name into a single full name.

---

## Example 2: Course Duration Status

### Formula
```salesforce
IF(Credits__c > 3, "Advanced Course", "Basic Course")
```

### Explanation
If credits are greater than 3, the course is considered an advanced course.

---

# 5. Validation Rules

## Example 1: Age Validation

### Rule
```salesforce
Age__c < 17
```

### Error Message
```text
Student age must be at least 17.
```

### Explanation
Prevents users from entering students younger than 17 years.

---

# 6. Reflection

Structured enterprise data is important because it helps organizations manage information efficiently and accurately.

In a college management system, structured data helps:
- Store student and faculty details properly
- Reduce duplicate information
- Improve data security
- Generate reports easily
- Maintain relationships between different objects

Using proper data modeling makes applications scalable, organized, and easy to maintain.

---

# Conclusion

This project demonstrates the basics of Salesforce data modeling including:
- Objects
- Relationships
- Formula Fields
- Validation Rules
- Enterprise Data Structure

