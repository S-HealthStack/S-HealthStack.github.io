

Roles Management

Our stack allows users to assign user roles using the API endpoints in the  [Account Service  API Endpoints](account-service-api-endpoints.html).

V1.0 expanded roles from two to four. Following are the respective key values for these roles: 

| **Role**               | **REST API Key**         |
| ---------------------- | ------------------------ |
| Study Creator          | “study-creator”          |
| Principal Investigator | “principal-investigator” |
| Research Assistant     | “research-assistant”     |
| Data Scientist         | “data-scientist”         |

To get more information about the access level for each role, please refer to [Role-Based Access Control](role-based-access-control.html). 

## API Endpoints

To assign roles to a user using the API endpoints:

1. Refer to `POST /account-service/user/roles` in [Account Service  API Endpoints](account-service-api-endpoints.html#assigns-roles-to-a-user) in the API reference.

To remove roles from a user using the API endpoints:

1. Refer to `PATCH /account-service/user/roles/remove` in [Account Service API Endpoints](account-service-api-endpoints.html#removes-roles-from-a-user) in the API reference.

