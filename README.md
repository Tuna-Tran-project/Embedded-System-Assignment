
# Embedded-System-Assignment

Here is a requirements document for a **Checking Attendance Using RFID**:

---

# Checking Attendance Using RFID

## **1. Introduction**

### **1.1 Purpose**

The purpose of this document is to define the functional and non-functional requirements for a system that uses **Radio Frequency Identification (RFID)** technology to automate the process of checking student attendance. The system is intended to replace manual roll-calling methods with a faster, more accurate, and contactless alternative.

### **1.2 Scope**

The system will:

* Automate student attendance recording using RFID tags and readers.
* Provide real-time tracking and logging of attendance records.
* Generate reports and alerts for absent or late students.
* Allow administrators and teachers to monitor attendance via a web interface or local display.

---

## **2. Functional Requirements**

### **2.1 Student Registration and Tag Assignment**

* The system shall allow administrators to register students and assign each one a unique RFID tag.
* The system shall store student details including name, ID number, class, and RFID tag ID.

### **2.2 Attendance Detection via RFID**

* The system shall use an RFID reader installed at the classroom entrance.
* When a student with a valid RFID tag enters the classroom, the system shall detect the tag and mark the student as **present**.
* The system shall log the **check-in time**.
* If a student checks in after a predefined time threshold, the system shall mark the student as **late**.
* The system shall ignore duplicate scans from the same tag during one session.

### **2.3 Teacher/Admin Interface**

* The system shall allow teachers or admins to view a **list of present, late, and absent students**.
* The system shall allow exporting attendance data in formats such as CSV or Excel.
* The system shall provide functionality to manually override attendance in case of tag failure.

### **2.4 Real-time Notifications**

* The system shall optionally send email or SMS notifications to parents in case of absence or lateness.
* The system shall notify teachers in real-time via display or dashboard.

### **2.5 Server Database**

* All attendance data shall be stored in a structured SQL database.
* The system shall support backups and data recovery.

---

## **3. Non-Functional Requirements**

### **3.1 Performance**

* The RFID reader shall detect and log a student tag within **1 second**.
* The system shall be able to handle **at least 50 students** arriving simultaneously without failure.

### **3.2 Security**

* The system shall encrypt stored student data and restrict access to authorized personnel only.
* Unauthorized tag scans shall be logged and flagged.

### **3.3 Reliability and Availability**

* The system shall achieve **99% uptime** during school hours.
* The RFID hardware should support **at least 100,000 scans** before replacement.

### **3.4 Maintainability and Scalability**

* The system shall allow administrators to add new classes, students, or devices without code changes.
* The design shall support integration into larger school management systems.

---

## **4. Hardware and Software Requirements**

### **4.1 Hardware Requirements**

| Component                       | Description                                                          |
| ------------------------------- | -------------------------------------------------------------------- |
| **Microcontroller Unit (MCU)**  | ESP32 / Arduino Uno / STM32 to interface with RFID reader and server |
| **RFID Reader Module**          | MFRC522 or compatible HF reader for scanning RFID tags               |
| **RFID Tags**                   | Passive RFID cards (13.56 MHz), one per student                      |
| **OLED/LCD Display (Optional)** | Display attendance status or messages to student/teacher             |
| **Buzzer / LED**                | Signal success or failure during scanning                            |
| **Push Buttons**                | Manual override, reset, or mode switching (optional)                 |
| **Wi-Fi or Ethernet Module**    | Built-in (ESP32) or external module for communication with server    |
| **Power Supply**                | 5V regulated supply for MCU and reader module                        |

---

### **4.2 Software Requirements**

| Software Component       | Description                                                               |
| ------------------------ | ------------------------------------------------------------------------- |
| **Embedded Firmware**    | Code to control RFID reader, read tags, and send data via serial or Wi-Fi |
| **Database System**      | MySQL / PostgreSQL to store attendance records and student info           |
| **Web Server / Backend** | Python Flask / Node.js / PHP to receive data and serve dashboard          |
| **Admin Dashboard**      | Web interface for teachers/admin to view reports and student records      |
| **Notification Module**  | Optional integration with email (SMTP) or SMS (Twilio/Firebase) APIs      |
| **Driver Libraries**     | RFID and Wi-Fi libraries compatible with the chosen microcontroller       |

---

## **5. Assumptions and Constraints**

* Each student must carry their assigned RFID tag during class time.
* RFID readers must be installed and powered near classroom entrances.
* The system assumes that only one student enters at a time for accurate scan.
* A stable **Wi-Fi or LAN connection** is required for real-time data sync and notifications.
* The RFID reader’s range is assumed to be **<10 cm** to prevent misreads.
* The school must ensure physical security of hardware to prevent tampering.

---
