##### Prompt Agent : การทดสอบ ใส่ไว้ตอนจบของ prompt
```
Validation rules after all tasks are completed:
- Run the `npm run build` command only via the command prompt (CMD).
- Fix all build errors before proceeding.
- Run the `npm run dev` command only via the command prompt (CMD) when UI validation is required.
- Do not mark tasks as complete until the build is finished.
- All changes must be compatible with the production version of Next.js and its implementation.
```
---
##### Prompt Agent : แก้ไข/จัดการ .gitignore
```
Step : Security Audit & Git Operations
1. Scan the entire project directory.
2. Identify:
Unnecessary files
Build artifacts
   * Cache files
   * OS-generated files
   * IDE/editor files
   * Sensitive files (env, credentials, keys, certificates)
3. Review the current .gitignore.
4. Add any missing entries and explain why each entry should be ignored.
5. Verify that no sensitive files are tracked by Git.

Validation:
* Run git status
* Report files that would be committed
* Highlight any security risks found

After verification:
Create a conventional commit message that summarizes the changes.
Repository: https://github.com/Ittiphon17/cmms.git
Target Branch: dev
```
---
##### Prompt Agent : แก้ UI
```
Important: Do not modify any existing content, functionality, business logic, APIs, routes, or data structures.

Tasks:
- Improve only the UI/UX and responsive design across every component must be compatible devices.
- Make the application fully responsive across desktop, tablet or iPad, and mobile devices.
- Maintain all current features, workflows, and behavior.
- Do not delete, rename, or modify existing functionality.
```
---
##### Prompt Agent : เขียน Readme.md
```
Please write a readme () file following the details below (in English):
# Project Title: One-sentence summary of the project.

# Project Description
## Overview: Briefly describe what the application does and its main purpose.
Example: This project is a full-stack web application designed to help teams manage tasks, track project progress, and improve collaboration through a simple and intuitive interface.
## Features
* User authentication and authorization
* Dashboard and analytics
* Task management
* Real-time updates
* Responsive UI for desktop and mobile

## Technology Stack
Explain why these technologies were chosen.
### Frontend
* React
* TypeScript
* Tailwind CSS
### Backend
* Node.js
* Express.js

### Database
* PostgreSQL

## Folder Structure
```text
project-root/
├── src/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── hooks/
│   └── utils/
├── public/
├── docs/
├── tests/
├── package.json
└── README.md

### Structure Explanation
* components/ → Reusable UI components
* pages/ → Application pages/routes
* services/ → API communication layer
* hooks/ → Custom React hooks
* utils/ → Utility/helper functions
* public/ → Static assets
* tests/ → Unit and integration tests

# Installation
## Prerequisites
Make sure you have installed:

* Node.js (v18+ recommended)
* npm or yarn

## Clone Repository
```bash
git clone <repository-url>
cd <project-name>

## Install Dependencies
```bash
npm install

# Running the Project
## Development Mode
```bash
npm run dev

## Production Build
```bash
npm run build

# Usage
## Login
1. Open the application in your browser.
2. Sign in using your account credentials.

## Create a New Item
1. Navigate to the dashboard.
2. Click "Create New".
3. Fill in the required information.
4. Save the record.

## Manage Existing Data
* View records
* Edit records
* Delete records
* Search and filter records
```
---
##### Prompt Agent : 
```
# Task: In the Equipment Uptime Card zone, we want to change the format from a standard Equipment Uptime Card to three sections while maintaining the original size: "Repair Status Summary," "Average Completion Time," and "Preventive Maintenance (PM) Work."

## Context
This project is a computerized maintenance management system (CMMS) for Mercy Click Medical Clinic and its team of building technicians, surgical equipment technicians, and IT technicians. You must read the AGENTS.md before starting work and follow the instructions.

Do not redesign the entire webpage. Maintain the existing visual design, spacing, card components, colors, and layout structure.
Keep the current UI architecture intact. The design must support future multi-branch use. The implementation should allow for future API replacements without UI changes; use model data for now.
```
---
##### Prompt Agent : 
```
-
```
---
##### Prompt Agent : 
```

```
---
##### Prompt Agent : 
```

```
---
##### Prompt Agent : 
```

```
---

