---
title: Role-Based Access Control
sidebar: doc_sidebar
permalink: role-based-access-control.html
toc: false
---

The role-based access control feature provides security with differing levels of access permission granted to different roles.

# Team Roles

Team roles control access at the Samsung Health Stack level. Available roles are:

- Team Admin
- Team Member

The table shows available features for each role.

<table>
  <tr>
    <th style="text-align: center; border-right: 1px solid black;">Features</th>
    <th colspan="2" style="text-align: center;">Roles</th>
  </tr>
   <tr>
    <th style="text-align: center; border-right: 1px solid black;"></th>
    <th style="text-align: center;">Team Admin</th>
    <th style="text-align: center;">Team Member</th>
  </tr>
  <tr>
    <td style="border-right: 1px solid black;">Create Study</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">No</td>
  </tr>
  <tr>
    <td style="border-right: 1px solid black;">Invite Team Members</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">No</td>
  </tr>
</table>
> Only the first person to create a Samsung Health Stack account gets assigned the `Team Admin` team role. Accounts for all others are team member accounts.

# Study Roles

Study roles control access to various aspects of the study. To be part of the team for a given study, a person must have one or more study roles assigned. Available roles are:

- Principal Investigator - has full access to all aspects of the study.
- Research Assistant - has access to most aspects of the study.
- Data Scientist - has access to most aspects of the study, but no access to participants' personal information.

> The portal UI for this feature is complete, but the backend code wasn't completed in time to be included in the beta version. For beta, the`Research Assistant`and `Data Scientist` study roles are not available and the `Principal Investigator` study role displays  as `Researcher`in the **Members and access** table.

The table shows available features for each role.

<table>
  <tr>
    <th colspan="2" style="text-align: center; border-right: 1px solid black;">Features</th>
    <th colspan="4" style="text-align: center;">Roles</th>
  </tr>
  <tr>
    <th colspan="2" style="text-align: center;"></th>
    <th style="text-align: center;">Principal Investigator</th>
    <th style="text-align: center;">Research Assistant</th>
    <th style="text-align: center;">Data Scientist</th>
  </tr>
  <tr>
    <td colspan="6"><b>Study Overview</b></td>
  </tr>
  <tr>
    <td></td>
    <td>Study Progress</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Participant Dropout</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Participant Enrollment</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Task Compliance</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td colspan="6"><b>Participant List</b></td>
  </tr>
  <tr>
    <td></td>
    <td>View Aggregated</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">De-identified</td>
  </tr>
  <tr>
    <td></td>
    <td>View Individual</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">De-identified</td>
  </tr>
  <tr>
    <td colspan="6"><b>In-Lab Visit</b></td>
  </tr>
  <tr>
    <td></td>
    <td>View</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">No</td>
  </tr>
  <tr>
    <td></td>
    <td>Edit</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">No</td>
  </tr>
  <tr>
    <td></td>
    <td>Download</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">No</td>
  </tr>
  <tr>
    <td colspan="6"><b>Surveys</b></td>
  </tr>
  <tr>
    <td></td>
    <td>Create</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Edit</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>View</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Publish</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td colspan="6"><b>Activities</b></td>
  </tr>
  <tr>
    <td></td>
    <td>Create</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Edit</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>View</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Publish</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td colspan="6"><b>Educational Content</b></td>
  </tr>
  <tr>
    <td></td>
    <td>Create</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Edit</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>View</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Publish</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td colspan="6"><b>Sensor Data Viewing</b></td>
  </tr>
  <tr>
    <td></td>
    <td>Avg Resting HR by Gender</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Avg Resting HR by Age</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td colspan="6"><b>Data Queries</b></td>
  </tr>
  <tr>
    <td></td>
    <td>View</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">De-identified</td>
  </tr>
  <tr>
    <td></td>
    <td>Download</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">De-identified</td>
  </tr>
  <tr>
    <td colspan="6"><b>Member Access</b></td>
  </tr>
  <tr>
    <td></td>
    <td>View Members</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">Yes</td>
  </tr>
  <tr>
    <td></td>
    <td>Edit Members</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">If study creator</td>
    <td style="text-align: center;">If study creator</td>
  </tr>
  <tr>
    <td></td>
    <td>Invite Members</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">If study creator</td>
    <td style="text-align: center;">If study creator</td>
  </tr>
  <tr>
    <td></td>
    <td>Delete Members</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">If study creator</td>
    <td style="text-align: center;">If study creator</td>
  </tr>
</table>



<!-- Not until v1.0
  <tr>
    <td></td>
    <td>Grant Management Access</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">If study creator</td>
    <td style="text-align: center;">If study creator</td>
  </tr>
  <tr>
    <td></td>
    <td>Invite New Members</td>
    <td style="text-align: center;">Yes</td>
    <td style="text-align: center;">If study creator or granted access</td>
    <td style="text-align: center;">If study creator or granted access</td>
  </tr>
-->

