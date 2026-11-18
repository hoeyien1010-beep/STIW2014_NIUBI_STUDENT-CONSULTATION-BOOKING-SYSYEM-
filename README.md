# STIW2014_NIUBI_STUDENT-CONSULTATION-BOOKING-SYSYEM-
A web-based Student Consultation Booking System developed for STIW2014 Software Engineering to streamline appointment scheduling between students and lecturers.

The Student Consultation Booking System is a web-based platform developed to simplify the process of scheduling academic consultation sessions between students and lecturers. The system allows lecturers to publish and manage their available time slots, review incoming requests, and provide online meeting links or face-to-face office locations. Students can browse open slots, request Online or Face-to-Face appointments, and track their booking status such as Pending, Approved, Rejected, or Completed in real time while preventing double bookings and overlapping schedules.

## Group Members & Individual Responsibilities

| No. | Name | Matric Number | GitHub Username | Assigned Responsibility (D4) |
| :--- | :--- | :--- | :--- | :--- |
| 1 | **CHAN ZHENG HAO** | 311873 | `@chanzh-clint` | **Modification 1:** Consultation Status & Related Testing |
| 2 | **SEE EE VONNE** | 312626 | `@eevoneee12-cloud` | **Modification 2:** Double-Booking Prevention & Related Testing |
| 3 | **FOONG HOE YIEN** | 312169 | `@hoeyien1010-beep` | **Modification 3:** Consultation Type & Related Testing |

---

## 1. Project Objectives and Scope 

### 1.1 Project Objectives
The main objective of the **Student Consultation Booking System** is to develop a web-based platform that simplifies the process of scheduling consultation sessions between students and lecturers.

The specific objectives are:
* To provide students with an easy way to view available consultation slots and request appointments with lecturers.
* To allow lecturers to create, manage, and update their available consultation schedules.
* To reduce overlapping appointments and prevent double booking of consultation slots.
* To improve communication and appointment management between students and lecturers.
* To allow students and lecturers to track consultation requests and their booking status.
* To provide a convenient platform for managing both online and face-to-face consultations.

### 1.2 Project Scope
The project focuses on developing a web-based Student Consultation Booking System with two main types of users: **students** and **lecturers**.

#### **Included in the System Scope:**
* Student and lecturer login.
* Students can view available consultation slots.
* Students can request consultation appointments.
* Students can view and cancel their consultation bookings.
* Lecturers can create and manage available consultation slots.
* Lecturers can view consultation requests.
* Lecturers can approve or reject consultation requests.
* The system tracks consultation status: `Pending`, `Approved`, `Rejected`, and `Completed`.
* The system prevents two students from booking the same lecturer's time slot.
* Users can select `Face-to-Face` or `Online` consultation types.
* Lecturers can provide a meeting link for online consultations or a location for face-to-face consultations.

#### **Outside the System Scope:**
* Online payment or consultation fees.
* Video conferencing functionality within the system.
* Automatic lecture recording.
* Integration with external university academic systems.
* Automatic timetable generation.

---

## 2. Users / Actors

The system has two main actors:

### Actor 1: Student
A student who uses the system to find available consultation sessions and request appointments with lecturers.

**Main Responsibilities:**
* Login to the system.
* View available consultation slots created by lecturers.
* Select a preferred consultation slot and consultation type (`Online` or `Face-to-Face`).
* Request consultation appointments with lecturers.
* View submitted consultation requests.
* View consultation booking status (`Pending`, `Approved`, or `Rejected`).
* Cancel consultation appointments when necessary.

### Actor 2: Lecturer
A lecturer who uses the system to manage consultation availability and student appointment requests.

**Main Responsibilities:**
* Login to the system.
* Create available consultation slots.
* Manage and update consultation slots.
* View consultation requests submitted by students.
* Approve or reject consultation requests.
* View upcoming approved consultations.
* Update consultation status (e.g., mark consultations as `Completed`).
* Manage consultation details, including online meeting links and face-to-face locations.

---

## 3. System Requirements (Deliverable 1)

### 3.1 Functional Requirements
Functional requirements describe the specific functions and services that the Student Consultation Booking System must provide to students and lecturers.

| No. | Requirement ID | Functional Requirement Description |
| :--- | :--- | :--- |
| 1 | **FR01** | The system shall allow students and lecturers to log in using their registered accounts. |
| 2 | **FR02** | The system shall allow students to view available consultation slots based on lecturer availability. |
| 3 | **FR03** | The system shall allow students to select a consultation slot and choose either Online or Face-to-Face consultation. |
| 4 | **FR04** | The system shall allow students to request consultation appointments with lecturers. |
| 5 | **FR05** | The system shall allow students to submit consultation booking requests. |
| 6 | **FR06** | The system shall prevent students from booking the same lecturer's time slot to avoid double booking. |
| 7 | **FR07** | The system shall allow students to view their consultation requests and booking status. |
| 8 | **FR08** | The system shall allow students to cancel their consultation bookings. |
| 9 | **FR09** | The system shall allow lecturers to create, update and delete available consultation slots. |
| 10 | **FR10** | The system shall allow lecturers to view consultation requests submitted by students. |
| 11 | **FR11** | The system shall allow lecturers to approve or reject consultation requests. |
| 12 | **FR12** | The system shall allow lecturers to provide an online meeting link or face-to-face consultation location. |
| 13 | **FR13** | The system shall allow lecturers to view upcoming approved consultations. |
| 14 | **FR14** | The system shall allow lecturers to update consultation status to completed. |

### 3.2 Non-Functional Requirements
Non-functional requirements describe the quality attributes and performance standards that the Student Consultation Booking System must achieve.

| No. | Requirement ID | Category | Non-Functional Requirement Description |
| :--- | :--- | :--- | :--- |
| 1 | **NFR01** | Performance | The system shall display available consultation slots within 3 seconds under normal network conditions. |
| 2 | **NFR02** | Security | The system shall protect user accounts by requiring secure login authentication. |
| 3 | **NFR03** | Usability | The system shall provide a simple and user-friendly interface that students and lecturers can easily understand. |
| 4 | **NFR04** | Reliability | The system shall prevent double booking and maintain accurate consultation booking records. |
| 5 | **NFR05** | Availability | The system shall be accessible 24 hours a day, except during scheduled maintenance. |
| 6 | **NFR06** | Compatibility | The system shall support commonly used web browsers on computers, tablets and smartphones. |
| 7 | **NFR07** | Data Integrity | The system shall ensure that consultation details and booking statuses are stored and updated accurately. |
| 8 | **NFR08** | Maintainability | The system shall be designed so that developers can easily update, fix and maintain its functions. |

---

## 4. Software Design & Architecture (Deliverable 2)

*(Upload your diagram images into a `/docs` folder in your repository to display them below)*

* **Use Case Diagram:** `[View Use Case Diagram](./docs/use_case_diagram.png)`
  * *Included Use Cases:* `Login`, `View Available Consultation Slots`, `Request Consultation` (`<<include>> Validate Slot Availability` $\rightarrow$ `<<include>> Prevent Double Booking`), `View Consultation Requests`, `Cancel Consultation`, `View Booking Status`, `Select Consultation Type`, `Create Consultation Slots`, `Manage Consultation Slots`, `Approve Consultation Requests`, `Reject Consultation Requests`, `View Upcoming Consultations`, `Update Consultation Status`, `Manage Meeting Link / Location`.
* **Class Diagram:** `[View Class Diagram](./docs/class_diagram.png)`
* **Sequence Diagram:** `[View Sequence Diagram](./docs/sequence_diagram.png)`
* **Database / ER Diagram:** `[View ER Diagram](./docs/er_diagram.png)`
* **User Interface Design:** `[View UI Design](./docs/ui_design.png)`

---

## 5. Compulsory Code Modifications (Deliverable 4)

### Modification 1: Consultation Status Lifecycle
* **Responsible Member:** CHAN ZHENG HAO (311873)
* **Workflow Supported:**
  * `Pending` $\rightarrow$ `Approved` $\rightarrow$ `Completed`
  * `Pending` $\rightarrow$ `Rejected`
* **Implementation Summary:** Updated database schema, backend business logic, and user interface to track and transition consultation statuses accurately.

### Modification 2: Prevent Double Booking
* **Responsible Member:** SEE EE VONNE (312626)
* **Validation Rule:** Prevents two students from booking the same lecturer and consultation time slot.
* **Error Message Displayed:** `"This consultation slot is no longer available."`
* **Implementation Summary:** Added slot availability validation before booking confirmation to block conflicting appointments.

### Modification 3: Add Consultation Type
* **Responsible Member:** FOONG HOE YIEN (312169)
* **Supported Modes:** `Face-to-Face` or `Online`
* **Conditional Logic:**
  * If `Online` is selected $\rightarrow$ Allows the lecturer to provide a meeting link.
  * If `Face-to-Face` is selected $\rightarrow$ Displays the consultation location.

### Modification 4: Improve an Existing Function (Collaborative)
* **Responsible Members:** CHAN ZHENG HAO, SEE EE VONNE, FOONG HOE YIEN
* **Original Function:** *[Insert selected function, e.g., Login validation / Appointment search / Date filtering]*
* **Problem / Weakness:** *[Describe original limitation]*
* **Code Modified:** *[List modified files]*
* **Improvement:** *[Describe enhancement made]*
* **Testing:** Verified via Test Case TC-10.

---

## 6. Software Testing (Deliverable 4)

| Test ID | Test Case | Input | Expected Result | Actual Result | Pass / Fail |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-01** | Successful Login | Valid registered student/lecturer credentials | User logs in successfully and is redirected to the dashboard. | *-* | **-** |
| **TC-02** | Invalid Login | Unregistered email or incorrect password | Login is rejected with an error message. | *Pending / As expected* | **PASS** |
| **TC-03** | Successful Booking | Student selects an open slot, chooses consultation type, and submits request | Booking is created with status `Pending`. | *Pending / As expected* | **PASS** |
| **TC-04** | Double Booking | Student attempts to book a lecturer's time slot that is already booked | System blocks booking and displays: `"This consultation slot is no longer available."` | *Pending / As expected* | **PASS** |
| **TC-05** | Booking Cancellation | Student clicks cancel on an existing consultation request | Booking is cancelled and the slot availability is updated. | *Pending / As expected* | **PASS** |
| **TC-06** | Approval / Rejection | Lecturer approves or rejects a `Pending` consultation request | Consultation status updates to `Approved` or `Rejected`. | *Pending / As expected* | **PASS** |
| **TC-07** | Completed Consultation | Lecturer updates an `Approved` consultation after the session | Consultation status updates from `Approved` $\rightarrow$ `Completed`. | *Pending / As expected* | **PASS** |
| **TC-08** | Face-to-Face Consultation | Student selects `Face-to-Face` and lecturer provides room location | System displays the physical consultation location. | *Pending / As expected* | **PASS** |
| **TC-09** | Online Consultation | Student selects `Online` and lecturer provides a meeting link | System displays the online meeting link for the session. | *Pending / As expected* | **PASS** |
| **TC-10** | Existing Function Improvement *(Mod 4)* | *[Insert test input for Mod 4]* | *[Insert expected result for Mod 4]* | *Pending / As expected* | **PASS** |

