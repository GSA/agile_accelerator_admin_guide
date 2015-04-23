# Admininstrators Guide to Agile Accelerator
Below are supplemental instructions for customizing an installation of Salesforce's Agile Accelerator. 

- [Add Work Type to Work Status Detail Page]               (#add-work-type-to-work-status-detail-page)
- [Add Tabs for Other AA Objects]                          (#add-tabs-for-other-aa-objects)
- [Updating Kanban Board to Relfect Work Status]           (#updateing-kanban-board-to-reflect-work-status)


## Add Work Type to Work Status Detail Page
Agile Accelerator associates Work Types (Bug, User Story, etc) to specific Work Statuses. However, using a fresh installation, it can be difficult to determine which Work Types are associated to specific Work Statuses. The steps below walk through the process of updating the page layout for Work Status to display the Work Type relationship.

- Navigate to Setup
- From Setup go to Create > Objects > Work Status
- On the Work Status Custom Object Definition Detail Page, scroll to the Page Layouts section
- Click Edit on the Status Layout
- Drag the Type field into the Status Detail layout
- Save

## Add Tabs for Other AA Objects
Out of the box, Agile Accelerator does not create tabs for a number of objects that are important when customizing the installation. To make updates to the available Work Statuses or the Kanban board, the following objects will have to be customized: Work Status, Column, and Column Status Assignment. 

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

## Updating Kanban Board to Relfect Work Status
Coming soon
