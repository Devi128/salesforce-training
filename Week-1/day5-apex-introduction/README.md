## 1. What is Apex?

Apex is a strongly typed, object-oriented programming language used in Salesforce. It allows developers to implement complex business logic, automate processes, and perform database operations that go beyond declarative tools like Flow.
Apex runs on the Salesforce platform and works closely with CRM data such as Accounts, Contacts, Leads, and custom objects.

---

## 2. Difference

### Flow vs Apex

| Flow (No-Code) | Apex (Code) |
|----------------|------------|
| Drag-and-drop automation | Written in code |
| Easy for admins | Used by developers |
| Handles simple logic | Handles complex logic |
| Faster development | More flexible and powerful |
| Declarative tool | Programmatic approach |

Example:
- Flow → Send email when a record is created  
- Apex → Complex logic with API callouts + conditions + bulk processing  

---

### Configuration vs Coding

| Configuration | Coding (Apex) |
|--------------|--------------|
| Done using UI | Written in code |
| Low complexity | High complexity |
| No programming needed | Programming required |
| Example: Validation Rules | Example: Triggers, Classes |

---

## 3. Real Examples Where Apex Is Needed

1. **Complex Calculations**
   - Example: Scholarship calculation based on marks, income, and attendance.

2. **External Integrations**
   - Example: Sending Salesforce data to a payment gateway or university portal API.

3. **Advanced Business Rules**
   - Example: Prevent deleting a student record if fees are pending or courses are active.

---

## 4. Integrated System Design – College Management System

### CRM
Salesforce acts as the central CRM system storing all college-related data.

---

### Objects

- Student__c  
- Course__c  
- Faculty__c  
- Enrollment__c  
- Fee__c  

---

### Relationships

- Student → Enrollment (One-to-Many)  
- Course → Enrollment (One-to-Many)  
- Faculty → Course (Lookup / Master-Detail)

---

### Validation Rules

- Student age must be >= 17  
- Fee amount must be greater than 0  
- Enrollment must have a selected course  

---

### Flow

- Auto-create enrollment when a student is admitted  
- Send email when fee is paid  
- Update student status when course is completed  

---

### Apex

Apex is used for:

- Complex fee calculations  
- Grade calculation logic  
- Bulk data processing  
- Integration with external systems  

---

## 5. Pseudocode Examples

### Fee Discount Logic

IF marks > 90 THEN
discount = 20%
ELSE IF marks > 75 THEN
discount = 10%
ELSE
discount = 0%


---

### Enrollment Check

IF student already enrolled in course THEN
prevent duplicate enrollment

---

### Grade Calculation
IF score >= 90 THEN Grade = A
ELSE IF score >= 75 THEN Grade = B
ELSE Grade = C


---

## 6. Reflection

Enterprise systems start with no-code tools, but eventually require programming because real-world business logic becomes complex and cannot always be handled using configuration tools alone.

Apex provides flexibility, scalability, and control for implementing advanced logic.

---

## Reflective Questions

### 1. Why is Apex needed if Salesforce already has Flows?
Flows handle simple automation, while Apex is required for complex logic, integrations, and advanced processing.

---

### 2. When should developers prefer no-code solutions?
When the process is simple, repetitive, and does not require complex logic.

---

### 3. What problems require custom programming?
- Complex calculations  
- External integrations  
- Bulk data processing  
- Advanced conditional logic  

---

### 4. Why is business logic important in enterprise systems?
It ensures consistency, accuracy, and automation of real-world business rules.

---

### 5. Why should developers avoid unnecessary coding?
Because code increases maintenance cost and complexity when simpler tools can solve the problem.

---

### 6. How does programming increase flexibility?
It allows dynamic logic, reusable code, and integration with external systems, making the system scalable.
