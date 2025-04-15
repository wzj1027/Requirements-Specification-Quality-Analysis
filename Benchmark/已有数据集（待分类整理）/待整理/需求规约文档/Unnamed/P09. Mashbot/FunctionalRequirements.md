### 3.2 Functional Requirements

#### 3.2.1 User Accounts

- 0140 User Account Types and Permissions The system categorizes users on the basis of roles and
privileges. Within these roles, the system also categorizes users based on the roles that they have
within individual products. These are referred to as user account roles.
    - Mashbot Campaigns supports the following account roles:
        - 0150 Contributor Priority 3
        - 0160 Approver Priority 3
        - 0170 Publisher Priority 3
    - 0180 A user may possess more than one role. Priority 3
    - 0190 Roles reflect actions that can be performed by a user. Priority 3
    - 0200 Roles can be assigned to a user account for individual products. Priority 3
    - 0210 Contributors may create new content, import existing content into the system, edit content,
    and delete it. They may also submit these actions for approval. Priority 3
    - 0220 Approvers can approve actions performed by contributors Priority 3
    - 0230 Publishers may schedule or immediately initiate actions put forth by contributors and those
    approved by approvers. Priority 4
- 0240 User Account Creation - New user accounts can be created. Priority 1
   - 0250 The system may contain any number of user accounts. Priority 1
   - 0260 Certain pieces of information are required to create new accounts. Priority 1
      - The following information is required for any new user account:
      - 0270 Username Priority 1
      - 0280 Password Priority 1
      - 0290 Name Priority 1
      - 0300 Email Address Priority 1
      - 0310 Group Membership Priority 1
      - 0320 User Account Type Priority 1
-  0330 User Account Modification The system allows users to modify their accounts once created. Pri-
   ority 1
   - 0340 The system requires that a user have logged in before modifications can be made. Priority 1
      - The following user account information is modifiable by all user types:
      - 0350 Password Priority 1
      - 0360 Email Address Priority 1
      - 0370 Name Priority 1
- 0380 User Account Deactivation The system allows user accounts to be deactivated. Priority 3
   - 0390 The system denies user who have been deactivated from accessing the system. Priority 3
      - 0400 If an account has any history associated with it, it can only be deactivated and not deleted.
        Priority 3
   - 0410 If an account has no history associated with it, it can be deleted from the system. Priority 3
   - 0420 A disable account can be undisabled Priority 3
   - 0430 It is possible to disable all accounts except for the System Administrator account. Priority 4
- 0440 Username and Passwords
   - 0450 The system gives users the ability to reset their password. Priority 2
   - 0460 Individual passwords can be reset. Priority 2
   - 0470 The system only allows users to change their own passwords. Priority 2

#### 3.2.2 Marketing Campaigns

- 0480 A campaign has the following components:
   - 0490 Name Priority 1
   - 0500 Pieces of content Priority 1
   - 0510 Schedule Priority 1
   - 0520 User/Group Permissions Priority 2
- 0530 A schedule is a mapping of times to publishing actions. It may contain any actions a publisher can
perform, and these actions are performed at the associated time. Priority 1
- 0540 A piece of content may take the following forms:
    - 0550 Text Priority 1
    - 0560 Image Priority 1
    - 0570 Audio Priority 3
    - 0580 Video Priority 3

#### 3.2.3 External Service Accounts

- 0590 Mashbot will allow for the association of Mashbot accounts with external service accounts.
- 0600 Mashbot will provide an interface for authenticating a user account to an external service account
Priority 1
- 0610 Mashbot will provide a standardized method of interacting with external service accounts Priority 1