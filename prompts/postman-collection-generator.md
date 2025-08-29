# Postman Collection Generator

```markdown
# Role: Postman Collection Generator

## Goal
Generate a Postman Collection JSON file named `API.json` inside the `docs/` directory. This file must fully document the project’s API endpoints.

## Instructions

### 1. Analyze the Project API
- Review the project codebase to identify **all API endpoints**.  
- For each endpoint, determine:
  - **Purpose & functionality**  
  - **Request method & path**  
  - **Authentication requirements**  
  - **Required & optional headers**  
  - **Query parameters**  
  - **Request body (if applicable, with JSON schema & example payload)**  
  - **Response format & example JSON response**  

---

### 2. Build the Postman Collection (`API.json`)
- **Collections**: Include all API endpoints.  
- **Folders**: Organize endpoints logically (e.g., by feature, resource, or module).  
- **Variables**: Define reusable environment variables, examples:
  - `{{base_url}}` (API host)  
  - Other commonly reused values (e.g., `{{user_id}}`, `{{project_id}}`, `{{email}}`)  
- **Headers**: Include realistic default headers for each request, such as:  
  - `Content-Type: application/json`
  - Any custom headers required by the API  
- **Bodies**: Provide example **request body JSON objects** with realistic values.  
- **Scripts**:  
  - Add a **Pre-request Script** where necessary (e.g., set dynamic variables).  
  - Add a **Script** for login/auth endpoints that auto-saves the token or account ID into `{{auth_token}}` or `{{account_id}}`. Example:
    ```javascript
    let json = pm.response.json();
    if (json.token) {
      pm.environment.set("auth_token", json.token);
    }
    ```
- **Example Responses (Required)**:  
  - Provide **one example JSON response per endpoint**, with realistic data matching the expected schema.  
  - Ensure all responses are valid JSON.  

---

## Deliverable
- A **Postman Collection JSON file** named `API.json` in `docs/API.json` that:  
  - Contains **all endpoints** with correct headers, parameters, and bodies.  
  - Includes **folders** for organization.  
  - Defines **environment variables** for reusability.  
  - Implements **scripts**.  
  - Provides **example request bodies** and **example JSON responses**.  
```