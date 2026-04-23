# 🍽️ Foody App — QA Manual Testing

Manual testing of the **Foody** web application — a platform for sharing food experiences. The project covers 6 Use Cases with 70+ test cases and 10 reported bugs.

---

## 📋 Table of Contents

- [Test Scope](#test-scope)
- [Test Cases](#test-cases)
- [Bug Report](#bug-report)
- [Bug Priorities](#bug-priorities)
- [File Structure](#file-structure)

---

## Test Scope

| Use Case | Description | Test Cases |
|----------|-------------|------------|
| UC1 | Home Page | 19 |
| UC2 | User Registration (Sign Up) | 22 |
| UC3 | User Sign In (Log In) | 8 |
| UC4 | Profile Management | 15 |
| UC5 | Food Creation | 8 |
| UC6 | Food Management | 8 |

---

## Test Cases

### UC1 — Home Page
Covers page availability, navbar and button functionality for both **guest** and **logged-in** users. Includes search functionality and food card action buttons.

### UC2 — User Registration
Sign Up form tested with valid and invalid data for every field:
- `Username` — min. 2, max. 30 characters
- `Email` — valid format with `@` and `.`
- `First / Middle / Last Name` — min. 2, max. 60 characters
- `Password` — min. 6, max. 30 characters; both password fields must match
- `Middle Name` is optional

### UC3 — User Sign In
Log In form tested with correct and incorrect credentials. Covers `FORGOT PASSWORD` and `CREATE NEW` button functionality.

### UC4 — Profile Management
My Profile page — viewing and editing profile data. Validates all fields including profile picture (must be a valid URL), About Me and About Food Passion sections (max. 256 characters each).

### UC5 — Food Creation
Add Food form validation:
- `Food Name` — max. 70 characters
- `Describe your food` — max. 400 characters
- `Picture URL` — must be a valid URL

### UC6 — Food Management
VIEW / EDIT / DELETE functionality for existing food entries.

---

## Bug Report

| Bug ID | Test Case | Priority | Severity | Title |
|--------|-----------|----------|----------|-------|
| B1 | REQ | High | Critical | Inconsistent validation criteria between Sign Up and Edit Profile |
| B2 | UC1-7 | Medium | High | About Us page is missing |
| B3 | UC1-8 | Medium | High | "Sign Up Now" picture is not clickable |
| B4 | UC2-2 | High | Critical | Terms and Conditions checkbox and link are missing |
| B5 | UC2-12 | High | Critical | Registration accepted with email not containing "." |
| B6 | UC2-15 | High | High | Registration accepted with Middle Name of 1 character |
| B7 | UC3-8 | High | High | Forgot Password link does not work |
| B8 | UC1-10 | Medium | Low | Home page welcome message shows username instead of first name |
| B9 | UC4-5 | Medium | Medium | Edit Profile page fields have incorrect labels |
| B10 | UC6-1 | Low | High | VIEW button is missing on food cards |

---

## Bug Priorities

### 🔴 Critical — Fix Immediately
> Block core user functionality.

- **B4** — Terms & Conditions link missing on Sign Up page
- **B5** — System accepts email without a dot (e.g. `test@test`)
- **B1** — Inconsistent field validation rules between Sign Up and Edit Profile

### 🔴 High — Fix Before Release
> Significant issues affecting UX and security.

- **B6** — Middle Name of 1 character is accepted (minimum should be 2)
- **B7** — Forgot Password link leads nowhere

### 🟡 Medium — Fix in Next Sprint
> Functional issues, but the app remains usable.

- **B2** — LEARN MORE button does not open an About Us page
- **B3** — "Join Us" picture on Home Page is not clickable
- **B8** — Welcome message shows username instead of user's first name
- **B9** — Edit Profile fields have wrong or incomplete labels

### 🟢 Low — Nice to Fix
> Minor issues with low user impact.

- **B10** — VIEW button is missing from the food list

---

## File Structure

```
QA_Manual_Testing_Exam.xlsx
├── Sheet: Use Case 1 — Home Page
├── Sheet: Use Case 2 — User Registration
├── Sheet: Use Case 3 — User Sign In
├── Sheet: Use Case 4 — Profile Management
├── Sheet: Use Case 5 — Food Creation
├── Sheet: Use Case 6 — Food Management
└── Sheet: BUG REPORT
```

---

## Legend

| Field | Description |
|-------|-------------|
| **Priority** | Blocker / High / Medium / Low — business impact |
| **Severity** | Critical / High / Medium / Low — technical impact |
| **Pass / Fail** | Test execution result |
| **Prerequisites** | Required conditions before test execution |

---

*QA Project — Foody Web App | Manual Testing*
