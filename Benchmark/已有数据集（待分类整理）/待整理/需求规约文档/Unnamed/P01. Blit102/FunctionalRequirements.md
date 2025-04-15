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