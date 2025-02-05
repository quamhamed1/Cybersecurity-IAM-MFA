# Azure MFA Configuration Lab 

## Overview 
This repository contains a step-by-step guide to configuring MFA in Microsoft Azure.

Lab Objectives 

This lab demonstrates how to configure and enforce Multi-Factor Authentication (MFA) ub Azure Active Directory using Microsoft Authenticator. The key objectives include: 
- Enabling Per-user MFA
- Configuring Microsoft Authenticator as a supported athentication method
- Enforcing an MFA Registration Policy
- Creating a Conditional Access Policy to enforce MFA for users
- Testing the end-user experience with Microsoft Authenticator registration


  Step-by-step Implementation

  Step 1: Enable Per-User MFA
  key Actions:

  - Navigate to Entra ID Portal ---> Click Users
  - Select pER-USER mfa UNDER Manage user settings
  - Enable MFA for the test user
 
    Description: This step ensures that the test user is required to complete MFA authentication upon login.

  Step 2: Cofnigure Microsoft Authenticator as an authentication Method
  Key actions:

  - Navigate to Azure AD Portal ---> Go to Security --> Click Authentication Methods
  - Select Microsoft Authenticator and ensure it's enabled
  - Assign it to ALL Users or a specefic test user
 
    Description: This step configures Microsoft Authenticator as an allowed authentication method for MFA.

  Step 3:Configure MFA Regristration Policy
  Key actions:

  - Navigate to Azure AD --> go to Security  --> Click Identity Protection
  - Select MFA Registration Policy and Enable it
  - Assign the policy to the test user group
 
    Description: This step forces users to register for MFA when signing in to ensure they complete the setup.

  Step 4: Create a conditional Access Policy to enforce MFA
  Key actions:

  - Navigate to Azure AD --> Security --> Conditional Access
  - Click +NEW Policy and name it to your liking
  - Under Users, Select the specific user/ group
  - Under Cloud Apps, select all Apps
  - Under Access controls, Select require MFA
  - Click Enable Policy --> create
 
    Description: This step enforces MFA when users attempt to access cloud applications, increasing security.

  Step 5: Test User Registration for Microsoft Authenticator
  Key actions:

  - Open an incognito browser and navigate to https://aka.ms/mfasetup
  - Sign in as test user
  - Follow prompts to register Authenticator app
  - Enter code from Authenticator app to
  - Log out and attempt to log in again to verify MFA enforcement
 
    Description: This step ensures that the MFA setup works correctly and that the test user is required to authenticate using Microsoft Authenticator
