# Functional Requirements Specification: BLIT102

- Version: Draft


## Table of Contents

- Approval Log 
- Revision History
- Project Team
1. Introduction
    1. Purpose
    2. Scope
2. Specific Requirements
    1. Functionality
        1. Module: Admin
    2. Usability
        1. User Interface Guidelines
    3. Reliability
        1. System Downtime
    4. Performance
        1. Quality Assurance
    5. Supportability
        1. Coding Standards
        2. Maintainability Standards
    6. Design Constraints
        1. Development Platform
        2. Production Releases
        3. Development Process
    7. Online User Documentation and Help System Requirements
        1. Robohelp Tool: RoboHelp version 8 will be used to create the online [system
           name] Help hypertext links. The [system name] system will display a hypertext link
           labeled “Help” at the top right corner on each of the user screens to provide assistance
           to the user. Each of the Help topic pop-up windows will contain that same content that
           is available within the [system name] user’s manuals.
    8. Interfaces
    9. Applicable Standards
        1. HIPAA Compliance
3. Glossary


## Approval Log

| Print Name | Role | Date | Signature |
| --- | --- | --- | --- |


## Revision History

| Date | Version | Author | Description |
| --- | --- | --- | --- |
| 06/02/08 | Draft | NHarris | Document Created - Initial Revision |
| 08/11/08 | Draft | NHarris | Added [employee name] to the project team |
| 08/11/08 | Draft | NHarris | Updated with functional requirements based on use cases. |
| 08/15/08 | Draft | NHarris | Updated with functional requirements based on the approved use cases. |
| 08/18/08 | Draft | NHarris | Updated with functional requirements based on the approved use cases for iterations 1 and 2. |


## Project Team

| Name | Title/Role | Department/Team | Phone | E-mail |
| xxx | CIO and Business/Technical Owner/Final Approver | IT | xxx | xxx@xxx.com |
| xxx | Manager | IT – QA/QC & Implementation | xxx | xxx@xxx.com |
| xxx | Programmer Analyst/Project Manager | IT - Development | xxx | xxx@xxx.com |
| xxx | Programmer Analyst/SME | IT - Development | xxx | xxx@xxx.com |
| xxx | Programmer Analyst/SME | IT - Development | xxx | xxx@xxx.com |
| xxx | Technical Writer IT – QA/QC & Implementation | xxx | xxx@xxx.com |
| xxx | Sr. Business Systems Analyst | IT – QA/QC & Implementation | xxx | xxx@xxx.com |
| xxx | QA Analyst | IT – QA/QC & Implementation | xxx | xxx@xxx.com |
| xxx | Technical Writer | IT – QA/QC & Implementation | xxx | xxx@xxx.com |


## 1 Introduction

The management of [company name]. has identified a potential need for re-writing its core
Laboratory Information System (LIS) to improve the performance. In general, this project
will provide a stable environment, automate decisions, streamline workflows, and employ
industry standard coding and documentation practices. This effort will ensure System
Integrity/Reliability by developing a system that is reliable and low maintenance including
security and confidentiality requirements as dictated by HIPAA and FDA regulatory
standards.

### 1.1 Purpose
This Functional Requirements Specification (FRS) is intended to capture the changes in
functionality that will occur during [system name] Re-Writing effort, which is part of the xxx
Enhancements project. All functionalities for the new [system name] system would be
documented in this FRS. Any undocumented requirements will be considered out of scope
and will not be implemented during this phase of Re-Writing.

### 1.2 Scope
The existing functionalities in the core [system name] will remain same. This project is
limited in scope to the enhancements and defects that are critical in the severity level that is
the issues that cause great burden to the system users and the enhancements in system
architecture, which will facilitate efficient growth of [system name] and the [company name]
business, will fall under the purview of this project scope.

The functional issues and requirements that will be discussed and gathered respectively as
well as validated in the Requirements Gathering and Validating Sessions started on
MM/DD/YYYYwould be documented in this FRS moving forward. The project team has
decided that system development will occur on module by module basis.


## 2 Specific Requirements

### 2.1 Functionality

#### 2.1.1 Module: Admin
1. **Use Case: xxx Page, UC ID: UC_RR_xxx_xxx__000**
    1. System shall display the hyperlinks and descriptions for the user to perform the desired
functions as specified in the related UIS.
    2. The User shall be able to view the hyperlinks and descriptions listed.
    3. The User shall be able to choose a function by clicking the hyperlink.
    4. The system shall display the desired operational page for the user after clicking the
hyperlink.
2. **Use Case: xxx Page, UC ID: UC_RR_xxx_xxx__000**
    1. **Action: Create/Add User**
        1. A user with admin privileges shall be able to Add/Create a new user and associate the
user with specified role(s) in the system.
        2. The system shall display an error message if the new user is found in the [system name]
system.
        3. The system shall display an error message if the new user is not active in the Active
Directory.
        4. The system shall display the xxx tab as the default tab.
        5. The user shall be able to create/add a new user manually or from a template.
        6. The user record shall inherit all specified role(s) settings in the template when the user
record is created from the user template
        7. The user shall be able to add additional roles manually while creating/adding a new user
from a user template.
        8. The system shall save the user info to the database with specified roles associated with
divisions for the newly created/added user.
        9. The system shall perform a search on the [system name] user display name and user
name columns in the user tables to find the user and verify the user’s existence.
        10. The system shall perform a search in the Active Directory to verify the status of the user
— Active/Inactive within the company—when the user attempts to create/add a new userin the [system name] system.
        11. The system shall generate a standard confirmation message after saving data andwarning/caution messages after the cancel or close button is clicked.
        12. The user must have the flexibility to click any tab to commence the adding process,although the xxx Tab shall display as the default tab.
        13. All required fields as specified in the UIS must be marked with a red asterisk alerting theuser to fill the required fields in.
        14. The user shall be able to save data after creating/adding a new user or cancel data toabort the process.
        15. The system shall clear up data if the user chooses to click the Cancel button in the midstof creating/adding a new user.
        16. The system shall direct the user to the xxx Page if the user chooses to click the closebutton without entering any data.
        17. The user must associate at least one role, division, designator code, and lab location atthe time of creating/adding a new user.
        18. The user must fill in the required fields—User Name and Display Name—in the UserInformation section at the time of creating/adding a new user.
        19. The system shall generate a standard error/warning message after the user attempts tosave data without associating one of each of the following criteria—xxx—and/or without
filling in the required fields in the User Information section.

### 2.2 Usability

#### 2.2.1 User Interface Guidelines
1. The Project Team must demonstrate mockups of UI changes to project stakeholders earlyin the development process.
2. The Project Team must permit reasonable adjustment to the user interfaces of newfunctionality by project stakeholders when project schedule permits those adjustments.

### 2.3 Reliability

#### 2.3.1 System Downtime
1. The Project Team shall schedule updates to the production environment only on Tuesdays
between 7pm and 7am. (Example)

### 2.4 Performance

#### 2.4.1 Quality Assurance
1. The Project Team must perform applicable and appropriate testing against new functionality
prior to releasing that functionality/build to the production environment.
2. The project Team must allow a reasonable time to conduct User Acceptance Testing (UAT)
against the built functionalities prior to deploying the product to the production environment.

### 2.5 Supportability

#### 2.5.1 Coding Standards
1. The Development Team shall define coding standards for the application and follow those
standards consistently.
2. The Development Team shall be required to adjust existing source code to follow accepted
coding standards only if that source code must be modified.

#### 2.5.2 Maintainability Standards
1. The system shall log errors, warnings, and informational messages to an external log file onthe application server.
2. The Development Team shall be required to adjust existing source code to use the externallog file only if that source code must be modified to implement another requirement.
3. The system shall log an error message to the external data file when the user is directed tothe [SYSTEM NAME] error page.
4. The system shall send a notification email to a Client Services email distribution list if theuser is directed to the xxx error page.

### 2.6 Design Constraints

#### 2.6.1 Development Platform
1. The Development Team shall develop functionalities using the xx language and on the
supported .NET 3.5 Platform.
2. The Development Team shall utilize established open source frameworks instead of
proprietary custom components wherever appropriate.
3. The system shall continue to depend upon and use a single SQL Server 2008 database.

#### 2.6.2 Production Releases
1. The Technical Owner/Lead shall provide signoff before any [SYSTEM NAME] build can be
deployed to the production environment.

#### 2.6.3 Development Process
1. The Development Team shall perform weekly integrations of the [SYSTEM NAME] systemand deploy these system updates to the Staging environment.
2. The Development Team shall label every scheduled [SYSTEM NAME] build in the sourcecontrol system.
3. The Development Team shall perform scheduled [SYSTEM NAME] builds using codechecked out of source control using the label as defined and specified.
4. The Development Team shall develop and then send out release notes via e-mail to allProject Team after each [SYSTEM NAME] build deployed to the Staging environment.
5. The Technical Lead shall perform code reviews of every system change before thosechanges may be committed to source control.
6. The QA/QC Team must perform regression testing against all scheduled builds.

### 2.7 Online User Documentation and Help System Requirements

1. **Robohelp Tool: Help hypertext links. The [system name] system will display a hypertext link labeledRoboHelp version 8 will be used to create the online [system name]
“Help” at the top right corner on each of the user screens to provide assistance to theuser. Each of the Help topic pop-up windows will contain that same content that is
available within the [system name] user’s manuals.**
    1. The system shall provide the capability to open a pop-up window displaying information
about the specific page along with links to supporting help topics upon selecting each Helplink.
    2. The system shall display “[system name] Overview” page located under the Getting Startedsection of Help as default help topic page that will load upon selecting Help hypertext link.
    3. The system must allow users to easily navigate through each of the help topics by selectinga corresponding hypertext link provided in the left frame of the pop-up Help window.
    4. The system shall display the [company name] logo in the top, right side of the screen oneach of the help pages.
    5. The system must exhibit each of the help pages using the same color scheme andbackground as specified.
    6. The system shall provide searching ability to the users to quickly find specific topic materialthrough the online help tool.
    7. The system shall provide an index to the users for a more in-depth search of topic contentsthrough the online help tool.
    8. The system shall provide a Glossary for industry-related terms associated with [companyname] and the [system name] system to the users through the online help tool.

### 2.8 Interfaces

#### 2.9 Applicable Standards
1. **HIPAA Compliance**
    1. The system shall retain existing HIPAA compliance capabilities.
    2. The system shall follow HIPAA compliance capabilities in new functionality introduced to the
system.


## 3 Glossary