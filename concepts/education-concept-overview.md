---
title: "Education API overview"
description: "The education API in Microsoft Graph enhances Microsoft 365 resources with information that is relevant for education scenarios, including information about schools, classes, users (students and teachers), assignments, and submissions. This makes it easy for you to build solutions that integrate with educational resources for various school and classroom scenarios."
author: "mmast-msft"
ms.localizationpriority: high
ms.prod: "education"
ms.custom: scenarios:getting-started
---

# Education API overview

The education API in Microsoft Graph enhances Microsoft 365 resources with information that is relevant for education scenarios, including information about schools, classes, users (students and teachers), assignments, and submissions. This makes it easy for you to build solutions that integrate with educational resources for various school and classroom scenarios.

> [!VIDEO https://www.youtube-nocookie.com/embed/EnDM7KMTEqQ]

## Why integrate with education scenarios?

### Build applications that are aware of class roster

Most education software developers learn early on that class roster is one of the key pieces of information they need to run their application, and it's typically locked away inside a school Student Information System (SIS). Any time teachers bring a new application into their classroom, they spend time manually importing roster data into the app. Many independent software vendors (ISVs) address this by connecting with a SIS to import roster data. With hundreds of Student Information Systems with proprietary formats, this can become a challenge. [Microsoft School Data Sync](https://sds.microsoft.com/), combined with roster APIs, addresses this challenge for application developers and schools.

The following are some of the scenarios that the roster APIs enable:

- [Get all classes in a school](/graph/api/educationschool-list-classes?view=graph-rest-1.0)
- [Get all users in a class](/graph/api/educationclass-list-members?view=graph-rest-1.0)
- [Get all the classes I teach](/graph/api/educationuser-list-classes?view=graph-rest-1.0)


### Use Microsoft Teams to create class assignments in an assignments tab

You can use the assignment-related education APIs to integrate with assignments in Microsoft Teams. Microsoft Teams in Microsoft 365 for Education is based on the same education APIs, and provides a use case for what you can do with the APIs. Your app can use these APIs to interact with assignments throughout the assignment lifecycle.

The assignment APIs provide the following key resources:

•	[educationAssignment](/graph/api/resources/educationassignment?view=graph-rest-1.0) - The core object of the assignments API. Represents a task or unit of work assigned to a student or team member in a class as part of their study.
•	[educationSubmission](/graph/api/resources/educationsubmission?view=graph-rest-1.0) - Represents the resources that an individual (or group) submits for an assignment and the associated grade and feedback for that assignment.
•	[educationResource](/graph/api/resources/educationresource?view=graph-rest-1.0) - Represents the learning object that is being assigned or submitted. An **educationResource** is associated with an **educationAssignment** and/or an **educationSubmission**.


With the assignment API, your app can interact with the assignment service outside of Microsoft Teams. Microsoft Teams will handle distribution, due dates, and grading while your system can provide a rich learning experience to students.
The following are examples of a few scenarios enabled by the assignments API:

- [Add an assignment that links to your application](/graph/api/educationclass-post-assignments?view=graph-rest-1.0) 
- [Assign outcomes like grades to individual students for assignments linked to your application](/graph/api/educationoutcome-update?view=graph-rest-1.0)
- [Create a student dashboard to show which assignments are due by when](/graph/api/educationclass-list-assignments?view=graph-rest-1.0)


### Enable school admins to manage identity and roster sync using School Data Sync Management (preview)

[School Data Sync](https://sds.microsoft.com/) helps to automate the process of importing and synchronizing student identity and roster data from student information systems with Azure Active Directory (Azure AD) and Microsoft 365. When the information is synchronized, you can use the roster APIs to read the roster information into the applications. If you're a system integrator setting up integration of a school's Student Information System with School Data Sync, you can use the [SDS management APIs](/graph/api/resources/educationsynchronizationprofile?view=graph-rest-beta) in Microsoft Graph to set up synchronization from either a CSV file or a supported SIS API connector.

School Data Sync management APIs support end-to-end scenarios for managing sync; for example:

- [Create a synchronization profile that automatically starts a sync](/graph/api/educationsynchronizationprofile-post?view=graph-rest-beta)
- Manage sync lifecycle with [pause](/graph/api/educationsynchronizationprofile-pause?view=graph-rest-beta), [resume](/graph/api/educationsynchronizationprofile-resume?view=graph-rest-beta) and [reset](/graph/api/educationsynchronizationprofile-reset?view=graph-rest-beta) operations

## API reference
Looking for the API reference for this service?

- [Education API in Microsoft Graph v1.0](/graph/api/resources/education-overview?view=graph-rest-1.0)
- [Education API in Microsoft Graph beta](/graph/api/resources/education-overview?view=graph-rest-beta)


## Next Steps

- To start using the education APIs, see:
  - [Use the roster APIs](/graph/api/resources/education-overview?view=graph-rest-1.0)
  - [Use the assignment APIs](/graph/api/resources/educationassignment?view=graph-rest-1.0)
  - [Use the SDS management APIs](/graph/api/resources/educationsynchronizationprofile?view=graph-rest-beta)
- Try the education APIs in [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer).
- Explore the following education-related samples:
  - [.NET sample for SSO & Rostering](https://github.com/OfficeDev/O365-EDU-AspNetMVC-Samples)
  - [Sample for profile management APIs](https://github.com/OfficeDev/O365-EDU-SDS-AspNetMVC-Samples) 



