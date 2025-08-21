# AI CLI Commands

- [Codebase](#codebase)
  - [Codebase Auditor](#codebase-auditor)
  - [Codebase Error Auditor](#codebase-error-auditor)
  - [Gemini](#gemini)
- [Starting](#starting)
  - [Comments](#comments)
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
  • Architecture summary  
  • Schema  
  • Routes  
  • Dependencies  
```

### Codebase Error Auditor

```txt
You are an expert codebase error auditor.

Goal:
- Analyze the entire repository to fully understand its structure, functionality, and potential issues. 
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
- Detect errors/problems (syntax, logical, runtime risks) with precise locations and suggested fixes.

Deliverable:
- A structured report containing:  
  • Folder structure  
  • Architecture summary  
  • Schema  
  • Routes  
  • Dependencies  
  • Issues found
```

### Gemini

```txt
@GEMINI.md  
Carefully read GEMINI.md and all files mentioned in it. Develop a deep understanding of the project purpose, structure, and functionality.
```

## Starting

### Comments

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






