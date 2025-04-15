# Construction Junction: Inventory Management: Software Requirements Specification

Version 2.0

## Summa Technologies

October 1st, 200 9
Summa Technologies, Inc.
925 Liberty Avenue 6th Floor
Pittsburgh, PA 15222
(412) 258- 3300

## Table of Contents

- REVISION HISTORY
- APPROVALS
- REQUIREMENTS ANALYSIS TEAM
- 1. INTRODUCTION
   - 1.1. PURPOSE
   - 1.2. SCOPE
   - 1.3. AUDIENCE
   - 1.4. DEFINITIONS AND ACRONYMS
- 2. OVERVIEW
   - 2.1. ACTORS
- 3. DETAILED FUNCTIONAL REQUIREMENTS
   - 3.1. VIEW INVENTORY
   - 3.2. MANAGE DEPARTMENTS
   - 3.3. MANAGE CATEGORIES
   - 3.4. MANAGE ATTRIBUTES AND DETAILS
   - 3.5. ADD ITEM TO INVENTORY
   - 3.6. MANAGE INVENTORY ITEMS
   - 3.7. SUGGEST ITEM PRICE
   - 3.8. VIEW ACQUISITIONS
   - 3.9. RECEIVE ACQUISITION
   - 3.10. SELL ITEM
   - 3.11. REPORTS
- 4. HIGH-LEVEL FUNCTIONAL REQUIREMENTS
   - 4.1. MEDIUM PRIORITY
   - 4.2. LOW PRIORITY
- 5. SUPPLEMENTARY REQUIREMENTS
   - 5.1. USABILITY
   - 5.2. AVAILABILITY
   - 5.3. RELIABILITY
   - 5.4. SECURITY
   - 5.5. PERFORMANCE
   - 5.6. INTERFACES
   - 5.7. CLIENT PLATFORM
   - 5.8. DATA MIGRATION
   - 5.9. DISASTER RECOVERY, BACKUPS, AND BUSINESS CONTINUITY PLAN
   - 5.10. MAINTAINABILITY
   - 5.11. PORTABILITY
   - 5.12. LEGAL, COPYRIGHT AND OTHER NOTICES
   - 5.13. LICENSING
   - 5.14. APPLICABLE STANDARDS
- APPENDIX A: REFERENCES
- APPENDIX B: GLOSSARY

## REVISION HISTORY

| Date | Version | Description | Author |
| --- | --- | --- | --- |
| October 1st, 2009 | 1.0 | Initial draft | Adriano Wisnik |
| November 9th, 2009 | 1.1 | Changes from review by Mindy | Adriano Wisnik |
| March 7, 2011 | 2.0 | Final draft completed by Mindy | Mindy Schwartz |

## APPROVALS

| Name | Department | Version | Date | Approval | Method |
| --- | --- | --- | --- | --- | --- |

## REQUIREMENTS ANALYSIS TEAM

| Role | Name | Department |
| Business Unit Representative | Mindy Schwartz | Operations |
| Business Analyst | Adriano Wisnik | Summa Technologies, Inc.

## 1. INTRODUCTION

### 1.1. PURPOSE

The purpose of this document is to define the requirements of the Inventory Management System as
proposed by the Construction Junction (CJ) staff.

### 1.2. SCOPE

The scope of the Inventory Management project and subsequently the requirements defined by this
document is the creation of a categorized Inventory Management System that provides the functionality
identified by the Construction Junction team. Requirements defined in this document are prioritized by
business and technical sponsors (Please refer to Appendix A). All implementation will be based on project
planning estimates and revisions to these requirements.

### 1.3. AUDIENCE

This document is intended for the Construction Junction team, individual developers, and the system
architect.

### 1.4. DEFINITIONS AND ACRONYMS

Please see Appendix B for a list of terms and abbreviations that are used throughout this document.

## 2. OVERVIEW

The Inventory Management System is an application designed to allow the Construction Junction staff to
create, maintain and view the contents and value of its inventory of items in a categorized way. It also
facilitates the process of receiving items into the Construction Junction inventory via the drop-off, pick-up
and deconstruction donation processes so that items can be traced from donation through sale. It also
integrates with the QuickBooks Point of Sale retail management software currently in use by Construction
Junction as well as the organization‟s website.

### 2.1. ACTORS

Actors are people, hardware, systems, or other entities external to the system that interact with the
system. This section contains a description of each actor that interfaces with the system:

- Administrator: A member of the Construction Junction staff who can perform any of the Inventory
Management functions.
- Director: A member of the Construction Junction staff who can perform the same Inventory
Management functions as a Manager, plus view, create, modify and delete Inventory Management
users.
- Manager: A member of the Construction Junction staff who can perform the same Inventory
Management functions as a Receiving Associate, plus change item properties.
- Receiving Associate: A member of the Construction Junction staff who receives donated items at
the receiving docks and performs their initial entry into the Inventory Management System and
provides donors with their donation receipts.
- Customer Service Representative: A member of the Construction Junction staff who works in the
customer service desk and performs specific tasks such as constituent and member database
management, item returns processing, creating drop-off acquisitions, and others.
- Pickup Associate: A member of the Construction Junction staff who picks up donated items and
brings them for processing at the receiving dock.
- Decon Associate: A member of the Construction Junction staff who executes a deconstruction
and/or strip out job and brings the items for processing at the receiving dock.
- Sales Associate: A member of the Construction Junction staff who processes purchases by
Construction Junction customers.
- Construction Junction Staff Member: Any of the Construction Junction user types: Administrator,
Director, Manager, Receiving Associate, Pickup Associate, Decon Associate, Customer Service
Representative or Sales Associate.
- Donor: An individual or organization who donates items to the Construction Junction inventory and
receives a tax deduction for doing so.
- Buyer: A customer who purchases items from the Construction Junction inventory.
- Primary Contact: An individual who is the primary contact for a donation. The individual may be the
actual donor or be acting on behalf of one.
- Vendor: An individual or organization who sells items to be added to Construction Junction‟s
inventory
- Consigner: An individual who donates items to Construction Junction under consignment.


## 3. DETAILED FUNCTIONAL REQUIREMENTS

This section contains detailed reports for each product-functional use cases. Each report contains the
following data or sections (if a section has no content for a use case, it has been removed):
- Name of the use case
- High-level description
- Actor(s): All actors who interact with the system during the course of the use case.
- Pre-conditions: Pre-conditions are conditions that must be true prior to beginning the use case and
are assumed to be true throughout the use case.
- Triggers: Events and precursors that cause this use case to initiate.
- Use Case Dependencies: Other use cases which this use case depends on.
- Basic Flows: The flows for the standard, expected execution of the use case. This section provides
few details, but should be sufficient for a project manager or business representative to understand
the use case.
- Alternative Flows: Exceptional flows and how the system handles them.
- Business Rules: All of the detailed validation, logic, and other rules that govern the use case.
- Post-conditions: Any states the system could possibly be in when the use case terminates.
- Special Requirements: Any security, auditing, interface or other special requirements.
- Open Issues: Any issues that have yet to be resolved relating to the use case.
- Extension Points: Requirements or features that are beyond the scope of this release, but may be
included in later releases and subsequently should be kept in mind during design and
implementation.
- Activity Diagram: Visual representation of a complicated flow.
- Notes: Any ancillary details of importance that do not otherwise fit one of the above sections.

### 3.1. VIEW INVENTORY

The system should provide a categorized view of the entire inventory to the Construction Junction staff.
Starting at the department level, users can navigate into the inventory item categories and sub-
categories, all the way down to an individual inventory item.

#### 3.1.1. Actor(s):

- Administrator
- Director
- Manager
- Customer Service Representative
- Receiving Associate
- Pick Up Associate
- Decon Associate

#### 3.1.2. Assumptions, Pre-Conditions & Triggers:

1. User is logged into the system

#### 3.1.3. Use Case Dependencies

None

#### 3.1.4. Basic Flows:

1. User accesses the main inventory screen
2. The screen displays all inventory departments
3. User clicks a department cell
4. The screen displays all inventory categories for the selected department
5. User clicks a category cell that contains sub-categories
6. The screen displays all inventory sub-categories for the selected category
7. User clicks a sub-category cell (leaf category)
    1. For a Unique Item category:
        1. The screen displays a list of all inventory items for that selected category
        2. User clicks an item in the items list
        3. The screen displays the details for the item
    2. For a Stock Item category:
        1. The screen displays the details for that Stock Item category
    3. For a Under $5 category:
        1. Nothing happens – The category cell is not clickable

#### 3.1.5. Alternative Flows:

1. At any point, the user may click on a department on the inventory department shortcuts list, which
    takes the user to the inventory view for that particular department.
2. The user may click the View All Items button at any level in the inventory to view a list of all items in
    that department or category
3. The user may click the View All Items button on the main inventory screen to view the complete list of
    all items in the inventory
4. Once in the view items list screen, the user may filter the results by searching for:
    1. A particular item by item number
    2. All items with Donor, Department, Category or Description matching the provided keyword
    3. All items with certain attributes, features and/or details

#### 3.1.6. Business Rules:

1. Inventory departments and categories are displayed in matrix format
2. The matrix dimensions are fixed, and are the same when displaying departments or categories.
3. Unused matrix cells are displayed empty.
4. The actual matrix dimensions are to be determined during system implementation.
    1. The matrix should be able to hold at least 30 tiles at each level
5. Each matrix cell displays a department or category name.
    1. For departments with subcategories, the department name is a hyperlink to the view of the
       department subcategories
    2. For a department with no subcategories, the department name is a hyperlink to the view of the
       items in that department
    3. For categories with subcategories, the category name is a hyperlink to the view of the
       subcategories
    4. For a category with no subcategories
        1. For a Unique Item category, the category name is a hyperlink to a view of the items under
          that category
        2. For a Stock Item category, the category name is a hyperlink to a view of the details for that
          Stock Item, including the current quantity on hand
        3. For a Under $5 category:
            1. The category name is not a hyperlink
6. By default, the items list contains the list of all Unique and Stock items in the selected department or
    category, or across all departments and categories when viewing the all inventory items screen
7. When a search keyword is specified, the system filters the default items list for that screen and
    returns only the items for which the keyword matches one or more of the following columns:
    1. Donor
    2. Department
    3. Category
    4. Description
8. When user clicks on an item in the items list for a category or department, the system displays the
    item details screen
9. Departments and categories are listed in alphabetical order in each row, from left to right and top to
    bottom
10. The cell in the top left corner of the matrix always represents a generic item in the selected
    department (e.g. a generic appliance when viewing the categories in the appliance department) and
    is automatically generated by the system
11. The cell to the right of the top left corner of the matrix always represents under $5 items in the
    selected department and is automatically generated by the system

#### 3.1.7. Post-Condition(s):

None

#### 3.1.8. Open Issues:

None

#### 3.1.9. Extension Points:

None

#### 3.1.10. Activity Diagram(s):

None

#### 3.1.11. Notes:

See the View Inventory user interface requirements.

### 3.2. MANAGE DEPARTMENTS

The system should allow inventory administrators to customize the inventory structure by defining the
inventory departments (not to be confused actual retail floor departments known later in this document as
stocking locations).

#### 3.2.1. Actor(s):

- Administrator

#### 3.2.2. Assumptions, Pre-Conditions & Triggers:

1. User is logged into the system

#### 3.2.3. Use Case Dependencies

1. View Inventory

#### 3.2.4. Basic Flows:

1. Add Department
    1. User accesses the main inventory screen
    2. System displays the Add Department button
    3. User clicks the Add Department button
    4. User enters the Department data
    5. System validates the Department data
    6. System adds the new Department to the inventory
    7. User is taken back to the main inventory screen
2. Edit Department
    1. User navigates to a Department (see View Inventory)
    2. System displays the Edit Department button
    3. User clicks the Edit Department button
    4. System displays the Department data
    5. User edits Department data
    6. System validates the Department data
    7. System updates the Department information
    8. User is taken back to the Department screen
3. Delete Department
    1. User navigates to a Department (see View Inventory)
    2. System displays the Edit Department button
    3. User clicks the Edit Department button
    4. System displays the Department data
    5. User clicks the Delete Department button
    6. System validates the Department deletion
    7. System removes the Department from the inventory
    8. User is taken back to the main inventory screen

#### 3.2.5. Alternative Flows:

1. Add Department
    1. User cancels the Department add and is taken back to the main inventory screen
    2. During data validation, data is deemed invalid and an error message is presented to the user
2. Edit Department
    1. User cancels the Department edit and is taken back to the main inventory screen
    2. During data validation, data is deemed invalid and an error message is presented to the user
3. Delete Department
    1. User cancels the Department deletion and is taken back to the Department screen
    2. During deletion validation, deletion is deemed invalid and an error message is presented to the
       user

#### 3.2.6. Business Rules:

1. Add Department
    1. The following fields are mandatory:
        1. Name
        2. POS Department Code
        3. Unique Tag
    2. The Department Name must be unique across the inventory
    3. The Department‟s Unique Tag must be unique across the inventory
    4. The POS Department Code must be at most 3 characters long
    5. The Unique Tag must be at most 18 characters long
    6. There must be at least one slot available in the Department matrix to hold the new Department
2. Edit Department
    1. The following fields are mandatory:
        1. Name
        2. Unique Tag
    2. The Department Name must be unique across the inventory
    3. The Department‟s Unique Tag must be unique across the inventory
    4. The Unique Tag must be at most 18 characters long
3. Delete Department
    3.1. A Department cannot be deleted if it contains categories and/or items
    3.2. The system must ask for confirmation before deleting a Department

#### 3.2.7. Post-Condition(s):

1. Add Department
    1.1. The new Department is added
2. Edit Department
    2.1. The Department is updated
3. Delete Department
    3.1. The Department is deleted

#### 3.2.8. Open Issues:

None

#### 3.2.9. Extension Points:

None

#### 3.2.10. Activity Diagram(s):

None

#### 3.2.11. Notes:

See the Manage Departments user interface requirements.

### 3.3. MANAGE CATEGORIES

The system should allow inventory administrators to customize the inventory structure by defining the
inventory departments and categories.

#### 3.3.1. Actor(s):

- Administrator

#### 3.3.2. Assumptions, Pre-Conditions & Triggers:

1. User is logged into the system

#### 3.3.3. Use Case Dependencies

1. View Inventory
2. Manage Attributes and Details

#### 3.3.4. Basic Flows:

1. Add Category
    1. User navigates to a Department or Category (see View Inventory)
    2. System displays the Add Category buttons
        1. Unique Item
        2. Stock Item
    3. User clicks the desired Add Category button
    4. System displays the appropriate screen for the Category type
        1. Unique Item
        2. Stock Item
    5. User enters Category data
    6. System validates the Category data
    7. System adds the new Category to the inventory
    8. User is taken back to the parent Department or Category of the added Category
2. Edit Category
    1. User navigates to a Category (see View Inventory)
    2. System displays the Edit Category button
    3. User clicks the Edit Category button
    4. System displays the appropriate screen for the Category type
       1. Unique Item
       2. Stock Item
    5. User edits Category data
    6. System validates the Category data
    7. System updates the Category information
    8. User is taken back to the Category screen
3. Delete Category
    1. User navigates to a Category (see View Inventory)
    2. System displays the Edit Category button
    3. User clicks the Edit Category button
    4. System displays the appropriate screen for the Category type
        1. Unique Item
        2. Stock Item
    5. User clicks the Delete Category button
    6. System validates the Category deletion
    7. System removes the Category from the inventory
    8. User is taken back to the parent Department or Category of the deleted Category
4. Move Categories
    1. User navigates to a Department or Category (see View Inventory)
    2. System displays the Move Categories button
    3. User clicks the Move Categories button
    4. System displays the Move Categories screen
    5. User selects Categories to move
    6. User selects target location on categorized inventory for the moved Categories
        1. User may select an existing Department or Category
        2. User may choose to create a new Category to hold the moved Categories
            1. In this case, user selects the parent Department or Category of the new Category
             to be created
            2. User enters the new Category data
    7. User selects the type of move to be performed
        1. Move selected categories as-is and make them children of the target Department or
           Category
        2. Merge the contents (items) of the selected categories and add them to the target
           Department or Category
    8. System validates the entered data
    9. System moves the selected Categories
    10. User is taken back to the parent Department or Category of the moved Categories

#### 3.3.5. Alternative Flows:

1. Add Category
    1. User cancels the Category add and is taken back to parent Department or Category
    2. During data validation, data is deemed invalid and an error message is presented to the user
2. Edit Category
    1. User cancels the Category edit and is taken back to Category screen
    2. During data validation, data is deemed invalid and an error message is presented to the user
3. Delete Category
    1. User cancels the Category deletion and is taken back to the Category screen
    2. During deletion validation, deletion is deemed invalid and an error message is presented to the
       user
4. Move Categories
    1. User cancels the Category move and is taken back to the parent Department or Category screen
    2. During move validation, move is deemed invalid and an error message is presented to the user

#### 3.3.6. Business Rules:

1. Add Category
    1. The following fields are mandatory:
        1. Unique Item Category
            1. Name
            2. Unique Tag
        2. Stock Item Category
            1. Name
            2. Unique Tag
            3. Price
    2. The Category Name must be unique across the inventory
    3. The Category‟s Unique Tag must be unique across the inventory
    4. The Unique Tag must be at most 18 characters long
    5. There must be at least one slot available in the Category matrix at the level the new Category will
       be created to hold the new Category
    6. The available options in the Material, Finish, Color and Features selectors should be the ones
       defined for the selected department (see Manage Attributes and Details)
    7. The fields and available options under the Details section should be the ones defined for the
       selected category (see Manage Attributes and Details)
    8. When a Stock Item Category is created, a corresponding item is added to QuickBooks POS
        1. The ID of the item in POS is set to the Category‟s Unique Tag
        2. The initial item quantity in POS is set to zero
2. Edit Category
    1. The following fields are mandatory:
        1. Unique Item Category
            1. Name
            2. Unique Tag
        2. Stock Item Category
            1. Name
            2. Unique Tag
            3. Price
    2. The Category Name must be unique across the inventory
    3. The Category‟s Unique Tag must be unique across the inventory
    4. The Unique Tag must be at most 18 characters long
    5. The available options in the Material, Finish, Color and Features selectors should be the ones
       defined for the selected department (see Manage Attributes and Details)
    6. The fields and available options under the Details section should be the ones defined for the
       selected category (see Manage Attributes and Details)
    7. When a Stock Item Category is updated, the corresponding item is updated in QuickBooks POS
        1. The ID of the item in POS is set to the Category‟s Unique Tag
        2. The initial item quantity in POS is set to zero
    8. Generic categories and Under $5 item categories are generated automatically by the system and
       cannot be modified
3. Delete Category
    1. When a Category is deleted, all of its items should be moved to the parent category
    2. The system must ask for confirmation before deleting a Category
    3. Generic item categories and Under $5 item categories are generated automatically by the system
       and cannot be deleted
4. Move Categories
    1. The Categories to Move selector is populated with the categories seen on the matrix at the level
       where the Move Categories button was pressed.
    2. User must select at least one Category to move
    3. User must select either an existing or new target Department or Category
    4. User cannot move categories to any Departments or Categories that don‟t have enough slots
       available in the matrix to hold the moved categories
    5. User cannot move categories to any of their subcategories (cannot create loops in the inventory
       hierarchy)
    6. If a new target Category is selected
        1. User must enter
            1. Name
            2. Unique Tag
            3. Parent Department or Category of the new Category
        2. The Category is created as a Unique Item Category
    7. User cannot select a Stock Item, Under $5 Category or Generic Category as the target Category
    8. When a Category is moved it keeps its assigned Item Details
    9. When the option to merge the contents of the selected Categories is selected, the Item Details
       assigned to the selected Categories are combined and assigned to the target Department or
       Category
    10. When the option to merge the contents of the selected Categories is selected, the moved
        items must be updated in QuickBooks POS

#### 3.3.7. Post-Condition(s):

1. Add Category
    1. The new Category is added
2. Edit Category
    1. The Category is updated
3. Delete Category
    1. The Category is deleted
4. Move Categories
    1. If the „move to a new Category‟ option is selected, a new Category is created
    2. If the „move categories and make them children‟ option is selected, the selected Categories are
       moved to the selected target location
    3. If the „merge contents of selected categories‟ option is selected, the contents of the selected
       Categories are moved to the selected target location

#### 3.3.8. Open Issues:

None

#### 3.3.9. Extension Points:

None

#### 3.3.10. Activity Diagram(s):

None

#### 3.3.11. Notes:

See the Manage Categories user interface requirements.

### 3.4. MANAGE ATTRIBUTES AND DETAILS

The system should allow inventory administrators to customize the attributes and details available for
each inventory item. Attributes can be defined for each department, and details can be defined for each
department and/or category

#### 3.4.1. Actor(s):

- Administrator

#### 3.4.2. Assumptions, Pre-Conditions & Triggers:

1. User is logged into the system

#### 3.4.3. Use Case Dependencies

1. View Inventory

#### 3.4.4. Basic Flows:

1. View Item Attributes
    1. User accesses the main inventory screen
    2. System displays the Edit Attributes button
    3. User clicks the Edit Attributes button
    4. System displays the Edit Attributes screen which displays all existing item attributes and their
       attribute x department assignments
    5. Optionally, user filters view by attribute status (active, inactive, all)
    6. User clicks the Done button
    7. User is taken back to the main inventory screen
2. View Item Details
    1. User accesses the main inventory screen
    2. System displays the Edit Details button
    3. User clicks the Edit Details button
    4. System displays the Edit Details screen which displays all existing item details and their detail x
       department and category assignments
    5. Optionally, user filters view by detail status (active, inactive, all)
    6. User clicks the Done button
    7. User is taken back to the main inventory screen
3. Edit Item Attributes
    1. User accesses the main inventory screen
    2. System displays the Edit Attributes button
    3. User clicks the Edit Attributes button
    4. System displays the Edit Attributes screen which displays all existing item attributes and their
       attribute x department assignments
    5. Optionally, user filters view by attribute status (active, inactive, all)
    6. User edits attributes
        1. User changes attribute x department assignments
        2. User changes attribute data
        3. User changes attribute active x inactive status
        4. User creates new attribute
        5. System validates the attribute data
        6. System updates the Item Attribute information
    7. User clicks the Done button
    8. User is taken back to the main inventory screen
4. Edit Item Details
    1. User accesses the main inventory screen
    2. System displays the Edit Details button
    3. User clicks the Edit Details button
    4. System displays the Edit Details screen which displays all existing item details and their detail x
       department and category assignments
    5. Optionally, user filters view by detail status (active, inactive, all)
    6. User edits details
        1. User changes detail x department or category assignments
        2. User changes detail data
        3. User changes detail active x inactive status
        4. User creates new detail
        5. System validates the detail data
        6. System updates the Item detail information
    7. User clicks the Done button
    8. User is taken back to the main inventory screen

#### 3.4.5. Alternative Flows:

1. View Item Attributes
    None
2. View Item Details
    None
3. Edit Item Attributes
    1. User cancels the Item Attribute edit and is taken back to the main inventory screen
    2. During data validation, data is deemed invalid and an error message is presented to the user
4. Edit Item Details
    1. User cancels the Item Detail edit and is taken back to the main inventory screen
    2. During data validation, data is deemed invalid and an error message is presented to the user

#### 3.4.6. Business Rules:

1. View Item Attributes
    None
2. View Item Details
    None
3. Edit Item Attributes
    1. The following fields are mandatory:
        1. Name
    2. The Item Attribute Name must be unique across the inventory
    3. The De-Activate Attribute button is replaced with an Activate Attribute button when the attribute is
       inactive
    4. Material and Features attributes can be assigned to any combination of departments
    5. Material and Features attributes can be assigned to „All‟ departments
    6. Color and Finish attributes can only be set to „All‟ departments
    7. An Attribute cannot be set simultaneously to „All‟ departments and to specific department(s)
        1. Assigning an attribute to „All‟ departments disables the individual department selectors, but
           preserves the current department selections
        2. Un-assigning an attribute from the „All‟ departments enables the individual department
           selectors, restoring the previous department selections
4. Edit Item Details
    1. The available detail types are:
        1. Number
        2. Text
        3. Selection
    2. The following fields are mandatory:
        1. Name
        2. Type
    3. If the Type is set to „Selection‟, then the selection list must contain at least one item
    4. The Item Detail Name must be unique across the inventory
    5. The De-Activate Detail button is replaced with an Activate Detail button when the detail is inactive
    6. Details can be assigned to any combination of departments and categories
    7. Details can be assigned to „All‟ departments and/or categories
    8. Assigning a detail to a department or category automatically assigns it to its subcategories
        1. Assignments automatically made by the system can be changed by the user

#### 3.4.7. Post-Condition(s):

1. View Item Attributes
    None
2. View Item Details
    None
3. Edit Item Attributes
    1. The Item Attributes are updated
4. Edit Item Details
    1. The Item Details are updated

#### 3.4.8. Open Issues:

None

#### 3.4.9. Extension Points:

None

#### 3.4.10. Activity Diagram(s):

None

#### 3.4.11. Notes:

See the Manage Attributes and Details user interface requirements.

### 3.5. ADD ITEM TO INVENTORY

Items are typically added to the inventory as part of the donation processes. This is called adding an item
in donation processing. Alternatively, items can be added during routine inventory maintenance. This is
called adding an item in inventory management mode.

#### 3.5.1. Actor(s):

- Administrator
- Director
- Manager
- Receiving Associate
- Pickup Associate
- Decon Associate
- Customer Service Representative

#### 3.5.2. Assumptions, Pre-Conditions & Triggers:

1. User is logged into the system

#### 3.5.3. Use Case Dependencies

1. View Inventory
2. Suggest Item Price
3. Manage Attributes and Details
4. Receive Acquisition

#### 3.5.4. Basic Flows:

1. User accesses the main inventory screen
5. The screen displays all inventory departments in matrix format (see View Inventory)
2. User drills down to the appropriate category for the item
    1. If in donation processing mode, the item entry screen is presented automatically
    2. If in inventory management mode, the list of existing inventory items in that category is displayed
        1. User clicks the Add Item button
3. The appropriate item entry screen is presented
4. User fills in item information
5. User confirms the addition of the new item
6. Inventory is updated
7. System gives the option of printing an item tag
8. User prints item tag(s)s for unique or stock item(s)
9. User attaches tag(s) to the item(s)

#### 3.5.5. Alternative Flows:

1. At any point, the user may click on a department on the inventory department shortcuts list, which
   takes the user to the inventory view for that particular department.
2. At any point while in the item add screen, the user may cancel the operation.

#### 3.5.6. Business Rules:

1. When navigating to the desired item category, departments and categories are displayed according to
   the rules defined in View Inventory
2. Items can be added at any level in the categorized inventory
3. Only unique and stock items are tracked by the inventory system
    1. Only unique and stock items are available to be added in inventory management mode
    2. Under $5 items can only be added in donation processing mode
        1. Information about Under $5 items is only added for the purpose of generating the donation
           receipt
4. When an item is added to the inventory, the system updates QuickBooks POS accordingly and
   promptly
    1. A new item entry is created in POS for a unique item
    2. The item category name in POS is set to XXXXXXXXXXXXXXXXXX-NNNNNNNNNNN, where
       XXXXXXXXXXXXXXXXXX is the category‟s Unique Tag and NNNNNNNNNNN is a sequential,
       system–generated number
    3. The item quantity is updated for a stock item
5. Mandatory fields:
    1. Unique items
        1. Quantity
        2. Condition
        3. Price
        4. Description, if the selected category is a generic category
    2. Stock items
        1. None – all fields are pre-set and cannot be modified
    3. Under $5 items
        1. Description
6. The Category field is a link to the inventory matrix view, which allows you to select a new category by
    drilling down to any existing category
7. The available options in the Material, Finish, Color and Features selectors should be the ones defined
    for the selected department (see Manage Attributes and Details)
8. The fields and available options under the Details section should be the ones defined for the selected
    category (see Manage Attributes and Details)
9. For Stock Items, all fields are pre-set and disabled, and cannot be changed
10. For Unique Items, all fields with values defined when the Unique Item category was created are pre-
    set and cannot be changed
11. For unique and stock items, the system makes pricing recommendations to the user on the item entry
    screen (see Suggest Item Price)
    1. For unique items, user can accept the suggested price, enter a different one, or leave it
       blank
        1. The item price can only be left blank during the processing of an acquisition. The price
           has to be set before the item can be added to the inventory
    2. For stock items, the price is pre-set and the user cannot change it
12. Receiving Associates and Pickup and Decon Associates can only add items to the inventory as part
    of processing a donation (see Receive Acquisition)
13. Pickup and Decon Associates can access the screen and enter all item information, but they cannot
    complete the add operation and add the item into the inventory.
14. The item tag, which could be an RFID tag, should contain the following information:
    1. CJ logo
    2. Department name
    3. Category name
    4. Item description
    5. Condition
    6. Size (with units)
    7. Price (with indication if item is being sold on consignment)
    8. Item number and bar code
    9. Acquisition number
    10. Date received

#### 3.5.7. Post-Condition(s):

1. Item is present in the Inventory Management System
2. Unique and stock items have item tags
3. In the case of a unique item, item is added to QuickBooks POS
4. In the case of a stock item, item quantity is updated in QuickBooks POS

#### 3.5.8. Open Issues:

None

#### 3.5.9. Extension Points:

None

#### 3.5.10. Activity Diagram(s):

None

#### 3.5.11. Notes:

See the Add Item to Inventory user interface requirements.

### 3.6. MANAGE INVENTORY ITEMS

The system should allow various management actions to be performed on items existing in the inventory.
These include modifying, deleting and splitting an item, and viewing the item‟s details and item history.
These actions are only available for Unique and Stock items.

#### 3.6.1. Actor(s):

- Administrator
- Director
- Manager

#### 3.6.2. Assumptions, Pre-Conditions & Triggers:

1. User is logged into the system

#### 3.6.3. Use Case Dependencies

1. View Inventory
2. Add Item to Inventory
3. Suggest Item Price

#### 3.6.4. Basic Flows:

1. Modify Inventory Item
    1. User accesses the main inventory screen
    2. The screen displays all inventory departments in matrix format with option to select and/or edit
       items to move them to a new department/category
    3. User drills down to the desired existing inventory item (see View Inventory)
    4. The item detail screen is presented
    5. User modifies item information
    6. The system validates item information
    7. Item information is updated in the inventory
    8. System gives the option of re-printing then item tag
    9. User optionally re-prints the item tag and attaches it to the item
2. Adjust Item Quantity
    1. User accesses the main inventory screen
    2. The screen displays all inventory departments in matrix format
    3. User drills down to the desired existing inventory item (see View Inventory)
    4. The item detail screen is presented
    5. User changes the item quantity
    6. The system displays a confirmation screen where a reason for the adjustment must be specified
       by the user
    7. The system validates the item change
    8. Item information is updated in the inventory
3. Split Inventory Item
    1. User accesses the main inventory screen
    2. The screen displays all inventory departments in matrix format
    3. User drills down to the desired existing inventory item (see View Inventory)
    4. The item detail screen is presented
    5. User clicks the Split Item button
    6. The system displays the Item Split screen
    7. User builds the list of items that the original item will be split into
        1. User can clone the original item to add new item(s) to the list that have similar attributes as
           the original item
        2. User can add new items to the list by selecting Unique and Stock categories in the same
           way as adding a new item to the inventory (see Add Item to Inventory)
    8. Once the list is complete, user confirms the split
    9. The system validates the split
    10. Item information is updated in the inventory
        1. The original (split) item is updated in the inventory
        2. Any new items that were added to the split list are added to the inventory maintaining
           parental history
4. View Inventory Item History
    1. User accesses the main inventory screen
    2. The screen displays all inventory departments in matrix format
    3. User drills down to the desired existing inventory item (see View Inventory)
    4. The item detail screen is presented
    5. User clicks the Item History button
    6. The system displays the Item History screen containing current and historical information about
       the inventory item

#### 3.6.5. Alternative Flows:

1. Modify Inventory Item
    1. User cancels the operation and is taken back to the item selection screen
    2. During data validation, data is deemed invalid and an error message is presented to the user
2. Adjust Item Quantity
    1. User cancels the operation and is taken back to the item selection screen
    2. During data validation, data is deemed invalid and an error message is presented to the user
3. Split Inventory Item
    1. User cancels the operation and is taken back to the item selection screen
    2. During data validation, data is deemed invalid and an error message is presented to the user
4. View Inventory Item History
    None

#### 3.6.6. Business Rules:

1. Modify Inventory Item
    1. All item properties available when the item was originally added to the inventory can be modified,
       except for the system-generated item number (see Add Item to Inventory).
    2. The business rules defined for adding a new item into the inventory are also applicable to
       modifying an existing inventory item (see Add Item to Inventory).
    3. Once set for the first time in the inventory, the item price can only be modified by a Manager,
       Director or Administrator, must maintain a history and include an explanation for the price
       change
    4. Changes to the item in the inventory should be reflected in the corresponding item in QuickBooks
       POS
2. Adjust Item Quantity
    1. When an item is updated, the system must automatically detect that the item quantity has been
       modified and present the adjustment confirmation screen
    2. If the quantity is decreased, a reason for the change is required
        1. Valid reasons for are:
            1. Scraped
            2. Given Away (free bin)
            3. Discarded
            4. Broken
            5. Shrinkage (stolen or lost)
            6. Correction (data entry mistake)
            7. Other (please explain)
       2. If the „Other‟ reason is selected, the user must enter an additional comment
    3. If the quantity is increased, the user must enter a comment describing the reason for the change
    4. Changes to an item‟s quantity in the inventory should be reflected in the corresponding item in
       QuickBooks POS
3. Split Inventory Item
    1. When building the split item list, at least two items must exist in the list, including the original item
    2. When building the split item list, the business rules defined for adding a new item into the
       inventory are also applicable (see Add Item to Inventory).
    3. Clicking the Clone button on a row adds a new item row with the same item values as the
       original, except for the item number, which is left blank
    4. Clicking the Add Item button takes the user through the inventory matrix so that a category can
       be selected for the new item. The user is then taken to the View/Update Item screen
    5. Clicking the category name for an item takes the user to the View/Update Item screen for that
       item
    6. All items in the split item list are saved in the inventory when the user confirms the split
       1. The original item is updated
       2. The new items are added to the inventory
       3. New items added to the inventory as part of a split item operation contain a reference to the
          original item they were split from
4. View Inventory Item History
    1. The system should record the following actions and associated parameters for every item in the
       inventory and display them on the item history screen, along with action date/time:
       1. Item added to inventory: Initial quantity, user and original (parent) item number if this item
          was created as part of a split
       2. Item price set: Initial price and user
       3. Item price changed: New price and user
       4. Item sold: Sale price and quantity
       5. Quantity adjusted: Adjusted quantity, user and reason if quantity decreased
       6. Item split: Item numbers of the new items added as part of the split and user

#### 3.6.7. Post-Condition(s):

1. Modify Inventory Item
    1. Item is updated in the inventory
    2. Item is updated in QuickBooks POS
2. Adjust Item Quantity
    1. Item is updated in the inventory
    2. Item is updated in QuickBooks POS
3. Split Inventory Item
    1. Original item is updated in the inventory
    2. Original item is updated in QuickBooks POS
    3. New items are updated in the inventory
    4. New items are updated in QuickBooks POS
4. View Inventory Item History
    None

#### 3.6.8. Open Issues:

None

#### 3.6.9. Extension Points:

None

#### 3.6.10. Activity Diagram(s):

None

#### 3.6.11. Notes:

See the Manage Inventory Items user interface requirements.

### 3.7. SUGGEST ITEM PRICE

The system should assist in the task of pricing a new inventory item by making pricing suggestions to the
user when adding to or modifying an item in the inventory. The suggested prices should be calculated
based on the original and sale prices of similar items that currently exist or existed in the inventory in the
past.


#### 3.7.1. Actor(s):

- Administrator
- Director
- Manager
- Customer Service Representative
- Receiving Associate
- Pickup Associate
- Decon Associate

#### 3.7.2. Assumptions, Pre-Conditions & Triggers:

1. User is logged into the system

#### 3.7.3. Use Case Dependencies

1. Add Item to Inventory
2. Manage Inventory Items

#### 3.7.4. Basic Flows:

1. User accesses the inventory entry screen (see Add Item to Inventory, Manage Inventory Items)
2. System shows price recommendations based on current item data and default price suggestion
   configuration options
3. User modifies item data
4. System makes new price suggestions based on new item data

#### 3.7.5. Alternative Flows:

1. User changes price suggestion configuration options
2. System shows new price recommendations based on current item data and new configuration options

#### 3.7.6. Business Rules:

1. Price suggestion is only applicable to Unique items
2. By default, price suggestion considers historical data for items of the same:
    1. Department
    2. Category
    3. Condition
3. The following price suggestion configuration parameters are available:
    1. Number of months of historical price information to include when calculating price
       recommendations. Available options:
        1. Six Months
        2. Twelve Months
        3. All (include all historical pricing data with no time restriction)
    2. Whether or not to include item attributes when finding items of similar characteristics
        1. When user chooses to include item attributes for item matching, user can specify which
           attributes to consider
4. System displays the following price recommendation information:
    1. For unique items:
        1. Historical original item price information:
            1. Lowest price
            2. Mean price
            3. Highest price
        2. Historical sale price information
            1. Lowest price
            2. Mean price
            3. Highest price
        3. Number of items evaluated when calculating the amounts above
5. For stock items
    1. System shows the pre-determined price for this stock item, set when the stock item
       category was created

#### 3.7.7. Post-Condition(s):

1. Price suggestion information is displayed on the screen

#### 3.7.8. Open Issues:

None

#### 3.7.9. Extension Points:

None

#### 3.7.10. Activity Diagram(s):

None

#### 3.7.11. Notes:

None

### 3.8. VIEW ACQUISITIONS

Acquisition records for Drop-Off, Pickup and Decon donations are created in the CRM system. Inventory
Management users should be able to view all past and current acquisitions. Receiving Associates use
this function to locate an expected acquisition when receiving a donation at the loading dock. Pickup and
Decon crews may also use this function to initiate the process of receiving items while in the truck, on
their way to the receiving dock.

Drop Off acquisitions are not typically pre-scheduled as Pick Up and Decon acquisitions except for those
submitted through the organizational website. As such, when a donor arrives with an unexpected drop off
donation, a new acquisition needs to be able to be created in the CRM system first, at either the customer
service desk or at the dock, before it can be viewed in the acquisitions screen.

#### 3.8.1. Actor(s):

- Administrator
- Director
- Manager
- Customer Service Representative
- Receiving Associate
- Pick Up Associate
- Decon Associate

#### 3.8.2. Assumptions, Pre-Conditions & Triggers:

1. User is logged into the system

#### 3.8.3. Use Case Dependencies

None

#### 3.8.4. Basic Flows:

1. User accesses the acquisitions screen
2. The screen displays a list of all acquisitions, latest ones at the top of the list
3. User may optionally filter the acquisitions displayed on the screen by changing filtering options
4. User clicks on an acquisition record
5. System display the details for that acquisition, including expected items

#### 3.8.5. Alternative Flows:

1. Drop Off acquisitions
    1. User may alternatively click the New Drop Off button on the acquisition list screen which redirects
       the user to the CRM acquisition creation screen
    2. User creates new Drop Off acquisition in the CRM system
    3. User returns to the acquisitions screen and sees the newly created Drop Off acquisition
2. User can use a bar code scanner to scan the acquisition ticket generated at customer service

#### 3.8.6. Business Rules:

1. The acquisitions screen should display:
    1. Acquisition Number
    2. Type
        1. Drop Off
        2. Pick Up
        3. Decon
        4. Donor Name with Zip Code
        5. Primary Contact Name
        6. Primary Contact Phone Number
        7. Start Date
        8. End Date
        9. Status
            1. Expected
            2. Partially Received
            3. Completed
2. Users should be able to filter (on multiple fields simultaneously ) acquisitions by:
    1. Type
    2. Donor and Primary Contact Name
    3. Acquisition Number
    4. Primary Contact Phone Number
    5. Status
3. User should be able to sort the acquisition list by any of its columns
4. The default sorting is by descending order of acquisition End Date
5. Changes to acquisition information in CRM should be immediately visible in the Inventory
    Management System.
6. Changes to acquisition information in the Inventory Management System should be immediately
    visible in CRM.
7. CRM should allow the creation of a Drop Off acquisition where only a Zip Code and Donation
    Location Type or Donor Type are provided.
8. All acquisitions are created in CRM.
9. The system should provide a link from the acquisitions view in the Inventory Management System to
    the acquisition creation screen in CRM for easy access.
10. Inventory Management users should be granted permission to create new Drop Off acquisitions in
    CRM in order to access that functionality.

#### 3.8.7. Post-Condition(s):

None


#### 3.8.8. Open Issues:

None

#### 3.8.9. Extension Points:

None

#### 3.8.10. Activity Diagram(s):

None

#### 3.8.11. Notes:

See the View Acquisitions user interface requirements.

### 3.9. RECEIVE ACQUISITION

A donor in possession of a valid acquisition number can proceed to the receiving dock where the items to
be donated will be received and processed, and a donation receipt will be generated. Alternatively, a
donor may go directly to the receiving dock, in which case a new acquisition is created by the Receiving
Associate before items can be received and processed.

The screens used for the acquisition process should simplify and expedite the data entry process,
allowing the Receiving Associate to enter only the information needed to generate the donation receipt.
Additional attributes needed to complete the item information and effectively add the item to the inventory
can be added at a second step, after the receipt has been printed and the donor has been served. The
Receiving Associate can print temporary acquisition labels for items that require further processing.

Pick Up and Decon crews may also initiate the receiving process, entering as much detailed information
about the donated items as desired, and generating a donation receipt. They cannot, however, add items
to the inventory or complete the acquisition process. A Receiving Associate is required to review all the
acquisition information before those actions can take place.

#### 3.9.1. Actor(s):

- Donor / Primary Contact
- Administrator
- Director
- Manager
- Customer Service Representative
- Receiving Associate
- Pick Up Associate
- Decon Associate

#### 3.9.2. Assumptions, Pre-Conditions & Triggers:

1. An acquisition has been created for this donation in CRM and exists in the system in the Expected
   state.

#### 3.9.3. Use Case Dependencies

1. View Acquisitions
2. Add Item to Inventory

#### 3.9.4. Basic Flows:

1. Donor or Primary Contact arrives at receiving dock with a valid donation number
2. Receiving Associate locates donation request in the system (see View Acquisitions)
3. System displays donation request information
4. Receiving Associate enters information about each donated item into the donation request (see Add
   Item to Inventory)
    1. A new item can be added to the list by cloning an existing item
    2. A new item can be added by clicking the Add Item button
    3. An item can be removed by setting the received quantity to zero
5. Receiving Associate prints a donation receipt
6. Receiving Associate optionally writes information to the receipt by hand such as condition
7. Donation receipt is given to the Donor or Primary Contact
8. Receiving Associate prints item tags for unique and stock items (see Add Item to Inventory)
9. Receiving Associate attaches printed tags to corresponding items
10. Receiving Associate closes donation request

#### 3.9.5. Alternative Flows:

1. Items can be set aside for further processing
    1. In this case, the Receiving Associate can alternatively tags displaying the donation number and
       donor information.
    2. The acquisition is left in the Partially Received state until processing is completed at a later time

#### 3.9.6. Business Rules:

1. Donation receipt information:
    1. Donation date
    2. List of donated items
        1. Description
        2. Quantity Received
        3. Condition
    3. Name of Construction Junction representative
    4. Signature of Construction Junction representative
    5. Construction Junction contact information
    6. Tax deduction information text
2. Buttons and shortcuts should be easy to click on a touch screen workstation. Extra spacing between
   rows should be added if necessary.
3. The donation item name initially displayed on each item row is the donation item name in the CRM
    acquisition record.
4. The Pickup and Decon crews can change anything on this screen and also in the item detail screen,
   but can't complete the acquisition or add items to the inventory (buttons are disabled)
5. The Email Receipt button takes you to the Email Receipt screen
6. The email receipt screen shows all email addresses associated with the Acquisition in CRM
    1. One or more can be selected to receive the email receipt
    2. If no emails are available, they need to be added in CRM
7. The system must record every time a receipt is printed or emailed
8. Selecting a stock category takes you back to the acquisition screen , not to the items details page
9. Selecting an under $5 category prompts for a description and also takes you back to the acquisition
   screen
10. Condition is optional. If left blank, the donor may write it manually on the receipt
11. Clicking add item takes you directly to the inventory matrix so that the item category can be selected,
    then to the item details screen
12. Adding an item here also adds a record to the Acquisition in CRM (shared entities)
13. Updating an item here updates the inventory fields on the Acquisition record in CRM (shared entities)
14. Completing the acquisition freezes the record in both CRM and the Inventory Management System
15. The system should record the total amount of time taken to process each acquisition
16. The original CRM acquisition data must be kept, not overridden by the values entered here

#### 3.9.7. Post-Condition(s):

1. Donated items are present in the Inventory Management System
2. Unique and stock items have item tags
3. Unique items are added to POS
4. Quantities for stock items are updated in POS
5. Donor has donation receipt
6. Donation request in the system has a status of Processed

#### 3.9.8. Open Issues:

None

#### 3.9.9. Extension Points:

None

#### 3.9.10. Activity Diagram(s):

None

#### 3.9.11. Notes:

See the Receive Acquisition user interface requirements.

### 3.10. SELL ITEM

Any item in the inventory may be purchased by a Construction Junction customer. The sale of the item is
processed by QuickBooks POS and the inventory must be updated accordingly.

#### 3.10.1. Actor(s):

- Buyer
- Sales Associate
- Customer Service Representative

#### 3.10.2. Assumptions, Pre-Conditions & Triggers:

1. The item being purchased has been previously added to the inventory.

#### 3.10.3. Use Case Dependencies

1. Add Item to Inventory

#### 3.10.4. Basic Flows:

1. Buyer arrives at the cashier or checkout desk with the items to be purchased
2. Sales associate scans the item tags
3. Sales associate processes the sale of the items in QuickBooks POS
4. The system updates the inventory to reflect the sale

#### 3.10.5. Alternative Flows:

1. Certain items sold in QuickBooks POS may not exist in the inventory (under $5 items, for instance).
   The system must be able to recognize that situation and bypass the inventory update.

#### 3.10.6. Business Rules:

1. After a sale in QuickBooks POS, the following item attributes must be updated in the inventory:
    1. Sale price
    2. Quantity on hand
2. The sale price must not override the original item price in the inventory
3. The item quantity on hand in the inventory must be decremented by the quantity sold

#### 3.10.7. Post-Condition(s):

1. Inventory is updated to reflect the sale

#### 3.10.8. Open Issues:

None

#### 3.10.9. Extension Points:

None

#### 3.10.10. Activity Diagram(s):

None

#### 3.10.11. Notes:

None

### 3.11. REPORTS

The application will provide a reporting mechanism that, at a minimum, allows Construction Junction to
review and report by inventory, inventory type, donor contact information, and the ability to link inventory
to individual that donated it.

The system should be able to generate reports based on the following entities, including reports that
correlate them:
- Inventory items
- Inventory departments
- Inventory categories
- Acquisitions
- Donors

The following are examples of reports that the system is expected to be able to generate:
- Current status of inventory
    - Item counts, value and volume by department, category, acquisition type, donor, donor
      location, donor type on hand, by date range and date range comparison
- Inventory changes
    - New item counts, value and volume by date range/comparison and by department,
      category, acquisition type, donor, donor location, donor type
    - Item sale counts, value and volume by date range/comparison and by department,
      category, acquisition type, donor, donor location, donor type
    - Deleted inventory items by date period, user
    - Item price adjustments by date period, user
- Acquisitions
    - Current partially received acquisitions
    - Number, value and volume of acquisitions processed by date range/comparison and by
      donation type, donor, donor location, donor type, receiving associate
    - Processing time by date range and by donation type, donor, donor location, donor type,
      receiving associate
    - Acquisition items entered as generic items by donation type, donor, donor location, donor
      type, receiving associate

The system should allow the Construction Junction Staff to create new reports whenever required to
satisfy their changing operational and business needs.


## 4. HIGH-LEVEL FUNCTIONAL REQUIREMENTS

This section contains high-level requirements for systems functions identified during the inception phase
as being medium and low priority items.

### 4.1. MEDIUM PRIORITY

#### 4.1.1. Website Integration

The system should integrate with Construction Junction‟s
website and allow, in addition to capacity outlined in later sections, the ability for customers to
view and search CJ‟s inventory online. The item search can be done in two ways:
- The user may „drill down‟ to a particular category using the hierarchical inventory view
  displayed on the website.
- The user may perform a search for items by keyword (basic search) and other parameters
  such as price, date received and/or discount (advanced search).

The „Shop‟ page on CJ‟s website provides a starting concept of what the categorized inventory
search might look like as does the website at http://www.seconduse.com.

„Contact Us‟ and „Online Donation Form‟ website pages should integrate with Salesforce and
allow donors to upload images.

The system should also include the implementation of Salesforce.com Ideas on CJ‟s „Recycling &
Resources‟ webpage to allow for crowd sourcing the best recycling options for various materials
in the Pittsburgh metropolitan area.

#### 4.1.2. E-Blast Flagging

The ability to easily flag items for inclusion in e-Blast, both
while adding the item to the inventory and after it has been added to inventory (such as by
scanning the bar code). This also includes adding one or more photographs of the item to the
inventory which can be included in the e-Blast or other marketing material.

A „blastworthy‟ flag already exists on the item entry and update screens. That field can be used to
flag an item for inclusion on the next e-Blast.

When an item is flagged for e-Blast, the system should verify that a stocking location has been
set for the item.

The system should allow Construction Junction staff to view a list of all items that are currently
flagged as blastworthy that haven‟t yet been included in an e-Blast. The user can then select
which flagged items should be included on the next e-Blast.

The system should also provide an e-Blast preview screen that displays all items selected for that
week‟s e-Blast, and also all items that have been flagged but not selected.

A cart with a laptop, camera and bar code reader will be used by the Construction Junction staff
when looking for items in the sales floor that should be e-Blasted. That allows the user to quickly
locate an item in the inventory by scanning its tag, flag items that aren‟t yet flagged and enter
additional item information prior to the e-Blast.

The system should integrate with Vertical Response (or its future possible replacement, Exact
Target) for the e-Blast email notifications.

The system should also allow Construction Junction staff to view a list of all items that were
included in previous week‟s e-Blast and that have been sold. The user can then select the items
that should be included in the „Great and Gone‟ section of the website. The system should also
allow the user to select any sold items, adding pictures as needed, to be included in the „Great
and Gone‟ section, even if they were not part of previous week‟s e-Blast. „Great and Gone‟ items
should have a “Sold” overlay over their associated images.

Items should be able to be re-Blasted without affecting previous e-Blast versions.

#### 4.1.3. e-Commerce Integration

Integration with the Construction Junction website to
allow for online purchases and auctions, automatically adding new items to the e-Commerce site
and updating the site when items are sold, either through the e-Commerce site or in the store.
Additionally, support inventory that is available only through the e-Commerce site and cannot be
purchased in the store.

The website should present an „Add to Cart‟ button on search results and item detail screens and
standard „View Shopping Cart‟ and checkout functionality as well as the option to „forward item to
a friend‟.

The system does not need to support shipping options. All items purchased have to be picked up
at the Construction Junction site.

Only items flagged as available for online purchase on the inventory system can be purchased
online. Those items are held in a separate area in the warehouse designated for online items and
can only be purchased online.

For items that are not available for online purchase the website should display a comment that
reads 'You can purchase this item over the phone or at Construction Junction'. When an item is
purchased over the phone it is physically moved to the SOLD items area in the warehouse, but
should remain on the website for an additional 15 days with “Sold” appearing across the item
name and image.

#### 4.1.4. Membership Program

Implement a membership program that would make it
easier to track customer/donor activity. Based on a membership card, linked to the
donor/customer contact in CRM and QuickBooks POS, where swiping or scanning the card
would quickly bring up the customers information, making the donation or purchasing process
faster (eliminating the need for Construction Junction staff to enter the name and demographic
information for repeat donors/customers). Once established, a membership card program could
be used for any number of uses, such as:
- A membership rewards or frequent donor rewards program
- Special “members only” promotions, coupons or discounts
- Targeting marketing for program members

Once registered online, the system should allow Construction Junction staff to print out a member
card (possibly via QuickBooks POS) containing the member‟s name and unique member ID, in
both numeric and bar code format. The member card can be scanned by Construction Junction
staff to quickly identify the member when donating or purchasing items. The member‟s email
address and associated customer ID/barcode should uniquely identity the member in both
QuickBooks POS and in the CRM system.

The system should allow Construction Junction to reward customers for frequent donating by
giving them in-store credit that can be used when purchasing items.

The „Reuse Reward‟ amount credited for each donated item should be kept separate from store
credit for returned merchandise and be calculated as follows:
- For stock items, credited when the item is received, and calculated as 0.5% of the stock
  item‟s pre-defined price.
- For unique items, credited only the item is sold, and calculated as 1% of the price the
  item was actually sold for.

The system should also provide reports that show all items a particular donor brought in and how
much those items were sold for.

QuickBooks POS should be aware of the current amount of credit accrued by a member so that it
can be used whenever the member wants to purchase an item. Users should be able to use their
accrued balance to buy gift certificates and give them to someone else.

The system should be able to print the donor‟s current credit amount on the donation receipt.
QuickBooks POS should also print a message on the sales and donation receipt informing
customers that they can earn rewards by donating to Construction Junction.

Additional membership benefits should include:
- Signing up for CJ‟s weekly e-Blast (all users who sign up for the e-Blast are automatically
  members and all users who sign up to be members automatically receive the weekly e-
  Blast (unless they manually uncheck that option)).
- Ability to manage online profile including status of e-Blast subscription, donation
  addresses, view sales history, donation history and re-reprint donation receipts online.
- Ability to have insight into the type of items scheduled for pickup by CJ
- Automatic notification when accumulated credits reach a certain self-defined threshold.
- Ability to create a public green business or service listing.
- Ability to upload images and video of their reuse project(s)
- Advance notification of new class offerings and upcoming events.
- Easier purchasing of items offered online and automatic pre-registration for online
  auctions.
- Option to purchase CJ gift cards at a slightly discounted rate.
- Bonus in store discounts on member‟s birthday.
- Allows faster completion of online donation form and allows user to view and request
  available slots in CJ‟s pickup schedule.

#### 4.1.5. Customer Wish List

Provide users with the ability to notify Construction
Junction of items that they would like to purchase and be notified when/if those items become
available. Customer wish lists would only be viewable by Construction Junction staff and will not
be publicly available.

Construction Junction website users should be able to select a particular item category in the
inventory (via an inventory or e-Blast view) and add it to their wish list. Users should also be able
to add to the wish list any of the categories for items returned as search results. Anytime a new
item is received into the inventory in that category, an automated notification is then sent to the
user.

The notification can be in multiple forms such as an email message, text message, voice blast,
Twitter or Facebook. That option is set by the user in his/her website account settings. That
means that in order to take advantage of the wish list functionality, the user must be registered as
a Construction Junction website member.

Customer Service representatives should also be able to add to a customer‟s wish list when
requested by him/her at the customer service desk or via email phone, etc..

Users should be able to view their current wish line online and remove entries from it.

Users should also be able to add to their wish lists the categories of items that have been sold
over the past 15 days. That means that once an item is sold, it should still be listed on the website
for a period of 15 days, and its listing should contain the „SOLD‟ word on it.

#### 4.1.6. Pickup/Decon Logistics

This functionality has been implemented in large part
to date, including donation receipts and pick up forms, but additional required functionality
includes:

- A system that will support scheduling and tracking Pickup and Decon jobs by providing
  map views that can be filtered by various parameters including location, date range
  (today, next week, next month, all, etc.) and donation type.
- Map shows donations with truck icon that reflects portion of truck capacity consumed.
- On hover over, mini page layout shows: date, portion of truck consumed, crew name,
  appointment time, estimated value and donation description.
- Automatic reminder emails to donors one day before a scheduled pickup is to occur as
  well as automatic thank you emails once a donation acquisition has been completed.

#### 4.1.7. Inventory Aging/Automatic Price Discount

Automatically decrease
price of inventory items by a set amount that have remained in the inventory for a set period of
time. For example, reducing the price by 10% each month that the item remains in inventory

The item entry and update screens should include a „Subject to Aging Discount‟ flag. The system
should use that flag to automatically generate discounts for items based on the amount of time
they have been in the inventory.

The discount should be calculated as a 10% discount for each month that the item has been in
the inventory, and the item label should display the discounted prices and their corresponding
date periods. The aging starts on the date when the item is assigned a price and is effectively
added to the inventory, and not when the item is received.

QuickBooks POS should apply the correct discount for the current date when an item is sold, and
the website should automatically display the correct discount for the current date (requires regular
data transfer).

#### 4.1.8. On-site Storage

The ability to track those items purchased by customers but left
on-site for a maximum seven day period until the customer is able to return to pick up the
item(s).

The sold item should be able to be viewed in Salesforce and flagged as „stored on-site‟ with an
automatic „pick up date‟ calculated for seven days out. Staff can print a sold tag that is affixed to
the sold item.

Automatic emails are sent to the customer as required pick-up dates approach and the status of
items is updated as they are picked up.

Tasks are generated for staff to return overdue items to the sales floor and apply the appropriate
store credit to customer accounts for items that have not been picked up within the allotted
seven day period. This puts the item back into inventory and affects customer store credit
accounts.

#### 4.1.9. Overstock Pricing

The ability to set thresholds for specific items or categories
that will indicate that there are too many or too little of these items in the inventory and allow the
prices to be adjusted for the over or under stock condition.

The system must allow a threshold quantity to be set at any level (department or category) in the
inventory. Once that threshold is reached for a department or category, the corresponding matrix
cell should change to a different color that indicates the overstock condition. Also, the current
quantity on hand and the threshold value for the item‟s department or category should be
displayed on the item entry and update screens. This information should also be displayed on a
different color or layout when the threshold is reached.

The system should still allow items to be received for a department or category that is
overstocked, but Construction Junction staff may decide to turn down those items at the receiving
dock.

The system should also provide a report that shows currently overstock departments and
categories.

Based on the overstock report Construction Junction staff may decide to put the entire category
on sale for a period of time, or until the category is no longer overstocked. As the discount is only
temporary, the item prices should not be changed in the Inventory. However, the price discount
should be automatically applied on purchases via QuickBooks POS, and should also be visible on
the website.

### 4.2. LOW PRIORITY

#### 4.2.1. Mobile Handheld Units

The ability to scan items on the store floor and update
the inventory item from a small handheld unit or tablet PC. Additionally, handheld/tablet units
that can be used by Pickup and Decon crews on worksites.

The mobile units should allow that all inventory screens can be displayed and used in the same
fashion as in the fixed workstations. This eliminates the need for designing a second set of
screens to be used on mobile units with limited display capabilities.

#### 4.2.2. Inventory Item Story/History

The ability to add a history or back story for
items with particularly unique or significant origins and share this store with customers on the
website and in the store.

The Inventory Item entry screen already provides a comments/history text field that can be used
for the purpose described.

In addition to that, the system should be able to generate and print signage containing the item
history, back story information and other item details. Ideally, the system would provide a few pre-
defined formats for signage that can be chosen from.

#### 4.2.3. Calculate Shipping Weight

Extend the Pickup/Decon Logistics system to
calculate donation size/truck capacity.

The described functionality is being implemented as part of the CRM project.

In addition, the Inventory Management System needs to store item weight information and
generate reports that indicate the total weight received, sold and diverted from landfills.

When the actual item weight is not indicated, the system should use a pre-set average weight for
the item category.

The system should also display the actual weight average for the category on the category
configuration screen, and also the number of items used when calculating that average. The
inventory administrator can then decide whether to configure the category to use the actual
average weight or a pre-set average weight, which would be set manually.

#### 4.2.4. Donor Ranking/Feedback

Allow Construction Junction staff to enter
information on Donors related to details of the donors location, ease of working with the donor,
and any additional information that may be helpful for future donations.

The described functionality, which ranks the donor in terms of ease of working with, is being
implemented as part of the CRM project.

Construction Junction would also like to be able to generate the following donor statistics, which
could be implemented in the form of reports:

- Number/value/volume of donations per donor
- Fastest selling donations / time to sell per donor
- Value retention of items (sold x estimated price) per donor
- Overall donor rating


## 5. SUPPLEMENTARY REQUIREMENTS

This section outlines requirements that are not covered within the use cases and other preceding high-
level requirements sections. It documents non-functional requirements of the system that capture quality
attributes, implementation approach, compatibility concerns, deployment and more.

### 5.1. USABILITY

The application is expected to operate via touch screen user interfaces, and take advantage of that
technology to be as fast, efficient, intuitive, and flexible as possible while also minimizing the potential for
errors and duplications. It should minimize the use of keyboard and mouse when processing
acquisitions, and should allow acquisitions to be completed with few clicks and page switches.

### 5.2. AVAILABILITY

For internal users:
- Donation/acquisition processing - The system must be available during normal Construction
  Junction operating hours.
- Sales processing - The system must be available during normal Construction Junction operating
  hours.
- Inventory management - The system must be available beyond normal operating hours to
  accommodate inventory management operations.

For external users - The system must be available beyond normal operating hours to accommodate
website use – Inventory listing, wish list management and online purchases.

### 5.3. RELIABILITY

There are no reliability requirements.

### 5.4. SECURITY

Access to the application by the Construction Junction staff must require user login. Access to application
screens and functions is granted or denied based on the profile and role of the currently logged in user,
as detailed in the preceding use-case requirements. The system should record changes to application
entities in the form of „created user/time‟, „modified user/time‟ fields. The system should also record
information about various sensitive inventory management operations such as deleting items and
changing the price of items.

### 5.5. PERFORMANCE

The functionality provided by the Inventory Management System will be critical to the normal operation of
the Construction Junction business. As such, the system should perform with consistently and predictably
low response times in order not to impact the performance or the timely execution of the various tasks
that need to be conducted by the Construction Junction staff.

### 5.6. INTERFACES

#### 5.6.1. User Interface

A web browser-based interface must be provided for all the Inventory Management functionality. This
sections lists the screens required and associated UI requirements.

The following are specific UI requirements for the entire Inventory Management application:
1. Buttons and shortcuts should be easy to click on a touch screen workstation. Extra spacing between
    rows should be added if necessary.
2. All required information fields should be marked with an asterisk (*).
3. During data validation, all validation errors must be reported to the actor and displayed on the screen.
4. In case of a validation error, the actor must not have to re-enter the values that are valid

#### 5.6.1.1. View Inventory

The following screens show the suggested screens and page layouts for the View Inventory use-case.

```
Figure 1 – Main Inventory View
```

The first screen in the categorized inventory view is the departments screen.

1. Inventory departments are displayed in matrix format
2. The matrix dimensions are fixed, and are the same when displaying departments or categories.
    1. The actual matrix dimensions are to be determined during system implementation.
    2. The matrix should be able to hold at least 30 tiles at each level
3. Unused matrix cells are displayed empty.
4. Each matrix cell displays a department name
    1. For departments with subcategories, the department name is a hyperlink to the view of the
       department subcategories
    2. For a department with no subcategories, the department name is a hyperlink to the view of the
       items in that department
5. Departments are listed in alphabetical order in each row, from left to right and top to bottom
6. Each cell in the matrix must indicate in some visual form that it contains subcategories
7. Inventory categories are displayed in matrix format
8. The matrix dimensions are fixed, and are the same when displaying departments or categories.
    1. The actual matrix dimensions are to be determined during system implementation.
    2. The matrix should be able to hold at least 30 tiles at each level
9. Unused matrix cells are displayed empty.
10. Each matrix cell displays a category name.
    1. For categories with subcategories, the category name is a hyperlink to the view of the
       subcategories
    2. For a category with no subcategories
       1. For a Unique Item category, the category name is a hyperlink to a view of the items under
          that category
       2. For a Stock Item category, the category name is a hyperlink to a view of the details for
          that Stock Item, including the current quantity on hand
       3. For a Under $5 category:
            1. The category name is not a hyperlink
11. Categories are listed in alphabetical order in each row, from left to right and top to bottom
12. Each cell in the matrix must indicate in some visual form that it contains subcategories
13. The cell in the top left corner of the matrix always represents a generic item in the selected
    department (e.g. a generic appliance when viewing the categories in the appliance department) and
    is automatically generated by the system
14. The cell to the right of the top left corner of the matrix always represents under $5 items in the
    selected department and is automatically generated by the system

```
Figure 2 - Inventory Department View
```

```
Figure 3 - Inventory Category View
```

1. Inventory categories are displayed in matrix format
2. The matrix dimensions are fixed, and are the same when displaying departments, categories.
    1. The actual matrix dimensions are to be determined during system implementation.
    2. The matrix should be able to hold at least 30 tiles at each level
3. Unused matrix cells are displayed empty.
4. Each matrix cell displays a category name.
    1. For categories with subcategories, the category name is a hyperlink to the view of the
       subcategories
    2. For a category with no subcategories
       1. For a Unique Item category, the category name is a hyperlink to a view of the items under
          that category
       2. For a Stock Item category, the category name is a hyperlink to a view of the details for that
          Stock Item, including the current quantity on hand
       3. For a Under $5 category:
            1. The category name is not a hyperlink
5. Categories are listed in alphabetical order in each row, from left to right and top to bottom
6. Each cell in the matrix must indicate in some visual form that it contains subcategories
7. The cell in the top left corner of the matrix always represents a generic item in the selected category
   (e.g. a generic refrigerator when viewing the sub-categories in the refrigerator category) and is
   automatically generated by the system

```
Figure 4 - Inventory Items View
```

1. The screen should display all items for the selected department or category that match the selected
   filter criteria including attributes, features and/or detail fields
2. The Item number is a hyperlink to the detailed item view screen for that item allowing recategorization
3. The list can be sorted by any table column
4. Each level (department or category) in the breadcrumbs at the top of the page is a hyperlink to the
   inventory items view for that department or category
5. The Add Item button is only present if user is a Manager, Director or Inventory Administrator

```
Figure 5 - Inventory Item View
```

1. Fields are only editable if user is a Manager, Director or Inventory Administrator
    1. All fields are editable with the exception of the system generated item number
2. The Cancel and Save buttons are only present if user is a Manager, Director or Inventory
   Administrator
3. The Split Item link is only present if user is a Manager, Director or Inventory Administrator
4. Additional fields could include: model #, eligible for commission, architectural salvage and URL links
   to similar items in retail stores such as Home Depot and Lowes.

#### 5.6.1.2. Manage Departments

The following screens show the suggested screens and page layouts for the Manage Departments use-
case.

```
Figure 6 – Main Inventory Management View
```

The first screen when managing the categorized inventory departments is the departments screen. A
button for adding a department should exist at this level.

```
Figure 7 – Inventory Management - Department
```

Drilling down to a particular department takes you to the view of all categories in the department. A button
to edit the department settings should exist at this level.

```
Figure 8 – Add/Edit Department Screen
```

1. The following fields are mandatory:
    1. Name
    2. POS Department Code
    3. Unique Tag
2. The Department Name must be unique across the inventory
3. The Department‟s Unique Tag must be unique across the inventory
4. The POS Department Code must be at most 3 characters long
5. The Unique Tag must be at most 18 characters long
6. There must be at least one slot available in the Department matrix to hold the new Department
7. A Department cannot be deleted if it contains categories and/or items
8. The system must ask for confirmation before deleting a Department

#### 5.6.1.3. Manage Categories

The following screens show the suggested screens and page layouts for the Manage Categories use-
case.

```
Figure 9 – Inventory Management - Department
```

To start managing categories, the user needs to drill down to the department level. Buttons for adding
and moving categories should exist at this level.

```
Figure 10 – Inventory Management - Category
```

The button for editing a category exists at that category level.

```
Figure 11 – Add/Update Category Screen - Stock
```

1. The following fields are mandatory:
    1. Name
    2. Unique Tag
    3. Price
2. The Category Name must be unique across the inventory
3. The Category‟s Unique Tag must be unique across the inventory
4. The Unique Tag must be at most 18 characters long
5. There must be at least one slot available in the Category matrix at the level the new Category will be
   created to hold the new Category
6. The available options in the Material, Finish, Color and Features selectors should be the ones defined
   for the selected department (see Manage Attributes and Details)
7. The fields and available options under the Details section should be the ones defined for the selected
   category (see Manage Attributes and Details)
8. The system must ask for confirmation before deleting a category
9. Additional fields could include: model # and URL links to similar items in retail stores such as Home
   Depot and Lowes.

```
Figure 12 – Add/Update Category Screen - Unique
```

1. The following fields are mandatory:
    1. Name
    2. Unique Tag
2. The Category Name must be unique across the inventory
3. The Category‟s Unique Tag must be unique across the inventory
4. The Unique Tag must be at most 18 characters long
5. There must be at least one slot available in the Category matrix at the level the new Category will be
   created to hold the new Category
6. The available options in the Material, Finish, Color and Features selectors should be the ones defined
   for the selected department (see Manage Attributes and Details)
7. The fields and available options under the Details section should be the ones defined for the selected
   category (see Manage Attributes and Details)
8. The system must ask for confirmation before deleting a category
9. Additional fields could include: model # and URL links to similar items in retail stores such as Home
   Depot and Lowes.

```
Figure 13 – Move Categories Screen
```

1. The Categories to Move selector is populated with the categories seen on the matrix at the level
    where the Move Categories button was pressed.
2. User must select at least one Category to move
3. User must select either an existing target Department or Category, or new target Category
4. User cannot move categories to any Departments or Categories that don‟t have enough slots
   available in the matrix to hold the moved categories
5. User cannot move categories to any of their subcategories (cannot create loops in the inventory
   hierarchy)
6. If a new target category is selected
    1. User must enter
        1. Name
        2. Unique Tag
        3. Location of new category
7. User cannot select a Stock Item, Under $5 Category or Generic Category as the target category
8. When a category is moved it keeps its assigned Item Details
9. When the option to merge the contents of the selected Categories is selected, the Item Details
   assigned to the selected Categories are combined and assigned to the target Department or
   Category

#### 5.6.1.4. Manage Attributes and Details

The following screens show the suggested screens and page layouts for the Manage Attributes and
Details use-case.

```
Figure 1 4 – Main Inventory Management View
```

The first screen when managing the categorized inventory attributes and details is the departments
screen. Buttons for editing attributes and details should exist at this level.

```
Figure 1 5 – Add/Edit Attributes Screen
```

1. Material and Features attributes can be assigned to any combination of departments
2. Material and Features attributes can be assigned to „All‟ departments
3. Color and Finish attributes can only be set to „All‟ departments
4. An Attribute cannot be set simultaneously to „All‟ departments and to specific department(s)
    1. Assigning an attribute to „All‟ departments disables the individual department selectors, but
       preserves the current department selections
    2. Un-assigning an attribute from the „All‟ departments enables the individual department selectors,
       restoring the previous department selections

```
Figure 1 6 – Add/Edit Attribute Screen
```

1. The following fields are mandatory:
    1. Name
2. The Item Attribute Name must be unique across the inventory
3. The De-Activate Attribute button is replaced with an Activate Attribute button when the attribute is
   inactive

```
Figure 1 7 – Edit Details Screen
```

1. Details can be assigned to any combination of departments and categories
2. Details can be assigned to „All‟ departments and/or categories
3. Assigning a detail to a department or category automatically assigns it to its subcategories and vice
   versa to its top level department

```
Figure 1 8 – Add/Edit Details Screen
```

1. The available detail types are:
    1. Number
    2. Text
    3. Selection
2. The following fields are mandatory:
    1. Name
    2. Type
3. If the Type is set to „Selection‟, then the selection list must contain at least one item
4. The Item Detail Name must be unique across the inventory
5. The De-Activate Detail button is replaced with an Activate Detail button when the detail is inactive

#### 5.6.1.5. Add Item to Inventory

The following screens show the suggested screens and page layouts for the Add Item to Inventory use-
case.

```
Figure 19 – Receive/Add Item
```

Users can access the Receive/Add Item from the Receive Acquisition screen when processing an
acquisition, or from the View Inventory Items screen when browsing the inventory.

1. Mandatory fields:
    1. Unique items
        1. Quantity
        2. Condition
        3. Price
        4. Description, if the selected category is a generic category
    2. Stock items
        1. None – all fields are pre-set and cannot be modified
    3. Under $5 items
        1. Description
2. The Category field is a link to the inventory matrix view, which allows you to select a new category by
   drilling down to any existing category
3. The available options in the Material, Finish, Color and Features selectors should be the ones defined
   for the selected department (see Manage Attributes and Details)
4. The fields and available options under the Details section should be the ones defined for the selected
   category (see Manage Attributes and Details)
5. For Stock Items, all fields are pre-set and disabled, and cannot be changed
6. For Unique Items, all fields with values defined when the Unique Item category was created are pre-
   set and cannot be changed
7. For unique and stock items, the system makes pricing recommendations to the user on the item entry
   screen (see Suggest Item Price)
    1. For unique items, user can accept the suggested price, enter a different one, or leave it blank
    2. For stock items, the price is pre-set and the user cannot change it
8. The Add to Inventory button is not enabled for Pickup and Decon Associates.
9. Additional fields could include: model #, eligible for commission, architectural salvage and URL links
   to similar items in retail stores such as Home Depot and Lowes.

#### 5.6.1.6. Manage Inventory Items

The following screens show the suggested screens and page layouts for the Manage Inventory Items
use-case.

```
Figure 20 – View/Update Item
```

All users can access the View/Update Item from the View Inventory Items screen when browsing the
inventory, and a Manager, Director or Inventory Administrator can update item properties.

1. All fields are editable with the exception of the system generated item number
2. Mandatory fields:
    1. Unique items
        1. Quantity
        2. Condition
        3. Price
        4. Description, if the selected category is a generic category
    2. Stock items
        1. None – all fields are pre-set and cannot be modified
    3. Under $5 items
        1. Description
3. The Category field is a link to the inventory matrix view, which allows you to select a new category by
   drilling down to any existing category
4. The available options in the Material, Finish, Color and Features selectors should be the ones defined
   for the selected department (see Manage Attributes and Details)
5. The fields and available options under the Details section should be the ones defined for the selected
   category (see Manage Attributes and Details)
6. For Stock Items, all fields are pre-set and disabled, and cannot be changed
7. For Unique Items, all fields with values defined when the Unique Item category was created are pre-
   set and cannot be changed
8. For unique and stock items, the system makes pricing recommendations to the user on the item entry
   screen (see Suggest Item Price)
    1. For unique items, user can accept the suggested price, enter a different one, or leave it blank
    2. For stock items, the price is pre-set and the user cannot change it
9. Additional fields could include: model #, eligible for commission, architectural salvage and URL links
   to similar items in retail stores such as Home Depot and Lowes.

```
Figure 21 – Adjust Item Quantity
```

1. Mandatory fields:
    1. Reason, if quantity is being adjusted down
    2. Comment, if quantity is being adjusted up or if the selected Reason is Other
2. Valid reasons are:
    1. Scraped
    2. Given Away (free bin)
    3. Discarded
    4. Broken
    5. Shrinkage (stolen or lost)
    6. Correction (data entry mistake)
    7. Other (please explain)

```
Figure 22 – Split Item
```

1. Mandatory fields:
    1. New quantity
    2. Condition
2. When building the split item list, at least two items must exist in the list, including the original item
3. Clicking the Clone button on a row adds a new item row with the same item values as the original,
   except for the item number, which is left blank
4. Clicking the Add Item button takes the user through the inventory matrix so that a category can be
   selected for the new item. The user is then taken to the View/Update Item screen
5. Clicking the category name for an item takes the user to the View/Update Item screen for that item
6. Item history should also include:
    1. On hand value
    2. Plus or minus value adjustment

```
Figure 23 – View Item History
```

#### 5.6.1.7. View Acquisitions

The following screens show the suggested screens and page layouts for the View Acquisitions use-case.

```
Figure 24 – View/Search Acquisitions Screen
```

1. The acquisitions screen should display:
    1. Acquisition Number
    2. Type
        1. Drop Off
        2. Pick Up
        3. Decon
    3. Donor Name
    4. Primary Contact Name
    5. Primary Contact Phone Number
    6. Start Date
    7. End Date
    8. Status
        1. Expected
        2. Partially Received
        3. Completed
2. Users should be able to filter acquisitions by:
    1. Acquisition Number
    2. Donor and Primary Contact Name
    3. Type
    4. Primary Contact Phone Number
    5. Status
3. User should be able to sort the acquisition list by any of its columns
4. The default sorting is by descending order of acquisition End Date
5. The New Drop Off button takes the user to the acquisition creation screen in CRM for easy access.

#### 5.6.1.8. Receive Acquisition

The following screens show the suggested screens and page layouts for the Receive Acquisition use-
case.

```
Figure 25 – Receive Acquisitions Screen
```

1. Mandatory fields:
    1. Received Quantity
2. Condition is optional. If left blank, the donor may write it manually on the receipt
3. The donation item name initially displayed on each item row is the donation item name in the CRM
   acquisition record.
4. Selecting a stock category takes you back to the acquisition screen , not to the items details page
5. Selecting an under $5 category prompts for a description and also takes you back to the acquisition
   screen
6. Clicking add item takes you directly to the inventory matrix so that the item category can be selected,
   then to the item details screen
7. Date received is tracked on an item by item basis
8. The Complete Acquisition button is disabled for Decon and Pickup Associates
9. The Email Receipt button takes you to the Email Receipt screen
10. The email receipt screen shows all email addresses associated with the Acquisition in CRM
    1. One or more can be select to receive the email receipt
       If no emails are available, they need to be added in CRM

### 5.6.2. Hardware Interfaces

The system should support the following hardware interfaces:

- Touch screen monitors – To facilitate navigation of the categorized inventory when processing
  acquisitions and also for normal inventory maintenance tasks
- Bar code readers – For scanning item labels and member cards
- Zebra printers – For quick printing of item labels
- Standard, color laser printers – For printing donation receipts, item signage and reports
- Mobile devices

### 5.6.3. Software Interfaces

Implementation of all requirements outlined in this document requires that the Inventory Management
System interface with the following systems:

1. QuickBooks POS
    1. Constituent data between QuickBooks POS and Salesforce must be synchronized
    2. Updates to the inventory such as new items and changes to existing items must be synchronized
       to QuickBooks POS
    3. Inventory items must be updated as a result of sales in QuickBooks POS
    4. Customer‟s sales history must be synchronized to QuickBooks POS and roll up in a similar
       fashion as donation statistics
    5. Changes to a member‟s in-store credit amount as a result of donated item sales should be made
       available to QuickBooks POS
    6. Customers with bouncing email addresses must be identified in QuickBooks POS
    7. Integration between QuickBooks POS and Salesforce must use Middleware
2. Salesforce CRM
    1. All contact information utilized by the Inventory Management System, including donor and
       donation acquisition information, is stored in Salesforce CRM
3. Vertical Response
    1. Construction Junction currently uses Vertical Response to deliver email marketing functionality
       such as weekly e-blasts.
    2. Vertical Response App must be installed in Salesforce and consider storage consumption
    3. At the time of this writing, Construction Junction is considering replacing VerticalResponse with
       ExactTarget
4. Construction Junction website
    1. The system must be able to provide the contents of the categorized inventory for viewing on the
       website, allowing users to create wish lists and purchase items online
    2. The inventory should be updated to reflect item purchases via the website
    3. Construction Junction members should be able to log into CJ‟s website
5. CTI Telephony Integration
    1. Construction Junction intends to add this functionality
6. MS Outlook integration
7. Google Apps
    1. Construction Junction is currently evaluating the benefits of replacing Microsoft Office products
       and Exchange Server with Google Apps and Gmail.

### 5.7. CLIENT PLATFORM

The user interface implementation should strive to use cross-browser standards wherever possible and
avoid any use of browser-specific features.

### 5.8. DATA MIGRATION

Constituent and sales history data from Construction Junction‟s QuickBooks POS system must be
migrated to Salesforce.

As the Inventory Management System does not replace any existing legacy system, there is no inventory
data to migrate.

Construction Junction has acquired CRM Fusion products including Demand Tools, People Import and
Dupe Blocker to assist with these efforts.

### 5.9. DISASTER RECOVERY, BACKUPS, AND BUSINESS CONTINUITY PLAN

As the Inventory Management System does not replace any existing legacy system, Construction
Junction doesn‟t currently have documented procedures for disaster recovery, backups and business
continuity for its inventory operations. Appropriate procedures will need to be developed and documented
for the chosen implementation platform. That should include:

- Backups - How will backups be done, what data the backups are to include, where the backup media
  will be stored, and for how long that media will be maintained.
- Disaster Recovery and Business Continuity Plan - How the system will be recovered, the timeframe
  for recovery, and the fallback procedures to allow business to continue including offline capabilities.

### 5.10. MAINTAINABILITY

The system must be written using industry best practices, and must be built using only Construction
Junction approved products and technologies. The system must also be written in such a way that it can
be supported by planned Construction Junction staffing levels.

### 5.11. PORTABILITY

There are no applicable portability requirements to implement this functionality.

### 5.12. LEGAL, COPYRIGHT AND OTHER NOTICES

The following copyright notice must be displayed in all user interfaces:

```
© 2009 - <current year> Construction Junction
```

### 5.13. LICENSING

The Inventory Management System will most likely utilize a variety of open source and commercial
products in its development lifecycle. The Inventory Management System is not considered a derivative
work of such products.

### 5.14. APPLICABLE STANDARDS

There are no applicable standards to implement this functionality.


## APPENDIX A: REFERENCES

The following print and electronic materials were used in reference for the creation of this document, both
in systematic structure as well as subject content.

- Construction Junction‟s Toolkit Inventory Screens spreadsheet
- Construction Junction‟s Project Goals document
- Construction Junction‟s Inception Findings and Recommendations document


## APPENDIX B: GLOSSARY

The following terms are used throughout the document. Their definitions in the context of this SRS are
listed below:

- Actor: Someone or something that supplies a stimulus to the system, including users and other
  systems. Actor definitions do not map one-to-one with specific people or things. For example, one
  particular user (John Smith) may interact with the system as an Internal User to run a report and as a
  User Administrator to modify a user‟s information.
- SRS: Software Requirement Specification – a document defining and describing the business needs
  and processes related to the system and the expectations for the completed system.
- POS: QuickBooks Point of Sale system. The point of sale system currently in use by Construction
  Junction
- Unique Item: A type of item which typically has unique characteristics and is individually priced. E.g.:
  Antique piece of furniture. Each unique item has its own entry in the inventory system.
- Stock Item: A type of item with which typically has similar characteristics and a standard price. E.g.:
  Toilet seat. There is only one entry in the inventory for each stock item category.
- Under $5 Item: Small, inexpensive items which are not tracked by the inventory system. E.g.: Nuts
  and bolts