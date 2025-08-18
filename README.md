# AI CLI Commands

- [Codebase](#codebase)
  - [Review](#review)
  - [Rereview](#rereview)
- [Starting](#starting)
  - [Comments](#comments)
  - [Classes](#classes)
  - [Functions](#functions)
  - [Variables](#variables)

- [Postman](#postman)
---

### Codebase

### Review

```txt
Review the entire codebase carefully. Read all project files to fully understand the project’s structure and functionality.

Instructions :
- Review every directory in the project.
- Review every subdirectory in the project.
- Review every file in the project.
- Pay special attention to GEMINI.md (if present).
- Pay special attention to README.md (if present).

Rules :
- Exclude compiled Python files (.pyc, __pycache__) and other non-essential/generated files.

You are expected to:
- Gain a complete understanding of the codebase.
- Identify and note the project’s objectives, structure, and key details.
- Identify and note database design/usage, patterns, and file/directory map.
```

### Rereview

```txt
Rereview the entire codebase carefully from scratch. Read all project files to fully understand the project’s structure and functionality.

Instructions :
- Start the review from scratch.
- Rereview every directory in the project.
- Rereview every subdirectory in the project.
- Rereview every file in the project.
- Pay special attention to GEMINI.md (if present).
- Pay special attention to README.md (if present).

Rules :
- Exclude compiled Python files (.pyc, __pycache__) and other non-essential/generated files.

You are expected to:
- Gain a complete understanding of the codebase.
- Identify and note the project’s objectives, structure, and key details.
- Identify and note database design/usage, patterns, and file/directory map.
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

### Classes

```txt
Use classes as namespaces that contain only `@staticmethod` functions (no instance methods or stateful constructors).
```

### Functions

```txt
Use snake_case for function names, e.g., get_user, delete_user; avoid PascalCase like GetUser.
```

### variables

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