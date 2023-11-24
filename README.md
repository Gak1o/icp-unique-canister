# icp-unique-canister
Title: Event Management Canister

Description:

I am submitting a Rust program that implements an event management canister for the Internet Computer (IC). The canister allows users to add, remove, and query events, each defined by a name, start date, and duration. The code uses the IC libraries and canister development macros to achieve CRUD functionality.

Key Components:

Event Structs:

Event struct represents an event with a name and timestamp.
EventWithDuration includes additional information such as a start date and duration.
Date Parsing:

The parse_date function parses a date string into a timestamp, supporting the expected format "YYYY-MM-DD."
Duration Validation:

The validate_duration function ensures that event durations are less than or equal to 31 days.
Query Function - get_events:

Retrieves a list of events by iterating over canister storage.
Update Function - add_event:

Adds an event to the canister, validating the duration and storing the event with the current timestamp.
Update Function - remove_event:

Removes an event from canister storage based on the provided event ID.
How to Use:

Deploy the canister.
Use the addEvent update function to add new events with a name, start date, and duration.
Use the removeEvent update function to remove events by specifying their event ID.
Use the getEvents query function to retrieve a list of all events.
Note:
Ensure that the provided date follows the "YYYY-MM-DD" format for accurate parsing.

This code is designed for managing events within the Internet Computer environment, providing a simple and flexible way to handle event-related data.
