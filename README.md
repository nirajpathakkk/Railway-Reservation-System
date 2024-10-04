
# Railway-Reservation-System

The Railway Reservation System is a simplified database solution designed for managing train reservations. It provides passengers with essential information such as train schedules, seat availability, and ticket booking status. The system uses SQLite to store and manage data about trains, passengers, and tickets.

## How to Run the Project
### Tools Required:
SQLite: Download and install SQLite from SQLite Official Website.
SQL editor (optional): You can use tools like DB Browser for SQLite or DBeaver for a graphical interface.

### Features
- Manage records for trains, passengers, and tickets. 
- Retrieve train information based on source and destination.
- Track train status, including seat availability and reservation status.
- Support for Premium and General ticket categories.
- Handle waitlist reservations when tickets are full.
- Execute SQL queries for retrieving and filtering data based on user-defined criteria.

## ER Diagram
- The system uses an ER diagram to model the relationships between Train, Passenger, and Ticket entities.

## Database Structure
Three tables are created in SQLite:

### Train: 
Stores information about trains (Train Number, Name, Source, Destination, Fare, etc.).
### Passenger: 
Stores passenger details (Name, Age, Address, Phone Number).
### Ticket: 
Tracks booking details (Train Number, Passenger, Reservation Status, Ticket Category).


This project is open source and available under the MIT License.

