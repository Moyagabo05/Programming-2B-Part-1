## Core Business Rules Enforced by the ERD
1. **Role Exclusivity:** A single User account can only ever be an Organiser OR a Participant, never both. This is enforced by the application logic checking the `Role` column in the `Users` table.
2. **Category Specificity:** A Category (e.g., "Under 21") is strictly tied to one specific Event. You cannot have a global "Under 21" category that applies to all races.
3. **Result Uniqueness:** A participant can only ever have one recorded result per specific enrolment. An organiser cannot accidentally upload two finish times for the same person in the same race.
