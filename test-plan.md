# Test Plan (unTill Air)

----------------

## Principles

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

We must highlight the possible errors, bugs etc. before going live. Our aim is to prevent collapses. We work to gurantee the high quality of the Products which we provide to our customers.

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
- Set various option categories. Trace the changes in how it is displayed.
- Add items
    + Add article: choose several articles and then check their availability in the POS.
    + Add text item: enter the text and then check its availability in the POS.
- Assign to articles and verify in the POS.
- Assign to departments and verify in the POS.
- Try various types of modifiers (Optional and Mandatory). Check that they are applied in accordance with its essense.
- Try to delet an existing modifier.
- Try to modify an existing modifier.
- Try to duplicate an existing modifier.
- Check the columns. 

### Menus

- Click 'Add New Menu'.
- When assigning to a department, make sure all departments are listed.
- Verify that the menu is automatically assigned to current spaces.
- Assign to a preparation printer. If you have a printer to issue a ticket, test it in the POS. 
- Click 'New Item Group'.
- Select a course, then verify that the menu item is correctly assigned to it and functions as expected when you click the 'Fire Next Course' button.
- Check the 'Allow to Skip' checkbox, then verify its functionality in the POS.
- Add articles.
- Add additional item groups and verify their display in the POS.
- Try to delet an existing menu.
- Try to modify an existing menu.
- Try to duplicate an existing menu.
- Check the columns. 

### Combi deal

- Click 'Add new combi deal'.
- Assign new combi deal to department, make sure all departments are presented here.
- Tick the checkbox 'Suggest missing articles...' and ensure that the prompts with combi deal suggestions appear accordingly.
- Further, leave this checkbox unticked and verify in the POS that waiters do not receive any prompts.
- Verify that the combi deal is automatically assigned to current spaces.
- Assign to a preparation printer. If you have a printer to issue a ticket, test it in the POS. 
- Add items.
- Assign articles.
- Set POS Display sequence and then check it in the POS.
- Try to delet an existing menu.
- Try to modify an existing menu.
- Try to duplicate an existing menu.
- Check the columns.

### Courses

- Click 'Add new course'.
- Change the course number to enhance that new course can be assigned to non-occupied by other courses number.
- Tick and untick the checkbox 'Changeable' and then verify how it works in the POS.
- Pick colour for new course. Check this colour in the POS.
- Try to delet an existing course.
- Try to modify an existing course.
- Try to duplicate an existing course.
- Check the columns.

### Categories

- Click 'Add new category'.
- Make sure that you are able to preserve a new category.
- Try to delet an existing category.
- Try to modify an existing category.
- Try to duplicate an existing category.
- Check the columns.

### Groups

- Click 'Add new group'.
- Make sure appropriate categories are displayed in the selector.
- Select VAT level. Then check in the POS that items from this group will be sold with correct VAT level that was indicated in the group section. 
- Add secondary VAT. It should be available in the spaces which support secondary VAT. The check it in the POS.
- Check the columns, each column should display the concerning values such as VAT, secondary VAT, and category.
- When you have previously set up a secondary VAT, click on the 'Hide secondary VAT' to ensure that the reverse can be performed.
- Try to delete an existing group.
- Try to modify an existing group.
- Try to duplicate an existing group.

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
- Check the values.
- Switch between different timeframes and observe how the data changes.
- Create new orders and trace how the data changes.
- Export this report and open this in different formats such as PDF.
- Verify that the exported report matches with the report displayed in the Back Office.

#### Financial

- Open the Financil Report
- Check the values.
- Switch between different timeframes and observe how the data changes.
- Create new orders and trace how the data changes. 
- Export this report and open this in different formats such as PDF.
- Verify that the exported report matches with the report displayed in the Back Office.

#### Discounts

- Open the Discounts Report.
- Check the values. 
- Check the empty fields if you see them, it can be an error.
- Switch between timeframes and observe the changes.
- Create new orders and trace how the data changes. 
- Export this report and open this in different formats such as PDF.
- Verify that the exported report matches with the report displayed in the Back Office.

### POS Action sets

- Navigate to POS Actions sets.
- Modify the actual Action sets (add, remove, replace etc.)
- Check the sequence and correctness of Action sets in the POS.

### Company settings

- Verify that the user can modify any information EXCEPT the 'VAT number'.

### Restaurant settings

- Navigate to Restaurant Settings.
- Set the start time.
- Open POS.
- Generate an X Report.
- Verify that the time on the X Report matches the time set in the Back Office.
- Configure the log-off settings.
- Open POS.
- Verify that the log-off feature works as expected.
- (???)
- Turn on/off the availability of courses.
- Verify that courses appear/disappear from the sections within the Back Office.
- Open POS.
- Check that course buttons appear/disappear as expected.

### unTill Payments

- Click 'Request access to unTill Payments' and verify that the request is sent. If you have an access to the Reseller Portal check that the email with this request should be received by the Reseller.
- Configure unTill Payments using UP Credentials from the Payments Portal to make sure it works as expected.


### POS Users

- Click 'Add new user'.
- Leave some 'General' information fields blank and try to proceed. The system should prevent you from doing so.
- Tick the checkbox 'Allow void' and 'Allow transfer'.
- Verify that the 'Allow void' and 'Allow transfer' settings are functional within the POS.
- Set the user's language.
- Verify the language in the POS.
- Enter the additional information.
- Click 'Save'.
- Edit an existing POS User.
- Verify that everything works as expected, consistent with the previous steps.
- Open POS, verify that newly created POS User can enter to the application.

### Need Help?

- Verify that all links to the Documentation pages are available.
- Verify that the link to the website of unTill (untill.com).

### Logout

- Verify that the user can perform the logout and sign in.

### My profile

- Verify that the changing the personal information about Location Owner is prohibited.
- Verify the capability to change the password.
- Click 'Add new location' and go through the entire process of the arranging the subscription.
- Check the dates for next payments.
- Verify the ability to renew the subscription.
- Verify the price when rise up the quantity of screens.
- Verify the ability to cancel an existing subscription.

### Languages

- Switch between several languages and check that the translations are displayed.

### Switch between locations

- Create several locations within the one account and switch between them.
- Verify that there are no strange artefacts, that the locations cannot influence on each other. 

## Test cases (POS)

### Ordering process

- Open POS application.
- Connect your tablet with the location. Check that the connection works as expected.
- Enter the personal password for specific POS User. Verify its uniqueness and the capability to enter the POS using these credentials.
- At first try to place an order in the POS.
- Make a more complex order using optional and mandatory modifiers, repeated articles etc.
- Order an article:
    + Click 'Repeat' and verify that the article was duplicated.
    + Click 'Void' and verify that the article was removed from the order list.
    + Click 'Undo' option and verify that the last action was unrolled.
    + Click 'Message' and ensure that the user is able to add an article message to the article.
    + Click 'Change course' and verify that the course can be changed if you have several courses and one course is assigned to this specific item.
- Order an article with a modifier (optional and mandatory; paid and free).
    + Click 'Free addon' and verify that the button works.
    + Click 'Paid addon' and verify that the button works.
    + Click 'Optional modifier' and verify that all optional modifiers appeared in the designated column.
    + Verify that the mandatory modifiers are inevitable to order and if you have several mandatory modifiers the corresponding pop-up appears.  
- Use a void button after the first confirming of the order.
- Try to search a specific article in the search line.
- Order article - click on the '-' and '+' buttons. Check that it works.
- Order article - click on the button with 'trash' sign. Check that the article was deleted.
- Enter the quantity on the calculation bar and click on the article - exactly the indicated quantity of the article must be added to an order. Check it.
- Verify that the 'Cancel' button works and you are able to exit an order list.
- Switch to 'Table info' and verify that the display name of the waiter, article course, current course, and table number are correct.

### Actions

- Click on the 'Fire next course' button and verify that the current ciurse was changed on this table.
- Open 'Table colour legend' and compare the colours in the space with colours presented in the legend. Make sure that they are matched.
- Click 'Transfer table'.
    + Transfer whole bill.
    + Transfer by item.
    + Verify that button 'Undo' works as expected.
- Configure the list by item to transfer and then cancel it using the red button.
- Order some articles and click 'Checkout' and then add tips to this order.
- Click 'Reset tips' and check that this button works as expected.
- Tips that were set by user should disappear from the order when you opt to make a split. Check that it works like this.
- Order some articles and make a split.
    + Make a split in equal parts.
    + Enter the quantity of parts.
    + Enter the fractional quantity of parts and verify that the system prevents such kind of actions.
    + Check the values after the splitting.
    + Pay the bills in turn.
    + Verify that after the each acceptance of the payment - the bill ticket is issued.  
    + Check the ability to add tips for each separate bill.
    + Click 'Reset tips' and verify that you are able to reset tips in the separate bill.
    + Make a split by item.
    + Verify that you are able to complect the bills by tapping on the articles.
    + Verify that you are able to split repeated articles by using the calculation bar. For information on how you can do so, [refer to this page](https://help.air.untill.com/features/pos/split-the-order).
    + Configure the conditions of splitting and then tap on the 'Reverse split' button. Check that pop-up with the quantity of parts appears and the splitting conditions are changed accordingly.
    + 





  


## Scenarious

### Edge cases

- Try to test the restrictions of system which can be unconsidered from the developer's side. The error might appear in the case when you make something unusual. 

**Example:**

Create 20 discounts and observe how it will work in the POS. Would the discounts available, how they will be placed in the discount list?
Assign 10 modifiers for one article to check 
On the page of the subscriptions, select more than 100 screens. Check which price would be displayed.
