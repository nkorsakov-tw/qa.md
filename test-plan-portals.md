# Test Plan

## Abstract

This document is written to provide guidelines that testers must adhere to in order to systematically optimise the testing of the Payments Portal and the Reseller Portal. This document contains the descriptions of basic approaches in testing that can help you to find the potential error quite more efficient.  

## Introduction

The creation of the document is motivated by [Increase Test Coverage Issue](https://dev.untill.com/projects/#!659377).

### Objectives

1. We must eliminate potential errors before going live. Therefore, the QA team should make efforts to alert the development team about areas at risk for errors.
2. We should provide not only error reports to the development team but also feedback. View the product as an end-user and recommend specific improvements to the development team.

### Scope

You must test the Portals on two environments (TEST cluster and DEV cluster) and two platforms (IoS and Android).

### Structure

This Test Plan has a separate structure that included two main sections: "Test cases" and "Edge cases".

- "Test cases" are designed to cover common situations encountered while using the Portals. Testers must follow all guidelines and recommendations to ensure that the system works correctly. The "Test cases" serve as a way to detect and resolve primarily issues corresponding with the basic features. Here we need make sure that all elements work as expected.
- "Edge cases" are designated to test the rare and comlex scenarios which are not come to the mind first while you working with the Portals. In the Test Plan, the approaches and examples of the "Edge cases" are presented but you do not need to follow these options like guidelines, you should keep it in your mind and impress it to make something similar and reach an error in the system.

### Principles

Please refer to the [Test Plan for unTill Air](https://docs.google.com/document/d/1JH1KWSJ1TzXFBp-H8c3hTkOsUP_n_cNefsJWcl0mQuA/edit?usp=sharing) that contains the principles and read them.

## Test Cases (Reseller Portal)

### Invitation Process

- Ask a unTill representative with Reseller Admin rights to invite you to the Reseller Portal as either an Air Reseller or Payments Reseller.
- Verify that you've received an email invitation to the Portal, designating you as an Air Reseller.
- Click on the link provided in the email and confirm that it directs you to the correct page (reseller.dev.air.untill.com).
- Make sure the page opens without significant delay and that you can enter the Portal.
- Attempt to initiate processes like inviting a user or switching between sections. The system should prevent these actions.
- The system should then redirect you to the 'Subscription Profile'.
- Unless you complete the 'Subscription Profile,' access to other sections related to Air subscriptions should be restricted.
- Test the same for the Payments Profile. Until you complete this profile, you should be restricted from accessing other unTill Payments-related sections, such as Payments Locations and Payouts.

### Subscriptions

- Switch to the 'Subscriptions' tab and review all titles, headings, and the interface.
- Click on 'Invite User'.
- A unique link to unTill Air should appear immediately.
- Use the provided tool to copy this link.
- Paste this link somewhere and click on it. Verify that it directs you to the unTill Air sign-up page.
- Create an account using this link and subscribe to the location.
- Return to the Reseller Portal.
- Visit the 'Subscription' section and ensure that all data for the user who recently arranged a subscription is correct and all fields are filled in.
- Return to the 'Subscription Profile' and verify that you can modify and add information, as well as remove information (except for the email address).

### Account

If you have a role as Payments Reseller, you can test other sections of the Reseller Portal such as 'Account'.

- Navigate to 'Account'. Review the provided data and check for its accuracy.
- Set different timeframes and monitor how the data changes.
- If you have access to execute payouts, test how this feature reflects in the 'Account' section.
 
### Payments Locations

- Navigate to 'Payments Locations'.
- Click 'Add location'.
- Switch between timezones. Ensure that you can do this.
- When entering the email, you should be prompted for its validity if necessary.
- Set different processing fees and acquirer fees.
- Add another email and confirm that it attaches to the payments location like the primary email.
- Click 'Continue'.
- Confirm that an invitation to the Payments Location was sent to the indicated email.
- Try to modify an existing Payments Location.
- Adjust existing fees and proceed.
- Change the location name and proceed.
- Click 'Invite new users' and confirm the user was added.
- Confirm you can cancel an user invitation by clicking the designated sign.
- Try to resend the invitation to the user and check its functionality.
- Try to delete a payments location at all by clicking the corresponding button. Confirm that you are warned this action could be irreversible.
- If you deleted a Payments Location, confirm it has been removed from the list of Payments Locations.
- Check the values in the list of Payments Locations.

### Payments Profile

- Navigate to 'Payments Profile'.
- Attempt to change the legal name of your incorporated company.
- Check that the 'Send to Transfer Instrument' functionality works correctly.
- Click 'Update profile settings'.
- You should be redirected to the Adyen page.
- Verify that the language displayed is consistent with the one set on the Portal.

**Note:** For testing purposes, you may input fictional information on this page.

- Click 'Company details' and provide the necessary information.
- Click 'Decision-makers' and input the required details. (For ID, a random image file will suffice).
- Click 'Payout details' and fill in the necessary details. (You'll need to generate an IBAN for the country you're based in).
- Click 'Sign services agreement' representing the imaginary person you used in the 'Decision-makers' section.
- After this, you should be able to set up card usage for the location via the Back Office.

For those equipped with test terminals and bank cards, follow these instructions to activate the terminals and test unTill Air's payment functions:

1. Navigate to 'Payment methods'.
2. Add a 'card' payment method.
3. Contact an unTill representative to link the terminal to your location.
4. Set up the payment methods as specified on your test card.
5. Note the POIID from the 'Terminals' section in the Payments Portal.
6. Add a new terminal in the Back Office using the POIID obtained from the Payments Portal.
7. Link the payment terminal to the POS screen you're using.

Now, you can test the payment process at your location.

**Note:** Ensure you're using consistent clusters for testing. If you're on the DEV cluster in the Payments Portal, use the DEV cluster in the Back Office too.

- Order some items at the location where the terminals are linked.
- Pay using the card payment method.
- Confirm that the payment isn't finalised until the test card is used.
- Follow the necessary steps with the test terminal.
- Check if the updates are visible in the Back Office, perhaps in the Reports section.
- Confirm that these updates are also visible on the Payments Portal, given that the transaction has been processed.


### Payouts



### Languages

- Switch between several languages.
- Verify that the translation appears.
- Go through the different sections to make sure that the translation is displayed. 

### Logout

- Click 'Logout'.
- Try to log in again. Verify that entire process was passed as expected.

## Test Cases (Payments Portal)

### Request access to unTill Payments

- Navigate to the unTill Payments page in the Back Office.
- Submit a request.
- Observe that the corresponding signs appear in this section when you attempt to submit a request.
- Verify that the request was successfully sent (use the Reseller account for this purpose).
- As a Reseller, create a Payments Location on the Reseller Portal, then invite users. Ensure that:
  - The invitation is received.
  - New users can access the Payments Portal when they click on the link provided in the email.
- Also, evaluate the email's sending and receiving time. If there's a significant delay, notify the development team as this might be an issue.


### Account

- Navigate to the 'Account' section on the Portal.
- View the values. Are they correct or no?
- Set different timeframes and trace the data changes.
- Check if the refresh button works as expected.

### Profile

- Navigate to 'Payments Profile' section.
- Click 'Update profile settings'.
- You will be redirected to the Adyen page.
- Confirm the language matches the one set on the Portal.
- Click 'Company details' and test the ability to input data and set conditions.
- Browse the list of Adyen pages.
- Copy the credentials provided in this section and input it to the designated page in the Back Office.

### Methods

- Navigate to 'Payments Methods'.
- Click 'Request Payment Methods'.
- The system should prevent when you try to request payment methods without the completing of the 'Profile page'.
- So, complete the 'Profile page' and request some payment methods.
- Check the corresponding values on this page. Verify that they are supposed to be realistic.
- Verify that the refresh page works as expected.

### Terminals

- Navigate to the 'Terminals' section.
- If the location has terminals, check their availability and presence of them in this section.

### Payouts

- Navigate to 'Payouts' section.
- If you have some payouts simulated, check the values, current balance, and all columns with data.

### Logout

- Click Logout.
- Sign in.
- Make sure that the process was passed as expected.

### Languages

- Switch between different languages.
- Go through the Payments Portal and make sure that pages are translated.


## Edge cases

To read a theoretical base regarding "Edge cases", [refer to the Test Plan for Back Office and POS](https://docs.google.com/document/d/1JH1KWSJ1TzXFBp-H8c3hTkOsUP_n_cNefsJWcl0mQuA/edit?usp=sharing).

### Extremal values

This basic approach in the Edge cases assumes the entering of the maximum and minimum values to provocate the possible errors of the system.

#### Examples:

- Try to reach a ceilure of the quantity of Payouts. The system must prevent it and do not allow you to do so until you will be onboarded on the Payments Profile section by clicking 'Update Profile settings' and redirecting to the Adyen Page.

- 

### Corner cases

Try to find the most rare scenarios for users on the Portals.

#### Examples:

- When you are looking for valid subscriptions which are contained in the list of the 'Subscriptions' section where the data regarding Location Owners and their Locations are stored.

- 


