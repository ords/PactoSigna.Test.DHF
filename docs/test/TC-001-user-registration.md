---
id: TC-001
title: User Registration Test Cases
version: "1.0"
status: approved
links:
  - TP-001
  - SRS-001-01
created: 2025-01-11
updated: 2025-01-14
author: James Wilson
reviewer: David Park
approver: Mike Chen
---

# User Registration Test Cases

## TC-001-01: Successful Registration

**Preconditions:**
- User is not logged in
- Email is not already registered

**Steps:**
1. Navigate to /register
2. Enter valid email: `test@example.com`
3. Enter valid password: `SecurePass123!`
4. Enter name: `Test User`
5. Click "Register" button

**Expected Result:**
- User is created in Firebase Auth
- User document created in Firestore
- Redirect to dashboard
- Welcome toast displayed

---

## TC-001-02: Invalid Email Format

**Steps:**
1. Navigate to /register
2. Enter invalid email: `notanemail`
3. Click "Register" button

**Expected Result:**
- Form shows error: "Invalid email format"
- No API call made

---

## TC-001-03: Weak Password

**Steps:**
1. Navigate to /register
2. Enter valid email
3. Enter weak password: `123`
4. Click "Register" button

**Expected Result:**
- Form shows error: "Password must be at least 8 characters"

---

## TC-001-04: Duplicate Email

**Preconditions:**
- Email `existing@example.com` already registered

**Steps:**
1. Navigate to /register
2. Enter email: `existing@example.com`
3. Enter valid password and name
4. Click "Register" button

**Expected Result:**
- Error: "Email already in use"
