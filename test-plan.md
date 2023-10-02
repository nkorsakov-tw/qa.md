# Test Plan unTill Air

----------------

## Rules for Testers

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
   When reporting an error, provide a detailed description. Include all essential steps taken, so that the issue can be easily understood and replicated.

9. **Stay in Touch with the Development Team**:  
   Keep track of the tasks you've set. Stay updated on their status, respond promptly to queries or requests from the development team, and don't forget to close tasks that have been resolved.

10. **Add tasks in the Feedback sections:** If you have any kind of suggestions (you should have them), create the tasks in the Feedback generously.


## Scope

You need to test services of unTill Air (Back Office and POS) on two environments (DEV cluster and TEST cluster) and two platforms (IOS and Android).

## Objective

We must highlight the possible errors, bugs etc. before going live. Our aim is to prevent collapses. We work to gurantee the high quality of the Products which we  provide to our customers.

## Resources

## Test cases

### POS Action sets

- Navigate to POS Actions sets
- Modify the actual Action sets (add, remove, replace etc.)
- Check the sequence and correctness of Action sets in the POS

### Restaurant settings

- Navigate to Restaurant settings
- Set the start time
- Open POS
- Make an X Report
- The time of X Report must be as it was set in the BO
- Set the log-off
- Open POS
- The log-off must work
- (???)
- Turn on/of availability of courses
- Check that courses are appeared/disappeared form the sections withing the Back Office
- Open POS 
- Check that courses buttons are appeared/disappeared

### POS Users

- Click 'Add new user'
- Miss some 'General' information fields and try to proceed. The system should not allow to do so
- Tick the checkbox 'Allow void' and 'Allow transfer'.
- Test that 'Allow void' and 'Allow transfer' work correctly in the POS.
- Set the user's language.
- Verify the language in the POS.
- Enter the additional information.
- Click 'Save'
- Edit an existing POS User.
- Verify that all works as expected in accordance with the previous steps.

### Reports

- Create orders with discounts, voids, by different payment methods.
- Make a Z Report and an X Report.
- Switch from one report to another in the Back Office and verify the values, numbers, and items included in these reports.


## Scenarious

### Exceed the limits

- Try to test the restrictions of system which can be unconsidered from the developer's side. The error might appear in the case when you make something unusual. 

**Example:**

Create 20 discounts and observe how it will work in the POS. Would the discounts available, how they will be placed in the discount list?
Assign 10 modifiers for one article to check 
