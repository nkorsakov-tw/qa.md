# Test Plan

## Abstract

This document is prepared to provide guidelines that testers must adhere to in order to systematically optimise the testing of the Payments Portal and the Reseller Portal. This document contains the descriptions of basic approaches in testing that can help you to find the potential error quite more efficient.  

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

### Payments Profile

- If you have a role of the Payments Reseller you are able to test other sections of the Reseller Portal.
- Navigate to Account. View the data provided. Check it correctness.
- Set the different timeframes and trace how the data is changed.
- If you have an access to execution of the payouts, test how the feature payouts will be reflected in the Account section.