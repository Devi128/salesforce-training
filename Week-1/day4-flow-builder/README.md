# Day 4 - Flow Builder

## 1. What is Flow Builder?

Flow Builder is a Salesforce automation tool used to automate business processes without writing code. It helps users create workflows using drag-and-drop elements such as screens, decisions, assignments, loops, and actions.

Using Flow Builder, organizations can:
- Automate repetitive tasks
- Update records automatically
- Send emails and notifications
- Collect user input
- Improve productivity and accuracy

Flow Builder is widely used in enterprise applications to simplify business operations.

---

# 2. Types of Flows

Salesforce provides different types of flows based on business requirements.

## Screen Flow

Screen Flow is an interactive flow that displays screens to users and collects input.

### Features
- User interaction through forms/screens
- Used for guided processes
- Can update or create records
- Supports buttons, choices, and validations

### Example
A student registration form where students enter:
- Name
- Course
- Email
- Phone number

After submission:
- Student record is created
- Confirmation message is displayed

---

## Record-Triggered Flow

Record-Triggered Flow runs automatically when a record is:
- Created
- Updated
- Deleted

### Features
- Fully automated
- No user interaction required
- Executes in the background
- Replaces workflow rules and process builder

### Example
When a new student registers:
- Send welcome email automatically
- Update available seats count
- Notify faculty

---

# 3. Automation Ideas

## College Management System Automation Processes

### 1. Auto Email After Registration
When a student completes registration, an automatic confirmation email is sent.

### 2. Auto Update Remaining Seats
Whenever a student enrolls in a course, the available seat count decreases automatically.

### 3. Notify Faculty When Course is Full
When the course reaches maximum capacity, faculty receives a notification.

### 4. Generate Student ID Automatically
A unique student ID is generated after successful admission.

### 5. Send Reminder Before Fee Deadline
Students receive reminder emails/SMS before the fee due date.

---

# 4. Flow Diagram

## Selected Automation:
Auto Email After Registration

### Flow Steps

1. Trigger:
   Student registration record is created

2. Get Student Details

3. Decision:
   Check if email exists

4. Action:
   Send confirmation email

5. Final Action:
   Update status as "Email Sent"

---

## Simple Flow Diagram

```text
+----------------------+
| Student Registers    |
+----------+-----------+
           |
           v
+----------------------+
| Get Student Details  |
+----------+-----------+
           |
           v
+----------------------+
| Email Available?     |
+----+------------+----+
     | Yes             | No
     v                 v
+----------------+   End
| Send Email     |
+--------+-------+
         |
         v
+----------------------+
| Update Status        |
| "Email Sent"         |
+----------------------+

---

# 5. Manual vs Automated Process

| Manual Process                 | Automated Process         |
| ------------------------------ | ------------------------- |
| Staff sends emails manually    | Emails sent automatically |
| Human errors possible          | Reduced errors            |
| Time-consuming                 | Fast execution            |
| Requires continuous monitoring | Runs automatically        |
| Delayed communication          | Instant notifications     |

---

# 6. Reflection

Automation is important in enterprise systems because it:
- Saves time
- Reduces manual work
- Improves accuracy
- Increases productivity
- Enhances user experience

In a College Management System, automation helps administrators, faculty, and students by simplifying daily operations. It ensures faster communication, better record management, and efficient handling of large amounts of data.

Flow Builder is a powerful no-code tool that enables organizations to automate processes easily and improve operational efficiency.
