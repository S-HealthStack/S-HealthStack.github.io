---
title: What is Samsung Health Stack?
sidebar: doc_sidebar
permalink: index.html
toc: false
---

{% include warning.html title="Warning" content="The tested wearable device for the pilot project is the Galaxy Watch 5. Documentation for v1.0 official release is currently under construction. In the meantime, check out release note v1.0 for new features." %}

Today’s health studies using wearable devices typically consist of a wearable device to sense input data, a mobile app that tracks the data, and additional tools to store and analyze the data. Developing these studies from scratch is costly and time consuming. Clearly, a common-use framework can lessen the burden for everyone.

A technology stack (tech stack) is a collection of tools, applications, and services used to build a product. Samsung Health Stack is a tech stack packaged as an open source project that provides end-to-end solutions for collecting and analyzing data from wearable devices in Android and Wear OS environments. Applications include medical research studies to clinician services to whatever your imagination envisions. And as open source project, you are invited to contribute those visions to grow the project.

The stack includes:

-   A software development kit (SDK) for app development
-   A web portal for survey creation, team member management, participant tracking, and data analysis
-   Backend services and a data engine available through application programming interface (API) endpoints

Develop your app using the full stack (recommended) or just the SDK, depending on your use case.

## The App SDK

The app SDK provides developers with what’s needed to create mobile apps that collect data from participants. You can create a mobile app that solicits survey responses from the participant, receives data from the wearable device, displays information to the participant, and transmits the data to a backend system (yours or ours) for further analysis. Building blocks cover:

- Participant onboarding and consent
- Survey presentation
- Creation of participant tasks
- Visual reporting to keep participants engaged
- Data management and transmission to the portal

## The Web Portal

The web portal is a customizable dashboard for interactive data visualization. Managers of studies use the portal to:

- Manage research team members
- Create and deploy app content (for example, participant surveys)
- Track study participant activity
- Analyze participant data

> As of this writing, Chrome is the only browser supported for accessing the web portal.

## Recommended Workflow

1.  Set up your environment.
2.  Set up a study.
3.  Create an app to collect wearable device data.
4.  Create a survey to collect user symptom data.
5.  Onboard participants.
6.  Run your study.
7.  Analyze the results.
