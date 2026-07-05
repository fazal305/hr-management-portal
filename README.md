# HR Management Portal

A browser-based enterprise HR management portal for managing employees,
attendance, leave requests, departments, payroll previews, dashboard
analytics, settings, and local workspace persistence.

## Live Links

- GitHub Repository: [fazal305/hr-management-portal](https://github.com/fazal305/hr-management-portal)
- Live Demo: [https://fazal305.github.io/hr-management-portal/](https://fazal305.github.io/hr-management-portal/)

## Overview

HR Management Portal is a no-build, multi-page frontend application built for portfolio use. It demonstrates enterprise dashboard UI, CRUD workflows, search and filter logic, attendance tracking, leave approvals, payroll previews, and localStorage persistence.

## Pages

- Dashboard: `index.html`
- Employees: `employees.html`
- Attendance: `attendance.html`
- Leave Requests: `leave-requests.html`
- Departments: `departments.html`
- Payroll Preview: `payroll.html`
- Settings: `settings.html`

## Features

- Dashboard metrics and Chart.js visualizations
- Employee CRUD with department, status, and employment type filters
- Attendance marking with duplicate prevention
- Leave request workflow with approve and reject actions
- Department management with manager assignment
- Payroll preview with bonuses, deductions, and net pay
- Settings for company details, currency, dark mode, compact sidebar, import, export, reset, and clear data
- Demo data seeded automatically through localStorage

## Technologies Used

- HTML5
- CSS3
- Bootstrap 5
- jQuery
- Vanilla JavaScript
- Chart.js
- LocalStorage
- Blob API
- Clipboard API

## Learning Outcomes

- Build a multi-page browser application without build tools
- Share layout and state across independent HTML pages
- Design enterprise-style dashboard workflows
- Persist structured frontend state with localStorage
- Implement CRUD, filtering, and workflow state transitions
- Calculate attendance deductions and payroll previews

## Architecture Notes

- Multi-page frontend architecture: every major module has a dedicated HTML page.
- Shared JavaScript utilities: `js/shared.js` owns the workspace model, demo data, helpers, navigation, theme settings, export, and formatting.
- Shared CSS plus page-specific CSS: `styles.css` defines the product shell and design system; every page also loads its own CSS module.
- localStorage workspace model: employees, departments, attendance, leave requests, payroll adjustments, settings, and activity logs are persisted in one local workspace object.
- HR CRUD workflows: employees and departments can be created, edited, deleted, searched, and filtered.
- Attendance and leave workflow state: attendance prevents duplicate employee/date records; leave requests move between pending, approved, and rejected.
- Payroll calculation preview: net pay includes salary, attendance deductions, manual bonuses, and manual deductions.
- Chart.js dashboard rendering: dashboard charts summarize attendance and department distribution.
- No-build browser architecture: the project runs by opening `index.html` locally.

## Folder Structure

```text
hr-management-portal/
  index.html
  employees.html
  attendance.html
  leave-requests.html
  departments.html
  payroll.html
  settings.html
  styles.css
  css/
    dashboard.css
    employees.css
    attendance.css
    leave-requests.css
    departments.css
    payroll.css
    settings.css
  js/
    shared.js
    dashboard.js
    employees.js
    attendance.js
    leave-requests.js
    departments.js
    payroll.js
    settings.js
  README.md
  LICENSE
  .gitignore
```

## How To Run Locally

```bash
git clone https://github.com/fazal305/hr-management-portal.git
cd hr-management-portal
open index.html
```

On Windows, double-click `index.html` or open it from your browser.

## How To Use

1. Open `index.html`.
2. Review dashboard metrics and charts.
3. Visit Employees to add or update employee profiles.
4. Visit Attendance to mark today's status.
5. Visit Leave Requests to create and approve leave.
6. Visit Departments to manage teams and managers.
7. Visit Payroll Preview to adjust bonuses or deductions.
8. Visit Settings to export, import, reset, or clear workspace data.

## Sample Workflow

1. Add department.
2. Add employee.
3. Mark attendance.
4. Create leave request.
5. Approve leave.
6. Preview payroll.
7. Export workspace.

## Agentic Engineering Process

- Specification first: the app goal, pages, features, data model, and expected outcome were defined before implementation.
- Plan and task breakdown: shared styles, page CSS, shared JavaScript, pages, module scripts, documentation, and repository setup were handled as separate steps.
- Verification loops: each file group has clear checks for layout, navigation, CRUD behavior, persistence, and console errors.
- Sandboxing and isolation: the application uses no frameworks or build tools and depends only on CDN Bootstrap, jQuery, and Chart.js.
- Exit criteria and gates: the project is complete only when all pages, localStorage persistence, navigation, dashboard charts, filters, and module workflows work.
- Feedback and iteration loop: the project can be extended page by page while keeping the architecture separated.

## Future Improvements

- Authentication
- Cloud database
- Role permissions
- PDF payslips
- Employee self-service portal
- Attendance calendar view
- Biometric import
- CSV export
- Email notifications
- Multi-branch support

## License

MIT License
