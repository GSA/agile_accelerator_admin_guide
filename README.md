# Admininstrators Guide to Agile Accelerator
Below are supplemental instructions for customizing an installation of Salesforce's Agile Accelerator. 

- [Add Work Type to Work Status Detail Page]               (#add-work-type-to-work-status-detail-page)
- [Add Tabs for Other AA Objects]                          (#add-tabs-for-other-aa-objects)
- [Update Column Lookup Search Layout]                     (#update-column-lookup-search-layout)
- [Updating Kanban Board to Reflect Work Status]           (#updating-kanban-board-to-reflect-work-status)


## Add Work Type to Work Status Detail Page
Agile Accelerator associates Work Types (Bug, User Story, etc) to specific Work Statuses. However, using a fresh installation, it can be difficult to determine which Work Types are associated to specific Work Statuses. The steps below walk through the process of updating the page layout for Work Status to display the Work Type relationship.

- Navigate to Setup
- From Setup go to Create > Objects > Work Status
- On the Work Status Custom Object Definition Detail Page, scroll to the Page Layouts section
- Click Edit on the Status Layout
- Drag the Type field into the Status Detail layout
- Save

## Add Tabs for Other AA Objects
Out of the box, Agile Accelerator does not create tabs for a number of objects that are important when customizing the installation. We found it helpful to create tabs for the following Agile Accelerator objects: Work Status, Column, and Column Status Assignment. 

- Navigate to Setup
- From Setup go to Create > Tabs > New
- Select the object of your choice and a color
- Click Next
- Associate the tab to any necessary profiles 
- Associate the tab to the Agile Accelerator App
- Save

Once the tab has been created, it can be added to the default display.
- Navigate to Setup
- From Setup go to Create > Apps > Agile Accelerator 
- Click Edit on the Agile Accelerator App Detail Page
- Add the desired tab to the Selected Tabs list
- Save

## Update Column Lookup Search Layout
Columns are associated to Teams which results in many columns of the same name being produced. However, when searching for a column, only the column name appears and it is easy to select the wrong column to associate.
- Navigate to Setup
- From Setup go to Create > Objects > Column
- Scroll down to the Search Layouts section
- Click Edit next to the Lookup Dialogs layout
- Add the following columns: Active, Team
- Check the "Override the search result column customizations for all users" checkbox
- Click Save

## Updating Kanban Board to Relfect Work Status
Out of the box, the Agile Accelerator Kanban board is set up with a basic workflow. However, this workflow may not match the workflow used by your team.  A number of steps must be taken to associate Work Statuses to the Kanban board and a specific team, they are outlined below.

### Create New Work Status
Each Work Type (Bug, User Story, Investigation) is associated with a number of Work Statuses. These statuses can be customized but will apply to all teams utilizing that Work Type.

- Go to the Work Status tab
- Click New
- Enter a number for the order in which you would like the Work Status to appear in a drop down list. Low numbers are 'lighter' and float the Work Status to the top of a picklist. For instance, a Work Status with an order of 5 will appear in a picklist before a Work Status with a value of 10.
- Enter the name of the Work Status
- Select the Work Type(s) which should be associated with the particular Work Status
- Save

#### Add New Work Status to Status Drop Down
Before you can use the new Work Status field, you must add it to a picklist in the Work object
- Navigate to Setup
- From Setup go to Create > Objects > Work
- Scroll down to the Custom Fields & Relationships section
- Click the Status link in the Field Label column
- Scroll down to the Picklist Values section
- Click New
- Add the name of the new Work Status to the text area
- Select the Work Types that will be associated with the new Work Status
- Save

### Add New Column
Agile Accelerator Column objects are what informs the columns on the Kanban board. Unlike Work Status objects, Columns are assigned to Teams. This allows you to create team-specific Kanban statuses.

- Go to the Column tab
- Click New
- Enter Column Name
- Enter the Team that will be associated with the Column
- Enter 0 for Position
- Enter 0 for Level
- Leave Max # Records blank
- Leave Parent Column blank
- Save

### Add Column Status Assignment 
To assign a Column to a Work Status, you must create a new Column Status Assignment. This will allow you to map a Work Status to a Column on the Kanban board.

- Go to the Column Status Assignment tab
- Click New
- Search for the Column Name you would like to use. Make sure that it is associated with the correct team.
- Search for the Work Status that will be associated with the Column
- Save
- 

### Update Kanban Columns
- Navigate to the Kanban board for the selected team
- Click Settings
- Click any of the columns listed in the modal window and then click Update/Remove
- Select the new Column is from the Status Mapping field list

