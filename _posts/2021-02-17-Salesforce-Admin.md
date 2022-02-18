---
layout:     post
title:      Salesforce Admin Notes
subtitle:   BY Guanqiao Huang
date:       2021-02-17
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - Salesforce
---

# Access and Permission
- Owner , Created Date and Last modify are System field. When ever you will create any object automaticly all those field will create.
- Owner field resides on every object in Standard fields.
- In only one scenario your custom objects will not contain owner field, and that it is in master-detail relationship with another object. As ownership is governed by master object, child object does not need any owner field. Please check if this is your case. 

## 1. Profile: Set/Collection of permissions
- Apps visible
- Tabs visible
- Object - View/Edit/Delete/Create
- Field permissions
- Login Time
- Admin Permissions
- User Permissions

- ***Every user should have a profile***
- ***A user can have only one Profile***
- Profile - User (One to Many Relationship)
## 2. Permission Set: used to define an Exception to Profile
- Collection of Permissions
- One user can have multiple permission sets
- Permission sets extend user's function access without changing their profiles

Example: Sales profile
- 10 Sales Reps
- 1 of these Sales Rep needs additional permissions
- Imagine: Profile (Mobile base plan) & permission Set (Extra Plan)

## 3. Sharing Settings: Data Sharing
- Organization-Wide Defaults = Default Sharing Settings
- Every data have data owner, ownership
- Private Data: Only the owner can see that data
- Public Data: Everyone can see that data, no matter which is the owner
- Setting an object to Private makes records visible to record owners and those above them in the role hierarchy
- Access can be extended using sharing rules.
- Grant access using Hierachies
- Standard Object by default checked on Grant Access Using Hierarchies
- Custom Object can be mofify the hierarchies option enable or not

Example: Sharing Settings:
- Org Wide Default: Private / Public
- Grant access using hierachies
- Sharing rule: which is used to define temporary excception to OWD

## 4. Data Admin Permissions
- View All - Allow users to view all the Data in an Object (Even if OWD is Private)
- Modify All - Allow user to create/Edit/Delete all the Data in an Object (Even if OWD is Private)

## [Review](https://trailhead.salesforce.com/content/learn/modules/data_security/data_security_records?trailmix_creator_id=irenechoi&trailmix_slug=sfd-generation-australia)
You control record-level access in four ways. They’re listed in order of increasing access. You use org-wide defaults to lock down your data to the most restrictive level, and then use the other record-level security tools to grant access to selected users, as required.
- Org-wide defaults specify the default level of access users have to each other’s records.
- Role hierarchies ensure managers have access to the same records as their subordinates. Each role in the hierarchy represents a level of data access that a user or group of users needs.
- Sharing rules are automatic exceptions to org-wide defaults for particular groups of users, to give them access to records they don’t own or can’t normally see.
- Manual sharing lets record owners give read and edit permissions to users who might not have access to the record any other way.

The visibility and access for any type of data is determined by the interaction of the above security controls, based on these key principles.
- A user’s baseline permissions on any object are determined by their profile.
- If the user has any permission sets assigned, these also set the baseline permissions in conjunction with the profile.
- Access to records a user does not own are set first by the org-wide defaults.
- If the org-wide defaults are anything less than Public Read/Write, you can open access back up for certain roles using the role hierarchy.
- You can use sharing rules to expand access to additional groups of users.
- Each record owner can manually share individual records with other users by using the Share button on the record.


## History Tracking
This section lets you set a custom object’s history for both standard and custom fields.

You can select up to 20 standard and custom fields per object. 
You can’t track:
- Formula, roll-up summary, or auto-number fields
- Created By and Last Modified By
- Fields that have the AI Prediction checkbox selected

https://help.salesforce.com/s/articleView?id=sf.tracking_field_history_for_custom_objects.htm&type=5

## Report
- A report can include up to ***5 Custom Summary Formula fields***. This limit is hard-coded and cannot be increased.

# Profiles
About Enahnced Profiles: From Setup, in the Quick Find box, enter User, and then select User Management Settings. Enable Enhanced Profile User Interface.

# User Record


里面有
- Profile Details （有 ***User license***）
- ***Page Layouts*** (有 Sandard page layout & Custom page layout)
- ***Field-Level Security*** (Standard & Custom...)
- Custom App Setting
- Connected App Access
- ***Tab Settings*** (Standard & Custom)
- ***Record Type Settings*** (Standard & Custom)
- Administrative ***Permissions***
- General user permissions
- Standard object permissions
- Custom object permissions
- External object permissions
- Session settings
- ***Password policies***
- ***Login Hours***
- ***Login IP Ranges***
- Enabled Apex Class Access
- Enabled Visualforce Page Access
- Enabled External Data Source Access
- Enabled Named Credential Access
- Enabled Custom Metadata Type Access
- Enabled Custom Setting Definitions Access
- Enabled Flow Access
- Enabled Service Presence Status Access
- Enabled Custom Permissions
- Default Experience Cloud Site

