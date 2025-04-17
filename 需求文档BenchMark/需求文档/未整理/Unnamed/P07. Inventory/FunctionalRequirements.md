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