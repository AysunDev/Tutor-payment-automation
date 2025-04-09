# Insightstem Tutors – Automated Fee Calculation System

This project is part of a Salesforce-based solution built for managing tutoring services. It focuses on automating the fee calculation and payment creation processes based on dynamic business rules.

---

## 💡 Project Summary

In traditional setups, calculating tutoring fees manually caused delays and errors. This system uses Apex, Custom Metadata, and automation to:

- Calculate fees based on selected packages and additional subjects
- Apply sibling discounts dynamically
- Support both monthly and yearly payment plans
- Allow admin users to configure pricing logic without needing a developer

---

## ⚙️ Features

### 🔹 Apex-Based Fee Engine
- `PaymentUtility.CalculateTotalAmount()`: Calculates total fee using package price, extra subjects, and sibling discounts
- `ChildDiscountConfigsUtility`: Applies discount rules based on number of siblings
- Uses centralized logic and utility classes for reuse and maintenance

### 🔹 Trigger-Based Automation
- `ServiceTriggerHandler`: Automatically generates `Payment__c` records on service creation
- Monthly/yearly logic handled via `DateUtility`
- Supports installment breakdowns

### 🔹 Admin-Friendly Configuration
- Custom Metadata Types used to define:
  - Package pricing
  - Discount percentages
  - Payment rules and installment months

### 🔹 Logging & Test Coverage
- Built-in logging via `APILogUtility` for error/success tracking
- Bulk-safe and test-covered (85%+)

---

## 🧩 Technologies Used

- Apex Classes and Triggers
- Custom Metadata Types
- Lightning Flow (for admin interaction if applicable)
- SOQL, DML
- Salesforce Platform Events (optional)
- Test Classes

---

## 📈 Result

- 80%+ reduction in manual errors
- Modular design allowed reusability for other finance modules
- Admins could update rules instantly — no deployments needed
- Highly scalable and robust logic

---

## 💬 Sample Interview Pitch

> "I developed a flexible fee automation system on Salesforce using Apex utilities and Custom Metadata Types. It handled sibling discounts, course logic, and created automated payment schedules. Admins could change pricing rules without touching code. This reduced manual work and errors significantly."

---

> **Disclaimer:** This project is anonymized and simplified for demo purposes. It does not contain any real user or business data.
