# springboot-dynamic-rule-engine-API
Spring Boot API for dynamically evaluating transactions against configurable rules. Add, view, and apply rules stored in memory without hardcoding. Supports JSON transaction input and returns matches based on runtime-evaluated conditions

<img width="1392" height="805" alt="Screenshot 2026-01-19 201812" src="https://github.com/user-attachments/assets/734b747e-9d80-4c5a-a49a-c85a21fa46e8" />
<img width="1370" height="799" alt="Screenshot 2026-01-19 201717" src="https://github.com/user-attachments/assets/9aaaf2ee-d790-4c85-811c-dc86ca360408" />

# Spring Boot Dynamic Rule Engine

## Overview
This project is a Spring Boot-based API that allows dynamic evaluation of transaction data against configurable rules. Rules are stored temporarily in memory and can be updated at runtime, making it flexible for various transaction scenarios.

## Features
- **Add Rules:** POST `/rules` — Add and store dynamic rules (e.g., `amount > 1000 && type == 'credit'`).
- **Evaluate Transactions:** POST `/evaluate` — Apply all active rules to a list of transactions and return those that match at least one rule.
- **View Active Rules (Optional):** GET `/rules` — Retrieve the currently active rules.
- **Dynamic Evaluation:** Rules are evaluated dynamically using Java’s `ScriptEngineManager`, avoiding hardcoded conditions.
- **In-memory Storage:** No database required; rules are stored temporarily in memory.

## Sample Transaction Data
```json
[
  { "id": 1, "amount": 2500, "type": "credit", "category": "electronics" },
  { "id": 2, "amount": 120, "type": "debit", "category": "grocery" },
  { "id": 3, "amount": 800, "type": "credit", "category": "fashion" }
]


Technology Stack

Java 24

Spring Boot 3+

Maven

ScriptEngineManager for dynamic rule evaluation
  


Clone the repository : git clone https://github.com/yourusername/springboot-dynamic-rule-engine.git

Build the project: mvn clean install

Run the application : mvn spring-boot:run


Developed by Prashant Guttedar
