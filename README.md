# 🌿 Agro Scan  
**Group D – PRT681 Software Testing Project**


##  Team Members

| Role | Name | Student ID | GitHub Folder |
|------|------|-------------|----------------|
|  **Tester** | **Musrat Jahan** | S380098 | [Tester Folder](https://github.com/25S2-PRT681-Group-D/Tester_Musrat) |
|  **Senior Developer** | **Haohua Mai** |  S371832 | [Server Repo](https://github.com/25S2-PRT681-Group-D/server) / [Web Repo](https://github.com/25S2-PRT681-Group-D/web) |
|  **Junior Developer** | **Ritiz Karkee** | S372192 | [Server Repo](https://github.com/25S2-PRT681-Group-D/server) / [Web Repo](https://github.com/25S2-PRT681-Group-D/web) |
|  **Business Analyst** | **Quoc Chien Kieu** | S374001 | [BA Folder](https://github.com/25S2-PRT681-Group-D/business_analyst) |


##  GitHub Repository

- **Repository Name:** `25S2_PRT681_GROUP_D`  
- **Repository URL:** [https://github.com/25S2-PRT681-Group-D](https://github.com/25S2-PRT681-Group-D)



##  Group Collaboration

- **Platform:** Microsoft Teams  
- **Channel:** Group D  
- **Channel URL:** [Group D Teams Channel](https://teams.microsoft.com/l/channel/19%3Af3727d1405ce40a8bab190d9c155236e%40thread.tacv2/Group-D?groupId=4ccfbc39-217a-4425-80bd-cb87296d1d50&tenantId=9f248767-8e1a-42f3-836f-c092ab95ff70)



##  Project Overview

**Agro Scan** is an AI-based agricultural inspection system that allows users to upload plant photos for automated health analysis.  
The system diagnoses plant health, classifies diseases, and allows admins to manage users, records, and monitor performance.

###  Key Features
- Upload plant images for AI-based disease detection  
- View health results and recommendations  
- Manage inspection history and records  
- Admin dashboard for system performance and user management  

🔗 **Live URL:** [http://170.64.225.221:5173](http://170.64.225.221:5173) *(inactive)*  

![Agro Scan Homepage](https://github.com/25S2-PRT681-Group-D/Tester_Musrat/blob/main/AgroScan_homepage.png)



##  Testing Overview

Testing verified both functional and non-functional requirements through manual and automated approaches.

---

###  Test Objectives
- Validate image upload, AI response, and record management  
- Verify API data exchange and backend accuracy  
- Assess UI performance and error handling  
- Perform load and performance testing under multiple requests  
- Identify vulnerabilities through active and passive scanning  

---

##  Test Cases

| Test ID | Feature | Description | Expected Result | Actual Result | Status |
|----------|----------|--------------|----------------|---------------|--------|
| TC01 | Navigate | Navigate homepage | Display homepage | Homepage loaded |  Passed |
| TC02 | Login | Login with valid credentials | Redirect to dashboard | Successful |  Passed |
| TC03 | Login | Invalid credentials | Error message | Message displayed |  Passed |
| TC04 | Upload | Upload plant image | Display AI result | Not Working |  Fail |
| TC05 | Upload | Upload invalid image | Error message | Not Working |  Fail |
| TC06 | Record View | Display inspection records | Records visible | Working |  Fail |
| TC07 | Admin Panel | Access as Admin | Admin dashboard loads | Not Working |  Fail|
| TC08 | Logout | Logout function | Redirect to login page | Working |  Passed |

---

##  API Testing — *Postman*

**Tool:** [Postman](https://www.postman.com/)  
**Goal:** Validate backend endpoints, database connections, and data accuracy.

| Endpoint | Method | Purpose | Status |
|-----------|---------|----------|--------|
| `/upload` | POST | Upload plant image for AI analysis |  200 OK |
| `/result/:id` | GET | Retrieve analysis result | 200 OK |
| `/users/login` | POST | Login verification |  201 Created |
| `/records` | GET | Fetch user inspection records |  200 OK |

 Postman: [`/Tester/API Testing`](https://github.com/25S2-PRT681-Group-D/Tester_Musrat/tree/main/API%20Testing)

### Screenshots
![Postman ](https://github.com/25S2-PRT681-Group-D/Tester_Musrat/blob/main/API%20Testing/PostmanAgroScan.png)  

---

## UI Automation Testing — *Selenium (Python)*

**Tool:** [Selenium WebDriver](https://www.selenium.dev/)  
**Goal:** Automate web UI to ensure reliable navigation and functionality.

###  Tests
- Homepage navigation test  
- Image upload automation  
- Login and logout flow  
- Admin dashboard access  

**Environment:** Chrome + Python (WebDriver Manager)

 Selenium: [`/Tester/Selenium`](https://github.com/25S2-PRT681-Group-D/Tester_Musrat/tree/main/Selenium)

###  Screenshots
![Selenium Homepage Test](https://github.com/25S2-PRT681-Group-D/Tester_Musrat/blob/main/Selenium/Selenium%20Agro%20Scan.png)  


---

##  Performance Testing — *Apache JMeter*

**Tool:** [Apache JMeter](https://jmeter.apache.org/)  
**Goal:** Measure API performance, concurrent user load, and server response.

###  Scenarios
- 50 users uploading plant images  
- AI result endpoint load test  
- Server throughput and response time tracking  

**Metrics:** Avg Response Time | Throughput | Error %  

 JMeter: [`/Tester/Performance Testing`](https://github.com/25S2-PRT681-Group-D/Tester_Musrat/tree/main/Performance%20Testing)

###  Screenshots
![JMeter Http request](https://github.com/25S2-PRT681-Group-D/Tester_Musrat/blob/main/Performance%20testing/JmeterAgroScan.png)

Website is notworking, so, request can not be passed.
---
##  Security Testing — *OWASP ZAP*

**Tool:** [OWASP ZAP](https://www.zaproxy.org/)  
**Goal:** Detect and mitigate potential security vulnerabilities.

###  Scans Performed
- Active Scan (SQL Injection, Broken Auth)  
- Passive Scan (Header & Cookie Analysis)  
- XSS and CSRF Testing  

 ZAP: [`/Tester/Security Testing`]( https://github.com/25S2-PRT681-Group-D/Tester_Musrat/tree/main/Security%20Testing)

###  Screenshots
![ZAP Dashboard](https://github.com/25S2-PRT681-Group-D/Tester_Musrat/blob/main/Security%20Testing/ZAP/AgroScan_ZAP_SS.png))  

Website is notworking, so, alerts can not be captured.
---


