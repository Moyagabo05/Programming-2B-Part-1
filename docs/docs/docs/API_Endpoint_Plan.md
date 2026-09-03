## API Assumptions & Edge Cases
- **Assumption:** The system assumes that an Organiser cannot enrol as a Participant in their own event. If this is required in the future, a separate `OrganiserEnrolments` table would be needed.
- **Edge Case (Cancellation):** If an Organiser deletes an Event, the system must handle the cascading deletion of associated Categories and Enrolments to maintain referential integrity.
- **Edge Case (Duplicate Enrolment):** The API must check if a `ParticipantID` and `EventID` combination already exists in the `Enrolments` table before inserting a new record to prevent duplicate entries.
