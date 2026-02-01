# Feature Test Scenarios – Add Expense

## Feature Name
Add Expense (Equal & Custom Split)

## Module
Expense Management

## Application
Settle Up – Group Expenses

---

## Feature Description
Users can add an expense within a group, select who paid, and split the amount among members either equally or using a custom split. The system should calculate balances correctly and notify group members.

---

## Preconditions
- Application is installed and launched
- User has created at least one group
- Group has a minimum of 2 members
- User is logged in / active session
- Internet connection available (unless testing offline scenarios)

---

## Test Scenarios & Test Cases

### 1. Functional Test Cases

| TC ID | Scenario | Steps | Expected Result |
|------|---------|-------|----------------|
| TC-01 | Add expense with equal split | Add expense of 300 split among 3 members | Each member owes 100 |
| TC-02 | Add expense with custom split | Enter 300 and split 100/200 | Balances calculated correctly |
| TC-03 | Select different payer | Choose payer other than self | Balance reflects correct payer |
| TC-04 | Save expense | Tap Save | Expense added successfully |
| TC-05 | Cancel expense | Tap Cancel | Expense not saved |

---

### 2. Validation & Negative Test Cases

| TC ID | Scenario | Steps | Expected Result |
|------|---------|-------|----------------|
| TC-06 | Empty amount | Leave amount blank | Validation error shown |
| TC-07 | Zero amount | Enter amount as 0 | Error message displayed |
| TC-08 | Negative amount | Enter -100 | Expense creation blocked |
| TC-09 | Invalid custom split | Split total ≠ expense amount | Error message shown |
| TC-10 | Empty description | Leave description empty | Warning or default text applied |

---

### 3. Edge Case Scenarios

| TC ID | Scenario | Steps | Expected Result |
|------|---------|-------|----------------|
| TC-11 | Decimal amount | Enter 99.99 | Correct rounding applied |
| TC-12 | Large amount | Enter 999999 | App remains stable |
| TC-13 | Long description | Enter 200+ characters | UI handles text properly |
| TC-14 | Emoji in description | Add emojis | Expense saved without UI issues |
| TC-15 | Split among 3 members | Split 100 among 3 | Total remains 100 |

---

### 4. UI & Device Handling Scenarios

| TC ID | Scenario | Steps | Expected Result |
|------|---------|-------|----------------|
| TC-16 | Screen rotation | Rotate device during input | Entered data retained |
| TC-17 | Back button pressed | Press back during entry | Confirmation popup shown |
| TC-18 | Multiple save taps | Tap Save repeatedly | Only one expense created |
| TC-19 | Dark mode enabled | Enable dark mode | Text and UI remain readable |
| TC-20 | Keyboard overlap | Open keyboard | Input fields visible |

---

### 5. Network & Stability Scenarios

| TC ID | Scenario | Steps | Expected Result |
|------|---------|-------|----------------|
| TC-21 | Save expense offline | Turn off internet and save | Proper offline error message |
| TC-22 | Network fluctuation | Toggle network while saving | No duplicate expense |
| TC-23 | App backgrounded | Background app mid-entry | Data preserved |
| TC-24 | App crash recovery | Force close app | No partial data saved |
| TC-25 | Low battery mode | Enable power saver | Expense saved correctly |

---

### 6. Notification & Data Integrity

| TC ID | Scenario | Steps | Expected Result |
|------|---------|-------|----------------|
| TC-26 | Notification on add | Add expense | Members receive notification |
| TC-27 | Notification on edit | Edit expense | Notification sent |
| TC-28 | Balance update | Add expense | Balances recalculated correctly |
| TC-29 | History update | Add expense | Appears in expense history |
| TC-30 | Export data | Export expenses | New expense included in export |

---

## Test Evidence
- Screenshots of expense form, validation errors, and balance updates
- Short screen recordings (5–10 seconds) showing expense creation flow

---

## Risk Areas Identified
- Split calculation and rounding errors
- Duplicate expense creation on multiple save taps
- Missing validations for amount and split
- Data loss during offline or rotation scenarios

---

## Interview-Ready Summary
This feature was tested using positive, negative, edge, UI, network, and data integrity scenarios to ensure accurate financial calculations, proper validations, stable behavior, and reliable notifications.
