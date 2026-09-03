# RaceDay Data Dictionary
This document provides a detailed breakdown of the data types and constraints for the core entities.

| Entity | Attribute | Data Type | Constraint | Description |
|--------|-----------|-----------|------------|-------------|
| Users | UserID | INT | PK, Identity | Auto-incrementing unique identifier. |
| Users | Email | VARCHAR(255) | Unique, Not Null | Used for authentication. |
| Events | Distance | DECIMAL(5,2) | Not Null | Race distance in km (e.g., 10.50). |
| Enrolments | Status | VARCHAR(50) | Default 'Pending' | Tracks entry approval state. |
