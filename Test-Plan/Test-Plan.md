# Test Plan: SettleUp App - Expense Management Feature
**Version:** 1.0
**Date:** Febuary 01, 2026
**Author:** QA Team
**Status:** 

## 1. Introduction
### 1.1 Purpose
To validate core expense management features and identify functional, usability, and data integrity issues through manual and exploratory testing.

### 1.2 Scope
**In Scope:**
- Group creation
- Add/Edit/Delete expense
- Expense split calculation
- Notifications
- Settlement & balances
- Core UI/UX flows

**Out of Scope:**
- Third-party payment integrations
- Advanced reporting features
- Backend API testing
- Performance testing
- Security & penetration testing

## 2. Test Objectives
1. Verify expense creation works with all split methods
2. Ensure accurate balance calculations
3. Validate data persistence and sync
4. Confirm proper error handling
5. Verify user-friendly interface

## 3. Test Approach
### 3.1 Testing Types
- **Functional Testing:** All business logic
- **UI/UX Testing:** Interface and user experience
- **Boundary Value Testing:** Input validations
- **Integration Testing:** Feature interactions
- **Exploratory Testing:** Unscripted testing

### 3.2 Testing Techniques
- Manual testing: 70%
- Checklist-based: 20%
- Regression testing: 10%

## 4. Test Environment
### 4.1 Devices
| Device | OS Version | Screen Size | Purpose |
|--------|------------|-------------|---------|
| OnePlus 7T | Android 12 | 6.55" | Primary testing |

### 4.2 Network Conditions
- WiFi (High speed)
- 4G (Medium speed)
- Airplane Mode (Offline)

### 4.3 Test Data
- Pre-created test groups (3-5 members each)
- Test users with different roles
- Sample expenses for regression

## 5. Schedule & Resources
| Phase | Duration | Resources | Deliverables |
|-------|----------|-----------|--------------|
| Planning | 1 day | 1 QA Lead | Test Plan |
| Design | 2 days | 1 QA Engineer | Test Cases |
| Execution | 3 days | 2 QA Engineers | Test Results, Bugs |
| Reporting | 0.5 day | QA Lead | Test Summary |

## 6. Entry & Exit Criteria
### 6.1 Entry Criteria
- Feature development complete
- Build available in test environment
- Test data prepared
- Test cases reviewed and approved

### 6.2 Exit Criteria
- All critical/high bugs resolved
- Test execution ≥ 95%
- Performance benchmarks met
- Stakeholder sign-off received

## 7. Risks & Mitigation
| Risk | Probability | Impact | Mitigation |
|------|-------------|---------|------------|
| Data corruption | Medium | High | Regular backups |
| Time constraints | High | Medium | Prioritize test cases |
| Device fragmentation | High | Medium | Focus on key devices |

## 8. Deliverables
1. Test cases with execution results
2. Bug reports with evidence
3. Test summary report
4. Risk assessment document
5. Test coverage report

## 9. Approvals
| Role | Name | Signature | Date |
|------|------|-----------|------|
| QA Lead | [Name] |Mallik Galib Shahriar | |
| Product Manager | [Name] | | |
| Development Lead | [Name] | | |