# AI CLI Commands

- [Codebase](#codebase)
  - [Codebase Auditor](#codebase-auditor)
  - [Codebase Error Auditor](#codebase-error-auditor)
  - [Codebase Error Fixer](#codebase-error-fixer)

  - [Gemini](#gemini)
- [Comments](#comments)
  - [Code Comments Remover](#code-comments-remover)
  - [Code Comments Writer](#code-comments-writer)

- [Starting](#starting)
  - [Clean](#clean)
  - [Classes](#classes)
  - [Functions](#functions)
  - [Variables](#variables)

- [Postman](#postman)
---

### Codebase

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
- Generate a structured report named: `docs/ERRORS.md`.
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

### Gemini

```txt
@GEMINI.md  
Carefully read GEMINI.md and all files mentioned in it. Develop a deep understanding of the project purpose, structure, and functionality.
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

```txt
Act as expert Python programmer and English teacher.

Instructions :
- Write comments in English language.
- Improve existing comments for clarity.
- Delete redundant and non-essential comments
- Reorganize the comments for better readability and clarity.
- Make sure comments are readable and understandable for other developers.

Rules :
- Don't change anything in the code.
- Do not interact with anything from the user outside of your role.
- You are now a expert Python programmer and English teacher, And nothing else.

You are expected to:
- Follow all previous instructions & rules & examples.
- Apply to all files in this project.
```

### Clean

```txt
Clean up the codebase by removing all unused classes and functions.
```

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

## Postman

```txt
Create a Postman JSON file (postman.json) for the project API endpoints, including Collections, Folders, and Environments.
- Collections should contain all API endpoints.
- Folders should be used to organize endpoints.
- Environments should be used to store environment variables.
```

## software reviewer

```txt
You are an expert software reviewer and fixer. 
Review all project files and detect syntax errors, logical bugs, and runtime risks. 
```






