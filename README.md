
# Railway-Reservation-System
Project Overview
The Railway Reservation System is a simplified database solution designed for managing train reservations. It provides passengers with essential information such as train schedules, seat availability, and ticket booking status. The system uses SQLite to store and manage data about trains, passengers, and tickets.

Features
Manage records for trains, passengers, and tickets.
Retrieve train information based on source and destination.
Track train status, including seat availability and reservation status.
Support for Premium and General ticket categories.
Handle waitlist reservations when tickets are full.
Execute SQL queries for retrieving and filtering data based on user-defined criteria.
ER Diagram
The system uses an ER diagram to model the relationships between Train, Passenger, and Ticket entities.

Database Structure
Three tables are created in SQLite:

Train: Stores information about trains (Train Number, Name, Source, Destination, Fare, etc.).
Passenger: Stores passenger details (Name, Age, Address, Phone Number).
Ticket: Tracks booking details (Train Number, Passenger, Reservation Status, Ticket Category).
SQL Queries
A variety of SQL queries are included to retrieve useful information such as:

Passengers booked on a particular train.
Confirmed passengers traveling on a specific day.
Train details and passengers between the ages of 50 and 60.
Waitlisted passengers and their train details.
Sample Queries:
Retrieve passengers booked on a train:

sql
Copy code
SELECT Train.TrainName, Train.Source, Train.Destination
FROM Passenger
JOIN Ticket ON Passenger.PassengerID = Ticket.PassengerID
JOIN Train ON Ticket.TrainNumber = Train.TrainNumber
WHERE Passenger.FirstName = 'John' AND Passenger.LastName = 'Doe';
List confirmed passengers for a specific day:

sql
Copy code
SELECT Passenger.FirstName, Passenger.LastName
FROM Ticket
JOIN Passenger ON Ticket.PassengerID = Passenger.PassengerID
WHERE Ticket.ReservationDate = '2024-09-30' AND Ticket.Status = 'Confirmed';
How to Run the Project
Tools Required:
SQLite: Download and install SQLite from SQLite Official Website.
SQL editor (optional): You can use tools like DB Browser for SQLite or DBeaver for a graphical interface.
Steps:
Clone or download the project files.
Run the provided SQL script to create the database tables (CREATE TABLE statements).
Insert sample data using the provided INSERT queries or by manually entering data through an SQL editor.
Execute the provided SQL queries to interact with the database and retrieve train and passenger information.
Assumptions
There are only two categories of tickets: Premium and General.
The maximum number of tickets available for each category is 10, and the waitlist supports 2 passengers.
The system does not consider intermediate stops before the train's destination.
The total number of trains in the system is 5.
Contributions
Database Design: Designed the ER diagram and developed the database schema.
SQL Queries: Wrote and optimized SQL queries to fetch information from the database.
Data Handling: Managed the insertion and retrieval of data for passengers, trains, and ticket reservations.
Future Enhancements
Adding support for real-time seat allocation and ticket booking via a user interface.
Expanding the system to handle multiple stop points and dynamic ticket pricing.
License
This project is open source and available under the MIT License.

