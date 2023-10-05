# Test Plan (unTill Air)

----------------

## 10 Principles

1. **Always Create a Task**:  
   If you encounter a potential error, don't hesitate to create a task. If in doubt, consult the development team for clarification, but generally, a task should be created for every issue you encounter.

2. **Follow Test Plans**:  
   Strictly adhere to the test plan and test cases. But...

3. **Be Creative**:  
   Don't limit yourself to these guidelines; feel free to deviate sometimes from the plan's clauses if it might help uncover issues.

4. **Don't Avoid Rare Scenarios**:  
   Even if an action seems unusual, aim to cover all possible situations. For example, why not try ordering 100 items to see what happens?

5. **Be Skeptical**:  
   Always question the system's behavior and functionality. Approach it like an end-user and try to identify weaknesses.

6. **Be Detail-Oriented**:  
   Pay attention to minor details, as they can sometimes indicate more significant underlying problems.

7. **Verify Fixes**:  
   Never approve a task without re-testing functionalities that have been updated or fixed to ensure they now work as expected.

8. **Comprehensive Descriptions**:  
   When reporting an error, provide a detailed description. Include all essential steps taken, so that the issue can be easily understood and reproduced. If you understand that there is the need in screenshots for visual representation, take them and attach to the task.

9. **Stay in Touch with the Development Team**:  
   Keep track of the tasks you've set. Stay updated on their status, respond promptly to queries or requests from the development team, and don't forget to close tasks that have been resolved.

10. **Add tasks in the Feedback sections:** If you have any kind of suggestions (you should have them), create the tasks in the Feedback generously (But in general do not set an assignee).


## Scope

You need to test services of unTill Air (Back Office and POS) on two environments (DEV cluster and TEST cluster) and two platforms (IOS and Android).

## Objective

1. We must detect the possible errors, bugs etc. before going live. Our aim is to prevent system failures. We work to gurantee the high quality of the Products which we provide to our customers.

2. Additionally, our aim is to suggest significant improvements to the development team to enhance the overall experience for our end clients. Don't approach the product solely as a tester; instead, use it as an end-user would. Identify features or actions that are complicated or non-intuitive. 

So, under these two main objectives, you should:

- Ensuring availability of all features.
- Verifying the accuracy of the reports including its values.

## Structure

The structure of this Test Plan mainly is divided into two parts: "Test cases" and "Scenarious". 

- The "Test cases" assume that you need from time to time ensure that the system works as expected and we have no serious issues in our software. So, all common operations in the Back Office and POS should be covered by following these described steps. 

- The "Scenarious" section assumes that the tester composes some rare scenarious to prevent the appearance of the issues, questions, bags which should be then resolved and explained. Based on some scenarious which sometimes help to find the mistake, you can try various approaches to detect an error which isn't obvious and eye-catching. 

The good example of such kind of scenario is the ["Edge case"](https://en.wikipedia.org/wiki/Edge_case). The essence of this scenario consists in the approach to the testing when you touch the extreme values of the parametres. This approach can be really effective to find the sections in the software product where the objective limits and restrictions take a place but didn't established in the product. This circumstance can be a potencial trouble for clients.  

## Test cases (Back Office)

### Home page

- Create orders with discounts and voids.
- Open the Home page.
- Verify that all tiles display numbers.
- Switch between different timeframes and observe how the data changes.
- Check if the values are realistic, including comparisons between various periods.

### Spaces

- Click 'Add new space'.
- Verify that all features (Use special price & Use secondary VAT) are available.
- Ensure you cannot enter an already existing table number in the 'Start from' field. The system should prevent this.
- Tick the 'Use special price' checkbox and verify that the option to set prices appears in the articles section.
- Click 'Edit space' and verify that all features are still available.
- Verify that you can rename the space.
- Click 'Modify table plan' and try to rearrange the tables, delete tables, and add new ones.
- Add visual elements and change the background.
- Try zooming in and out of the space.
- Activate the grid and move tables using it.
- Click on a table to check that you can change its settings.
- Change the table's size and try duplicating tables.
- Click the 'Undo' button and verify its functionality.
- Test the 'Restore' button and other buttons on the interface.
- Click 'Cancel' to verify that you can discard changes.
- Make changes again and click 'Save' to ensure they are preserved.
- Switch between spaces and verify that a warning appears if you have unsaved changes.
- Try deleting a space.
- Open the POS to verify that the new space is available. Compare it with the modified Table Plan in the Back Office.

### Payment methods

- Click 'Add new payment method'.
- Verify that numbers unoccupied by other payment methods are available.
- Choose different types of payments and verify that all corresponding scrollbars are appropriate.
- Modify, delete, duplicate, and search for payment methods.

### VAT levels

- Verify the default VAT levels are present.
- Click 'Add new VAT' and check that unoccupied VAT level letters are available.
- Try setting the VAT value to more than 100%. The system should prevent this.
- Modify, delete, and duplicate VAT levels.


### Equipment

#### Add a Printer
- Set up different purposes for the printer.
- Configure various types of order tickets.
- Provide the printer's technical specifications.
- Save these changes.
- Modify the settings as needed.
- Test by ticking the 'Null Printer' checkbox. Will it work?

#### Add a Terminal
- Provide a name for the terminal.
- Add a POIID.

#### Add a Tablet

- Attempt to connect the device in two modes: 'Direct Sales' and 'Table Overview'.
   + **Direct Sales**: Verify that all spaces are listed in the scroll bar; confirm that all bill printers appear in the scroll bar.
   + **Table Overview**: Confirm that all bill printers are visible in the scroll bar.
- Validate the data and ensure the correctness of the bill printers.
- Open the application on the tablet. Compare the layout with the information set in the Back Office, such as the placement of tables and decor elements configured in the Table Plan editor. Check for consistency between the settings configured in the Back Office and how they are displayed in the POS.

### Article messages

- Click 'Add new message'.
- Try to leave the text field blank. The system must prevent this action.
- Try to modify an existing article message.
- Try to delete an existing article message.
- Try to duplicate an existing article message.
- Open POS, verify that newly created article message is appeared.
- Use the appeared article message in the POS. Any problems?

### Discounts

- Click 'Add new discount'.
- Change value types and ensure that they correctly influence the discount value.
- Select a discount type and verify that it can be correctly applied in the POS.
- Choose an excluded period and verify that the discount is unavailable during this timeframe.
- Apply the discount to specific departments, courses, or groups and then verify that it is only available for the corresponding articles.
- Experiment with different options for reasons:
    + Choose the 'Fixed text' type, enter text, and then verify that the discount is applied with this reason.
    + Choose the 'Ask reason' type, select one of the created reasons, and then verify that the discount is applied with this reason.
- Attempt to delete an existing discount.
    + Click 'Undo' to ensure that the reverse function is also available.
- Modify an existing discount.
- Duplicate an existing discount.
- Review the values.
- Search for a specific discount on this page.
- Open the POS and verify that the discount is available and all its conditions are considered.


### Periods

- Click 'Add new period'.
- Create periods of various types (Weekly values, One-time use values, Annual values, Daily values).
- Create multiple periods and then verify that they are applicable for discounts.
- Try to modify an existing period.
- Try to delete an existing period.
- Especially, pay attention to dates, here the erorrs can be.
- Open POS, verify that these periods are available accordingly.

### Reasons

- Click add new reason.
- Choose different reason types and verify how it works in the POS.
- Try to delete an existing reason.
- Try to modify an existing reason.
- Try to search specific reasons.

### Tickets

- Click 'Add new ticket'.
- Choose ticket layout.
- Modify the width.
- Add image, verify that the image is displayed on the ticket template.
- Enter bottom text, verify that the text currently is presented.
- Make an order, print the ticket (if you can) and compare this printed ticket with template.
- Change some settings in the ticket templates and trace the results.

### Articles

- Click 'Add new article'.
- Try to assign various numbers for new article. Numbers occupied by other articles shouldn't be available.
- Set a negative price. System should prevent this kind of action.
- Assign to preparation printer. Verify that all preparation printers are available.
- Pay attention to assigned spaces. When you create an article, it should be automatically assigned to all current spaces in the location. Check it.
- Verify that all courses are available in the scrollbar.
- Pick colour. Then check that exactly this colour is presented in the POS.
- Add article barcodes. Check its availability.
- Add various modifiers (Mandatory and Optional).
- Open POS and check that the modifiers are applicable to this article.
- Set POS Display sequence and then check it in the POS application.
- Check the overall values on the page of articles such as quantity of spaces or assigned department.
- Switch to each department, check it and set POS Display sequence, then check it in the POS.
- Try to delete an article.
- Try to modify an article.
- Try to duplicate an article.
- Try to search a specific article.
- If you have some articles with special price, this price for a specific space should be displayed. Verify it.
- Click to test sorting within the articles page.

### Departments

- Click 'Add new department'.
- Select group, and then check that department is used with a right group therefore department is used with a right VAT level.
- Verify that existing spaces are assigned to the department automatically.
- Create special articles. They must be shown in different departments (in a native department and in the department where you work now). Check this.
- Set POS Display sequence for spesial articles. Verify that all works as expected in the POS.
- Try to delete an existing department.
- Try to modify an existing department.
- Try to duplicate an existing department.
- Set POS Display sequence.
- Check that the column 'Group' isn't empty. All departments must be assigned to a specific group.

### Modifiers

- Click 'Add new modifier'.
- Set various option categories and observe how they are displayed.
- Add items:
    + Add article: Select multiple articles and then verify their availability in the POS.
    + Add text item: Input text and then verify its availability in the POS.
- Assign to articles and confirm in the POS.
- Assign to departments and confirm in the POS.
- Experiment with various types of modifiers (Optional and Mandatory). Ensure they are applied correctly.
- Attempt to delete an existing modifier.
- Attempt to modify an existing modifier.
- Attempt to duplicate an existing modifier.
- Examine the columns.

### Menus

- Click 'Add New Menu'.
- Assign to a department, ensuring all departments are listed.
- Verify that the menu is automatically assigned to current spaces.
- Assign to a preparation printer and test in the POS if possible.
- Click 'New Item Group'.
- Select a course and confirm that the menu item is correctly assigned and functions as expected when clicking 'Fire Next Course'.
- Check 'Allow to Skip' and confirm its functionality in the POS.
- Add articles.
- Add additional item groups and verify their display in the POS.
- Attempt to delete an existing menu.
- Attempt to modify an existing menu.
- Attempt to duplicate an existing menu.
- Examine the columns.

### Combi Deal

- Click 'Add new combi deal'.
- Assign to a department, ensuring all departments are listed.
- Tick 'Suggest missing articles...' and verify that combi deal suggestions appear in the POS.
- Untick this checkbox and verify that no prompts appear in the POS.
- Verify that the combi deal is automatically assigned to current spaces.
- Assign to a preparation printer and test in the POS if possible.
- Add items and assign articles.
- Set POS Display sequence and verify in the POS.
- Attempt to delete an existing menu.
- Attempt to modify an existing menu.
- Attempt to duplicate an existing menu.
- Examine the columns.

### Courses

- Click 'Add new course'.
- Change the course number to ensure it can be assigned a unique number.
- Toggle 'Changeable' on and off, then confirm its functionality in the POS.
- Choose a color for the new course and verify it in the POS.
- Attempt to delete an existing course.
- Attempt to modify an existing course.
- Attempt to duplicate an existing course.
- Examine the columns.

### Categories

- Click 'Add new category'.
- Ensure you can save the new category.
- Attempt to delete an existing category.
- Attempt to modify an existing category.
- Attempt to duplicate an existing category.
- Examine the columns.

### Groups

- Click 'Add new group'.
- Ensure relevant categories appear in the selector.
- Select a VAT level and verify in the POS that items from this group are sold at the indicated VAT level.
- Add secondary VAT and verify its availability in spaces that support it, then confirm in the POS.
- Examine each column for relevant values such as VAT, secondary VAT, and category.
- If secondary VAT has been set, click 'Hide secondary VAT' to ensure it can be removed.
- Attempt to delete an existing group.
- Attempt to modify an existing group.
- Attempt to duplicate an existing group.


### Reports

#### Z-X Report

- Create orders with discounts, voids, by different payment methods.
- Make a Z Report and an X Report.
- Switch from one report to another in the Back Office and verify the values, numbers, and items included in these reports.
- Create orders featuring 'Modifiers,' bill splitting, tips, discounts, menus, combi deals, and special articles.
- Create orders in different spaces, utilising various VAT levels for the same article via the 'Secondary VAT' feature.
- Generate a Z-X Report for the period covering these orders.

  Note: The Z Report should have a preconfigured start date that cannot be modified, as it must cover all sales from the time of the last Z Report. Verify this.

  Note: If you have set the Work Start Time in Back Office settings, the X Report will be scheduled to start from this time. Confirm this.

- Open the Z-X Report.
- Ensure that Turnover matches Payments.
- Open the VAT calculator (e.g. [this one](https://badrequest.ru/vat_calculator/)) and validate the VAT values in this Z-X Report.
- Confirm the numbers related to turnover, both by waiter and by payment method.
- Verify that VAT for 'Modifiers' is calculated based on the groups to which the modifier articles belong, not the groups of the articles that include these modifiers.
- Ensure that articles with secondary VAT are categorized correctly, with the appropriate VAT level.
- Confirm that special articles are placed in the correct group with the corresponding VAT level. Note: Special articles should be assigned to the "native department" that was first associated with the article.
- Review other values, such as VAT deductions, for accuracy.


#### Location Report

- Open the Location Report.
- Ensure that Turnover matches Payments.
- Open the VAT calculator and validate the VAT values in this Location Report.
- Confirm the numbers related to turnover, both by waiter and by payment method.
- Review other values, such as VAT deductions, for accuracy.

#### Waiters

- Open the Waiter Report.
- Select a specific waiter and ensure that the data displayed relates specifically to the selected waiter.
- Pay attention to the displayed name of the waiter. The system should use the 'Display Name' in this instance.
- Review the values in this Report.
- Create orders using the waiter whose report you are viewing, and then recheck the values in the Report.
- Export this report and open it in different formats, such as PDF.
- Verify that the exported report matches the report displayed in the Back Office.


#### Sales per waiter

- Open the Sales per waiter report.
- Check that the values are sorted by the waiters and payment types.
- Switch between the dates and observe how the data changes.
- Create orders and trace how the data changes.
- Export this report and open this in different formats such as PDF.
- Verify that the exported report matches with the report displayed in the Back Office.

#### Voids

- Open the Voids Report.
- Check all properties. If you have no properties in the specific field it's an error.
- Check the Total amounts figures.
- Check the reasons.
- Create new orders with voids and trace how the data changes.
- Export this report and open this in different formats such as PDF.
- Verify that the exported report matches with the report displayed in the Back Office.

#### Sold articles

- Open the Sold articles Report.
- Check the values.
- Switch between different timeframes and observe how the data changes.
- Create new orders and trace how the data changes.
- Export this report and open this in different formats such as PDF.
- Verify that the exported report matches with the report displayed in the Back Office.

#### Sales per hour

- Open the Sales per hour Report.
- Check the values.
- Switch between different timeframes and observe how the data changes.
- Create new orders and trace how the data changes.
- Export this report and open this in different formats such as PDF.
- Verify that the exported report matches with the report displayed in the Back Office.

#### Sales per category

- Check the values.
- Switch between different timeframes and observe how the data changes.
- Create new orders and trace how the data changes.
- Export this report and open this in different formats such as PDF.
- Verify that the exported report matches with the report displayed in the Back Office.

#### Payments

- Open the Payments Report.
- Verify the values.
- Switch between different timeframes and observe any changes in the data.
- Create new orders and track how the data updates.
- Export the report and open it in various formats, such as PDF.
- Confirm that the exported report matches the one displayed in the Back Office.

#### Financial

- Open the Financial Report.
- Verify the values.
- Switch between different timeframes and observe any changes in the data.
- Create new orders and track how the data updates.
- Export the report and open it in various formats, such as PDF.
- Confirm that the exported report matches the one displayed in the Back Office.

#### Discounts

- Open the Discounts Report.
- Verify the values.
- Inspect any empty fields; these could indicate an error.
- Switch between timeframes and observe any changes.
- Create new orders and track how the data updates.
- Export the report and open it in various formats, such as PDF.
- Confirm that the exported report matches the one displayed in the Back Office.

### POS Action Sets

- Navigate to POS Action Sets.
- Modify the existing Action Sets (add, remove, replace, etc.).
- Verify the sequence and accuracy of the Action Sets in the POS.

### Company Settings

- Verify that the user can modify any information EXCEPT the 'VAT number'.

### Restaurant Settings

- Navigate to Restaurant Settings.
- Set the start time.
- Open the POS.
- Generate an X Report.
- Confirm that the time on the X Report aligns with the time set in the Back Office.
- Configure the log-off settings.
- Open the POS and verify that the log-off feature operates as expected.
- Toggle the availability of courses on/off.
- Confirm that courses appear or disappear from the sections in the Back Office.
- Open the POS and verify that the course buttons appear or disappear as configured.


### unTill Payments

- Click 'Request access to unTill Payments' and verify the request is sent. If you have access to the Reseller Portal, ensure the email request is received by the Reseller.
- Configure unTill Payments using UP Credentials from the Payments Portal to ensure it functions as expected.

### POS Users

- Click 'Add new user'.
- Leave some 'General' information fields blank and attempt to proceed. The system should prevent you from doing so.
- Tick the checkboxes for 'Allow void' and 'Allow transfer'.
- Verify that the 'Allow void' and 'Allow transfer' settings work in the POS.
- Set the user's language and verify it in the POS.
- Edit an existing POS User and verify functionality, consistent with previous steps.
- Open the POS and verify that the newly created POS User can access the application.

### Need Help?

- Ensure all links to Documentation pages are functional.
- Verify the link to unTill's website (untill.com) is functional.

### Logout

- Verify the user can log out and sign back in.

### My Profile

- Verify that changing personal information about the Location Owner is prohibited.
- Test the ability to change the password.
- Click 'Add new location' and complete the entire subscription arrangement process.
- Check the dates for the next payments.
- Verify the ability to renew the subscription.
- Confirm the price changes when increasing the number of screens.
- Verify the ability to cancel an existing subscription.

### Languages

- Switch between multiple languages and verify that translations are displayed correctly.

### Switch Between Locations

- Create multiple locations within a single account and switch between them.
- Verify that no strange artifacts appear and that locations do not influence each other.


## Test cases (POS)

### Ordering process

- Open the POS application.
- Connect your tablet to the location. Ensure the connection works as expected.
- Enter a unique personal password for a specific POS User. Verify that you can access the POS using these credentials. Verify its uniqueness.
- Attempt to place a basic order in the POS.
- Place a more complex order involving optional and mandatory modifiers, repeated articles, etc.
- To order an article:
    + Click 'Repeat' and ensure the article is duplicated.
    + Click 'Void' and ensure the article is removed from the order list.
    + Click 'Undo' and confirm that the last action is reversed.
    + Click 'Message' and verify you can add a message to the article.
    + Click 'Change course' and ensure the course can be changed if the item is assigned to one specific course.
- To order an article with modifiers (optional and mandatory; paid and free):
    + Click 'Free addon' and ensure it functions properly.
    + Click 'Paid addon' and ensure it functions properly.
    + Click 'Optional modifier' and verify all optional modifiers appear in the designated column.
    + Confirm that mandatory modifiers are required to proceed with the order. If multiple mandatory modifiers exist, a corresponding pop-up should appear.
- Use the 'Void' button after confirming the order for the first time.
- Search for a specific article using the search bar.
- To order an article:
    + Click the '-' and '+' buttons and verify they function correctly.
    + Click the 'trash' icon and ensure the article is deleted.
- Enter a quantity in the calculation bar and click the article. Verify the specified quantity is added to the order.
- Verify the 'Cancel' button functions correctly and allows you to exit the order list.
- Switch to 'Table info' and confirm that the waiter's display name, article course, current course, and table number are all correct.


### Actions

- Click on the 'Fire next course' button and verify that the current course has changed for this table.
- Open the 'Table color legend' and compare the colours in the space to those presented in the legend. Ensure they match.
- Click 'Transfer table'.
    + Transfer the whole bill.
    + Transfer by item.
    + Verify that the 'Undo' button functions as expected.
- Configure the list of items to transfer and then cancel it using the red button.
- Order some articles, click 'Checkout,' and add tips to this order.
- Click 'Reset tips' and check that this button works as expected.
- Tips that were set by the user should disappear from the order when you opt to split it. Verify this functionality.
- Order some articles and initiate a split.
    + Split the bill into equal parts.
    + Enter the number of parts.
    + Enter a fractional number of parts and verify that the system prevents such actions.
    + Check the values after splitting.
    + Pay the bills in turn.
    + Verify that after each payment is accepted, a bill ticket is issued.
    + Test the ability to add tips to each separate bill.
    + Click 'Reset tips' and verify that you can reset tips on a separate bill.
    + Split by item.
    + Confirm that you can combine the bills by selecting the articles.
    + Verify that you can split repeated articles using the calculation bar. For information on how to do so, [refer to this page](https://help.air.untill.com/features/pos/split-the-order).
    + Configure the splitting conditions and then click on the 'Reverse split' button. Verify that a pop-up with the number of parts appears and the splitting conditions are updated accordingly.

### Reports

- In the POS, navigate to 'Reports' section.
- Click 'Z Report', verify that the date 'From' is set automatically and equals the time of the last Z report.
- Try to set the date and time 'Till' of the day that is just coming up. The system should prevent such actions. 
- Click 'X Report', verify that the date 'From' is free to manage. X Reports have no date limits. 
- Check the values.
- Click the red button to cancel the report. Check that it works as expected.
- Try to make several reports.

### Logout

- Make a logout and enter new credentials to ensure that it works as expected.

## Scenarious

### Edge cases

- Try to test the restrictions of system which can be unconsidered from the developer's side. The error might appear in the case when you make something unusual. 

**Example:**

Create 20 discounts and observe how it will work in the POS. Would the discounts available, how they will be placed in the discount list?
Assign 10 modifiers for one article to check 
On the page of the subscriptions, select more than 100 screens. Check which price would be displayed.
