---
layout:     post
title:      Salesforce Introduction
subtitle:   BY Guanqiao Huang
date:       2021-02-10
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - Salesforcr
---
# Basic Terms
[Links](https://trailhead.salesforce.com/content/learn/modules/lex_salesforce_basics/lex_salesforce_basics_welcome)

| Terms | Description |
| ----------- | ----------- |
| CRM | CRM stands for Customer Relationship Management. This technology allows you to manage relationships with your customers and prospects and track data related to all of your interactions.|
| Record | An item you are tracking in your database; if your data is like a spreadsheet, then a record is a row on the spreadsheet |
| Field | A place where you store a value, like a name or address; using our spreadsheet example, a field would be a column on the spreadsheet |
| Object | A table in the database; in that spreadsheet example, an object is a tab on the spreadsheet |
| Org | Short for “organization,” the place where all your data, configuration, and customization lives. You log in to access it. You might also hear this called “your instance of Salesforce” |
| App | A set of fields, objects, permissions, and functionality to support a business process |

# Salesforce Standard Objects
| Terms | Description |
| ----------- | ----------- |
| Accounts | Accounts are the companies you’re doing business with. You can also do business with individual people (like solo contractors) using something called Person Accounts. 理解为每家公司|
| Contacts | Contacts are the people who work at an Account. 理解为每家公司里的人，联系方式|
| Leads | Leads are potential prospects. You haven’t yet qualified that they are ready to buy or what product they need. You don’t have to use Leads, but they can be helpful if you have team selling, or if you have different sales processes for prospects and qualified buyers. 潜在客户。可能的客户|
| Opportunities | Opportunities are qualified leads that you’ve converted. When you convert the Lead, you create an Account and Contact along with the Opportunity. 从潜在客户（潜水）转成有正式的可能客户|

When converting a lead, the following three records are created: Contact,account and opportunity

# Home
1. Performance Chart: Monitor and update your performance to goal.
2. Assistant: Stay on track by seeing the leads and opportunities that require your attention.
3. News: Get insights at a glance on your important accounts.
4. Upcoming events: See the next five meetings on your calendar today.
5. Today’s tasks: See up to five tasks due today.
6. Recent records: Access links to recently viewed records.
7. Top deals: View your top open opportunities in a convenient list.

[Link](https://trailhead.salesforce.com/content/learn/modules/lex_salesforce_basics/lex_salesforce_basics_getting_started)

# Opportunity Workspace
1. Highlights Panel: See important information right at the top of the record.
2. Path: Access customized guidance for each stage in your sales process 和某客户或者某事件的进度.
3. Composer: Quickly log a call, create a task, or send an email 快速做记录.
4. Activity Timeline: View emails, tasks, and events, grouped by your next steps and past activity 查看和这个客户的历史事件，和客户做了啥.
5. Quick View: Hover over any linked record to see details without having to leave the page 一个框在同一页面快速查看其他小数据.

# Accounts and Contacts
1. Highlights Panel: See important information right at the top of the record 用户的主要信息.
2. News and Twitter Integration: Stay informed about the latest news that affects your customers and stay connected through social media 客户的其他媒介动态更新.
3. Optimized template: Easy reference to related records and at-a-glance information.
4. Activity Timeline: View emails, tasks, and events, grouped by your next steps and past activity.

# View
- List Views
- The Kanban View

# What to Do If You Don’t Find What You’re Searching For
1. Check your spelling and verify that you entered the full search term.
2. Check whether the object or field is searchable.
3. Make sure you have access to the record. Search only returns results you have permission to view.
4. If you recently created or updated the record, wait a few minutes for the record to be made searchable. If you can’t find your record after 15 minutes, contact your admin.

# What is a Salesforce Admin?
- Advise on the best way to customize Salesforce to support the way you work
- Design automated processes to help you work faster and smarter
- Help your company learn about and adopt new features
- Work with users to gather feedback and make improvements
- Design and deliver training programs

# Navigate Setup
1. Object Manager: Object Manager is where you can view and customize standard and custom objects in your org.
2. Setup Menu: The menu gives you quick links to a collection of pages that let you do everything from managing your users to modifying security settings.
- Administration: The Administration category is where you manage your users and data. You can do things like add users, change permissions, import and export data, and create email templates.
- Platform Tools: You do most of your customization in Platform Tools. You can view and manage your data model, create apps, modify the user interface, and deploy new features to your users. If you decide to try your hand at programmatic development, Platform Tools is where you manage your code as well.
- Settings: Finally, Settings is where you manage your company information and org security. You can do things like add business hours, change your locale, and view your org’s history.
Of course, these are only some of the pages you can access in the Setup men

3. Main Window: We’re showing you the Setup home page, but this is where you can see whatever it is you’re trying to work on.

# Code with Salesforce Languages
- Lightning Component Framework: A UI development framework similar to AngularJS or React.
- Apex: Salesforce’s proprietary programming language with Java-like syntax.
- Visualforce: A markup language that lets you create custom Salesforce pages with code that looks a lot like HTML, and optionally can use a powerful combination of Apex and JavaScript.

# Lightning Components & Visualforce
The primary difference is right in the name. With Lightning components, you’re developing components that can be pieced together to create pages. With Visualforce, you’re developing entire pages at once. 

# About API
| API | Description |
| ----------- | ----------- |
| SOAP API | Integrate your org’s data with other applications using standard SOAP protocols. |
| REST API | Access objects in your org using standard REST protocols. |
| Metadata API | Manage customizations in your org and build tools that manage your metadata model. |
| Tooling API | Build custom development tools for platform applications. |
| Marketing Cloud API | Expose Marketing Cloud capabilities with the REST API and get comprehensive access to most email functionality with the SOAP API. |
| Bulk API | Load, delete, and perform asynchronous queries on large data sets. |
| Streaming API | Send and receive notifications securely and efficiently. Notifications can reflect data changes in your org, or custom events. |
| Connect REST API | Build UI for Commerce, CMS-Managed Content, Experience Cloud Sites, Files, Notifications, Topics, and more. |
| Mobile SDK | While it’s technically a software development kit, it’s worth including here. Integrate Native or Hybrid mobile apps directly with Salesforce. |

# Heroku
`Heroku` is a web development platform that lets you quickly build, deploy, and scale web apps. Heroku is built on Amazon Web Services (AWS), meaning a lot of infrastructure concerns you might have in standard web app development are taken care of for you. On top of that, `Heroku Connect` unifies your Salesforce data with your `Heroku Postgres` data so you don’t have to manage moving information across platforms. No worrying about infrastructure or data storage means more time for you to focus on new development.

[Links](https://trailhead.salesforce.com/content/learn/modules/starting_force_com/starting_tour)

# Resources
[Salesforce Term Glossary](https://trailhead.salesforce.com/content/learn/modules/starting_force_com/starting_intro)

[Code Sample](https://developer.salesforce.com/code-samples-and-sdks)