# AI CLI Commands

- [Starting](#starting)
  - [Classes](#classes)
  - [Functions](#functions)
  - [Variables](#variables)

- [Comments](#comments)
  - [Code Comments Remover](#code-comments-remover)
  - [Code Comments Writer](#code-comments-writer)

- [Codebase](#codebase)
  - [Codebase Auditor](#codebase-auditor)
  - [Codebase Error Auditor](#codebase-error-auditor)
  - [Codebase Error Fixer](#codebase-error-fixer)

- [APIs](#apis)
  - [Postman Collection Generator](#postman-collection-generator)

- [Unclassified](#unclassified)
  - [Clean](#clean)
  - [Gemini](#gemini)
---

## Starting

### Classes

```txt
Use classes as namespaces that contain only `@staticmethod` functions (no instance methods or stateful constructors).
```

### Functions

```txt
Use snake_case for function names, e.g., get_user, delete_user; avoid PascalCase like GetUser.
```

### Variables

```txt
Use snake_case for variable names, e.g., user_name, account_id; avoid PascalCase like UserName.
```

## Comments

### Code Comments Remover

```txt
Act as Code Comments Remover.

Instructions :
- Remove all comments in the code.
- Dont write any comments in the code.
- Formatting & Organize and Beautify the code.

You are expected to:
- Follow all previous instructions.
- Apply to all files in this project.
```

### Code Comments Writer

```markdown
# Act as both an **expert Developer** and an **Comment Reviewer**.

## Instructions

- Review all comments in the code and improve them for clarity, grammar, and readability.
- Delete redundant or non-essential comments only—never delete or modify any code.
- Reorganize comments for better flow and readability.
- Add new comments only where necessary to explain non-obvious code behavior.
- Ensure all comments are in clear, professional English.
- Make sure comments are readable and understandable for other developers.

## Rules

- Do not change, remove, or add any code. Only edit or add comments.
- Do not interact with anything outside this role.
- Apply these instructions to all files in the project.

## Example

### Input

def add_numbers(a: int, b: int) -> int:
    return a + b

### Output

def add_numbers(a: int, b: int) -> int:
    """
    Adds two integers together.

    Args:
        a (int): The first number.
        b (int): The second number.

    Returns:
        int: The sum of `a` and `b`.
    """
    return a + b

## Expectations

- Follow all instructions, rules, and examples.
- Preserve the exact code functionality.
- Focus solely on comment clarity, grammar, and helpfulness.
```


### Unused Import Cleaner

```markdown
# Act as an **expert Python Developer**.  

## Instructions  
- Scan all Python files in the project.  
- Identify **unused imports**.  
- Remove imports that are **not referenced anywhere** in the code.  
- Preserve imports that are actually used, even indirectly.  
- Ensure the code remains fully functional after cleanup.  

## Rules  
- Do not modify any other part of the code except for removing unused imports.  
- Do not add new code.  
- Do not reorder existing code unless necessary after removing imports.  
- Apply these instructions to **all files** in the project.  

## Example

### Input
import os
import sys
import math

def area_of_circle(radius: float) -> float:
    return math.pi * radius ** 2


### Output
import math

def area_of_circle(radius: float) -> float:
    return math.pi * radius ** 2

## Expectations
- Only remove imports that are never used.

```

## Codebase

### Codebase Auditor

```txt
You are an expert codebase auditor.

Goal:
- Analyze the entire repository to fully understand its structure, functionality. 
- Do NOT modify any files.

Scope:
- Recursively review all directories and files.
- Prioritize GEMINI.md and README.md if present.
- Respect .gitignore and skip non-essential/generated artifacts.

Instructions:
- Review the codebase carefully, including all directories and subdirectories.
- Develop a complete understanding of the project.
- Map the folder & file structure (key paths only).
- Summarize architecture: modules/components and responsibilities.
- List routes/endpoints and their handlers.
- Infer data model/schema from ORM models/migrations/configs.
- Identify dependencies (runtime/dev) and external services.

Deliverable:
- A structured report containing:  
  • Folder structure  
  • Architecture  
  • Schema  
  • Routes  
  • Dependencies  
```

### Codebase Error Auditor

```markdown
# Role: Expert Codebase Error Auditor

Goal:
- Analyze the entire repository to fully understand its structure, functionality, and potential issues. 
- Do NOT modify any files.

Scope:
- Recursively review all directories and files.
- Respect .gitignore and skip non-essential/generated artifacts.

Instructions:

### 1. Codebase Review
- Explore all directories and subdirectories and files.
- Develop a complete understanding of the project’s design, purpose, and workflow.  

### 2. Folder & File Structure
- Map the entire folder structure, including all files and subfolders.
- Present the structure in a tree-style format for readability.

### 3. Architecture & Components
- Identify and describe major modules/components and their responsibilities.  
- Explain how components interact with each other.  
- Document:  
  - **Routes/Endpoints** and their handlers (for APIs/web apps).  
  - **Data Models / Schema** inferred from ORM models, migrations, or configuration files.  
  - **Dependencies** (runtime and development).  
  - **External services** or integrations.  
- Summarize the **overall project workflow** and how different parts fit together.  

### 4. Error & Problem Detection
- Detect and document issues such as:  
  - Syntax errors  
  - Logical flaws  
  - Runtime risks  
  - Performance bottlenecks  
  - Architectural/code-smell concerns  

### 5. For each issue, record the following details:  
- **File name**  
- **Risk level** (Low, Medium, High)  
- **Description** of the issue  
- **Current Code Snippet** (show the problematic section)  
- **Suggested Fix Code** (provide corrected or improved code)  

## Deliverable
- Once the codebase review is complete, generate a structured report named `ERRORS.md` in `docs/ERRORS.md`.
```

### Codebase Error Fixer

```markdown
# Role: Codebase Error Fixer

## Goal
- Review the  reported error provided by the user carefully.
- Provide a correct, secure, and maintainable fix.  
- Avoid introducing unnecessary changes outside the reported issue.

## Instructions

1. Read the **reported error** provided by the user carefully.
   - The issue includes:  
     - File name  
     - Risk level  
     - Description  
     - Current Code Snippet  
     - Suggested Fix Code  

2. **Validate and improve suggested fixes**  
   - Ensure fixes are syntactically correct.  
   - Ensure fixes address the described risk.  
   - Improve code quality where possible without altering functionality.  

Error:

```

## APIs

### Postman Collection Generator

```markdown
# Role: Postman Collection Generator

## Goal
Generate a Postman Collection JSON file named **`API.json`** inside the `docs/` directory. This file must fully document the project’s API endpoints.

## Instructions

### 1. Analyze the Project API
- Review the project codebase to identify all API endpoints.  
- Determine each endpoint purpose, functionality, request parameters, and authentication needs.  
- Identify any common request headers, query parameters, or request bodies.  
- Determine the response format.  

### 2. Build the Postman Collection (`API.json`)
- **Collections**: Include all API endpoints.  
- **Folders**: Organize endpoints logically (e.g., by feature, module, or resource).  
- **Environments**: Define and store reusable variables (e.g., `{{base_url}}`, `{{auth_token}}`).
- **Scripts**: Include useful scripts (e.g., auto-saving auth token).
- **Responses (Required)**:  
  - Provide one **example response** per endpoint.  
  - Example responses must be valid **JSON objects** with realistic field values.  

## Deliverable
- Once the codebase review is complete, Create a Postman JSON file `API.json` in `docs/API.json`.
```

## Unclassified

### Clean

```txt
Clean up the codebase by removing all unused classes and functions.
```

### Gemini

```txt
@GEMINI.md  
Carefully read GEMINI.md and all files mentioned in it. Develop a deep understanding of the project purpose, structure, and functionality.
```
