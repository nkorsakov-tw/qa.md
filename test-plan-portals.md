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

- Request an invitation from the Reseller Admin and then check that the invitation was sent exactly as expected and then you have the ability to enter the payments portal and at the 