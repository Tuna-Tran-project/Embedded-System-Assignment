# Embedded-System-Assignment
Here is a requirements document for a **Smart Parking System Using RFID**:  

---

# **Smart Parking System Using RFID **  

## **1. Introduction**  
### **1.1 Purpose**  
The purpose of this document is to define the functional and non-functional requirements for a **Smart Parking System** that uses **Radio Frequency Identification (RFID)** technology to automate vehicle entry, exit, and parking fee management.  

### **1.2 Scope**  
The system will:  
- Automate vehicle identification using RFID tags and readers.  
- Provide security and access control.  

---

## **2. Functional Requirements**  

### **2.1 User Registration and Authentication**  
- The system shall allow vehicle owners to register their vehicles by assigning unique RFID tags.  
- The system shall store user details such as vehicle number, owner information.  

### **2.2 RFID-Based Vehicle Detection**  
- The RFID reader at the entrance shall detect and authenticate the vehicle’s RFID tag.  
- If the vehicle is registered, the barrier gate shall automatically open.  
- The system shall log the **entry time** and assign a parking slot.  
- The RFID reader at the exit shall detect the vehicle's RFID tag and log the **exit time**.  

### **2.2 Security and Access Control**  
- The system shall prevent unauthorized vehicles from entering.  
- The system shall maintain an audit log of all entries and exits.  
- The system shall integrate CCTV cameras for additional security.  

### **2.6 Server Database**  
- All information about user vehicles is stored in SQL database 

---

## **3. Non-Functional Requirements**  

### **3.1 Performance**  
- The RFID reader shall detect and process a vehicle within **2 seconds**.  
- The system shall handle up to **500 concurrent vehicles** in large parking lots.  

### **3.2 Security**  
- Unauthorized access attempts shall trigger alerts.  

### **3.3 Reliability and Availability**  
- The RFID tags shall be weather-resistant and last at least **5 years**.  

### **3.4 Maintainability and Scalability**  
- The system shall allow **easy integration** with existing parking infrastructure.  
- The system shall be **scalable** to support additional parking lots and users.  

---

## **4. Hardware and Software Requirements**  

### **4.1 Hardware Components**  
- **RFID Tags** – Passive UHF RFID tags for vehicle identification.  
- **RFID Readers** – Fixed UHF RFID readers installed at entry and exit points.  
- **Barrier Gates** – Automated gates controlled by the system.   
- **OLED Display Panels** – For showing parking slot availability.  

### **4.2 Software Components**  
- **Backend System** – Database management, user authentication.
- **Web Database** – Admin dashboard for monitoring and reporting.  

---

## **5. Assumptions and Constraints**  
- Vehicles must have an RFID tag installed for automatic entry/exit.  
- The system requires stable **internet connectivity** for real-time updates.  
---

## **6. Conclusion**  
The **Smart Parking System using RFID** aims to **streamline vehicle entry and enhance security**, providing a seamless parking experience for users and efficient management for parking operators.  

---
