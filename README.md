# Manual-Testing-Project-Login-Functionality

---

**Project 1: Login Functionality Testing**
 **Test Plan**
- *Objective*: Ensure that the login functionality of the web application works as intended, allowing valid users to log in while restricting unauthorized access.
- **Scope**:  
  - Test Login Page UI and functionality.  
  - Validate positive and negative test cases for login.  
  - Ensure proper error messages for invalid inputs.  
  - Verify compatibility across browsers.  
- **In-Scope Testing Types**:  
  - Functional Testing  
  - Usability Testing  
  - Compatibility Testing  
  - Security Testing  
- **Out of Scope**: Social login (Google, Facebook).  
- **Test Environment**: Windows 11, Google Chrome v120, Mozilla Firefox v118.  
- **Test Data**: Username, Password (Valid/Invalid), Blank Fields.  
- **Risks and Assumptions**: Risk of inconsistent network connectivity; assuming no major UI changes during testing.  

---

 **Test Cases**  
| **Test Case ID** | **Test Scenario**                | **Test Steps**                                                                 | **Test Data**         | **Expected Result**                                  | **Status** |
|-------------------|----------------------------------|-------------------------------------------------------------------------------|-----------------------|----------------------------------------------------|------------|
| TC001             | Verify login with valid details | 1. Open login page<br>2. Enter valid username<br>3. Enter valid password<br>4. Click Login | User: admin<br>Pwd: 1234 | User is redirected to dashboard                     | Pass       |
| TC002             | Verify login with invalid pwd   | 1. Open login page<br>2. Enter valid username<br>3. Enter invalid password<br>4. Click Login | User: admin<br>Pwd: 123 | "Invalid password" error message is displayed      | Pass       |
| TC003             | Blank username & password fields | 1. Open login page<br>2. Leave fields blank<br>3. Click Login                   | Blank fields          | "Username and password cannot be blank" is displayed | Pass       |
| TC004             | Password visibility toggle       | 1. Enter password<br>2. Click toggle icon                                    | Pwd: hidden initially | Password becomes visible/unhidden                  | Pass       |

---

#### **Bug Report**  
| **Bug ID** | **Severity** | **Priority** | **Description**                | **Steps to Reproduce**                                                | **Expected Result**                     | **Actual Result**       | **Status** |
|------------|--------------|--------------|--------------------------------|------------------------------------------------------------------------|-----------------------------------------|-------------------------|------------|
| BUG001     | Medium       | High         | Error message overlaps with UI | 1. Open login page<br>2. Enter invalid username/password<br>3. Click Login | Error should appear without UI issues | Error overlaps with buttons | Open       |

---

#### **Requirements Traceability Matrix (RTM)**  
| **Requirement ID** | **Description**                     | **Test Case IDs**       |
|---------------------|-------------------------------------|--------------------------|
| R001               | Login functionality with valid data | TC001                   |
| R002               | Error handling for invalid data     | TC002, TC003, BUG001    |
| R003               | Usability of password visibility    | TC004                   |

---

#### **Test Reports**  
- **Total Test Cases**: 10  
- **Test Cases Executed**: 10  
- **Test Cases Passed**: 9  
- **Defects Raised**: 1  
- **Defects Resolved**: 0  

**Summary**: The login functionality is mostly stable, with one UI-related issue requiring attention.

---

 **Test Metrics**  
| **Metric**                 | **Value** |
|-----------------------------|-----------|
| Test Case Pass Rate         | 90%       |
| Defect Detection Percentage | 10%       |
| Test Execution Time         | 2 hours   |

---


