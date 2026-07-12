# OnlyTech — AI Powered Enterprise Knowledge Management System

An AI-powered Enterprise Knowledge Management & Incident Management Platform that enables employees to securely upload organizational documents, query enterprise knowledge using AI, manage incidents, and allows administrators to review, approve, and govern the complete knowledge repository.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Proposed Solution](#proposed-solution)
- [User Roles](#user-roles)
- [Complete System Workflow](#complete-system-workflow)
- [Authentication Flow](#authentication-flow)
- [Employee Portal Workflow](#employee-portal-workflow)
- [Admin Portal Workflow](#admin-portal-workflow)
- [PlantMind AI Workflow](#plantmind-ai-workflow)
- [Document Approval Workflow](#document-approval-workflow)
- [Incident Management Workflow](#incident-management-workflow)
- [Dashboard Analytics](#dashboard-analytics)
- [Technology Stack](#technology-stack)
- [Project Architecture](#project-architecture)
- [Folder Structure](#folder-structure)
- [Installation](#installation)
- [Future Enhancements](#future-enhancements)

---

## Project Overview

Organizations store thousands of documents including SOPs, HR Policies, IT Guidelines, Security Manuals, Maintenance Documents, and Technical Knowledge.

Finding the correct document takes time, and employees often receive outdated or incorrect information.

**OnlyTech** solves this problem using an AI-powered Knowledge Repository where:

- Employees upload documents
- AI learns from approved documents
- Employees ask questions in natural language
- Administrators verify every uploaded document
- Incident reporting and tracking are integrated into one platform

---

## Problem Statement

Traditional document management systems suffer from:

- Difficult document search
- Duplicate files
- No AI assistance
- Manual knowledge sharing
- Unauthorized document access
- Lack of approval workflow
- No centralized incident management

---

## Proposed Solution

OnlyTech provides a centralized AI-powered platform where:

- Employees securely upload documents
- Admin reviews and approves submissions
- AI indexes approved knowledge
- Employees ask questions in plain English
- Incidents are tracked centrally
- Complete organization knowledge remains up-to-date

---

## User Roles

There are two separate portals.

### Employee

Responsible for:

- Uploading documents
- Updating existing documents
- Using PlantMind AI
- Reporting incidents
- Viewing personal dashboard

### Administrator

Responsible for:

- Managing repository
- Reviewing uploaded documents
- Approving or rejecting documents
- Managing incidents
- Monitoring AI usage
- Managing system settings

---

## Complete System Workflow

```
Employee Login
      │
      ▼
Dashboard
      │
      ├──────── Upload Document
      │
      ├──────── Update Existing Document
      │
      ├──────── Ask PlantMind AI
      │
      ├──────── Report Incident
      │
      ▼
Admin Receives Notification
      │
      ▼
Admin Reviews Document
      │
      ├──────── Reject
      │
      └──────── Approve
                    │
                    ▼
Repository Updated
                    │
                    ▼
PlantMind AI learns new knowledge
                    │
                    ▼
Employees receive updated AI answers
```

---

## Authentication Flow

**Step 1**
User opens application.

**Step 2**
User enters:
- Email
- Password

**Step 3**
System validates credentials.

If valid → **Authentication Successful**

User is redirected according to role.

```
Employee → Employee Dashboard
Admin    → Admin Dashboard
```

---

## Employee Portal Workflow

### Step 1 — Login

Employee logs in. Dashboard displays:

- Employee Name
- Employee ID
- Department
- Status
- Current Date

### Step 2 — Dashboard Overview

Employee immediately sees:

- Uploaded Documents
- Updated Documents
- Open Incidents
- System Alerts

These cards provide quick insights into daily work.

### Step 3 — Upload Documents

Employee selects **Upload Docs**. System asks for:

- Document Title
- Category
- Description
- File Upload

Supported formats:

- PDF
- DOCX
- TXT

### Step 4 — Document Validation

System checks:

- File format
- File size
- Duplicate files

If valid, status becomes **Pending Approval**.

### Step 5 — Admin Notification

Admin immediately receives **1 Pending Approval**.

### Step 6 — Update Existing Documents

Employee selects an already uploaded document. Can:

- Replace document
- Update content
- Modify description

The updated version goes into **Pending Review**.

### Step 7 — PlantMind AI

Employee opens **PlantMind AI**.

Example questions:

- How do I configure VPN?
- Explain leave policy.
- What is the onboarding process?
- Where is the network security SOP?

AI searches only the **approved repository**.

Response includes:

- Relevant answer
- Source document
- Related knowledge

### Step 8 — Incident Reporting

Employee opens **Maintenance** and creates an incident.

Example:

- Printer not working
- VPN issue
- Server downtime
- Network failure

Incident contains:

- Title
- Description
- Priority
- Timestamp

Status becomes **Open**.

### Step 9 — Recent Activity

Employee dashboard stores:

- Uploaded documents
- Updated files
- Incident reports

Everything appears inside **Recent Activity**.

---

## Admin Portal Workflow

Administrator has complete control over the system.

### Dashboard Overview

Admin can monitor:

- Active Documents
- Pending Approvals
- Open Incidents
- Critical Alerts

Everything updates in real time.

### Step 1 — Review Pending Documents

Admin opens **Approvals**. Each document contains:

- Employee Name
- Upload Time
- Department
- Document Preview

### Step 2 — Admin Decision

Admin can **Approve** or **Reject**.

**If Rejected** — Employee receives notification:
> Rejected — Reason: Incorrect Version

**If Approved** — Document moves into the **Knowledge Repository**. PlantMind AI automatically gains access.

### Step 3 — Knowledge Repository

Admin manages:

- Search
- Categories
- Version History
- Document Status

Repository becomes the organization's official knowledge base.

### Step 4 — Incident Management

Admin opens **Active Incidents**. Can:

- View incidents
- Change priority
- Assign employee
- Close incident

**Incident lifecycle:**

```
Open → Assigned → In Progress → Resolved → Closed
```

### Step 5 — Incident Analytics

Dashboard displays:

- Weekly incidents
- Incident trend
- Open incidents
- Critical alerts

Helps management monitor system health.

### Step 6 — Top Queries

PlantMind AI records most searched topics.

Examples:

- VPN
- Security Policy
- HR Leave
- Onboarding
- Maintenance SOP

This helps identify:

- Frequently requested knowledge
- Missing documentation
- Training requirements

### Step 7 — Settings

Administrator manages:

- User Accounts
- Roles
- Access Permissions
- Security
- System Configuration

---

## PlantMind AI Workflow

```
Employee asks question
        ↓
Question sent to Backend
        ↓
Embedding Generated
        ↓
Vector Database Search
        ↓
Relevant Documents Retrieved
        ↓
Large Language Model Generates Answer
        ↓
Answer Returned with Context
```

> Only approved documents participate in AI responses. This prevents misinformation.

---

## Document Approval Workflow

```
Employee Upload
        ↓
Pending Approval
        ↓
Admin Review
        ↓
Approve / Reject
        ↓
Knowledge Repository
        ↓
PlantMind AI Updated
```

---

## Incident Management Workflow

```
Employee Reports Issue
        ↓
Incident Created
        ↓
Admin Reviews
        ↓
Assign Priority
        ↓
Resolve Issue
        ↓
Close Incident
        ↓
Activity Logged
```

---

## Dashboard Analytics

### Employee Dashboard

- Uploaded Documents
- Updated Documents
- Open Incidents
- Alerts
- Recent Activities

### Admin Dashboard

- Active Repository
- Pending Reviews
- Open Incidents
- Critical Alerts
- Incident Trends
- AI Query Analytics
- Repository Growth

---

## Technology Stack

| Layer | Technologies |
|---|---|
| **Frontend** | HTML5, CSS3, JavaScript, Bootstrap / Tailwind CSS |
| **Backend** | Python, Flask |
| **Database** | Supabase |
| **AI** | Google Gemini API, Sentence Transformers, Vector Embeddings |
| **Authentication** | Flask Session, Role-Based Access Control |
| **Deployment** | GitHub, Render / Railway / Vercel |

---

## Project Architecture

```
                 Employee
                      │
                      ▼
              Employee Portal
                      │
       Upload / Update / AI Query
                      │
                      ▼
              Flask Backend API
                      │
       ┌──────────────┼──────────────┐
       ▼              ▼              ▼
   MongoDB        AI Engine        File Storage
       │              │
       └───────Repository────────────┘
                      │
                      ▼
               Admin Dashboard
```

---

## Folder Structure

```
OnlyTech/
├── README.md
└── AI_Document_manage-main/
    ├── .gitignore
    ├── admin.html
    ├── app.py
    ├── employee.html
    ├── requirements.txt
    └── runtime.txt
```

---

## Installation

```bash
git clone https://github.com/yourusername/OnlyTech.git

cd OnlyTech

pip install -r requirements.txt

python app.py
```

Open in browser:

```
(https://ai-document-manage-fyjk.onrender.com)
```

---

## Future Enhancements

- OCR support for scanned documents
- Voice-based AI assistant
- Multi-language document understanding
- Email notifications
- Slack / MS Teams integration
- Real-time collaboration
- Advanced analytics dashboard
- Mobile application
- AI-generated document summaries
- Automatic document version comparison

---

## License

This project is licensed under the terms specified by the repository owner.

## Contributing

Contributions, issues, and feature requests are welcome. Feel free to check the issues page if you want to contribute.
