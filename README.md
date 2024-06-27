# employee-management-system
CREATE TABLE Rooms (
    RoomID INT PRIMARY KEY,
    RoomNumber VARCHAR(10) NOT NULL,
    RoomType VARCHAR(50),
    BedType VARCHAR(50),
    Rate DECIMAL(10, 2) NOT NULL,
    Status VARCHAR(20) DEFAULT 'Available'
);
INSERT INTO Rooms (RoomID, RoomNumber, RoomType, BedType, Rate, Status)
VALUES
    (1, '101', 'ac room', 'double', 150.00, 'Available'),
    (2, '102', 'simple room', 'single', 90.00, 'Available'),
    (3, '103', 'ac room', 'single', 90.00, 'Available'),
    (4, '104', 'luxry room', 'double', 250.00, 'Available');


CREATE TABLE Guests (
    GuestID INT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Email VARCHAR(100),
    Phone VARCHAR(20),
    Address VARCHAR(100)
);
INSERT INTO Guests (GuestID, FirstName, LastName, Email, Phone, Address)
VALUES
    (1, 'John', 'Doe', 'john.doe@example.com', '+1234567890', '123 Main St, City'),
    (2, 'Jane', 'Smith', 'jane.smith@example.com', '+1987654321', '456 Elm St, Town'),
    (3, 'Michael', 'Johnson', 'michael.johnson@example.com', '+1122334455', '789 Oak St, Village');



CREATE TABLE Transactions (
    TransactionID INT PRIMARY KEY,
    TransactionType VARCHAR(50) NOT NULL,
    Amount DECIMAL(10, 2) NOT NULL,
    TransactionDate DATETIME DEFAULT CURRENT_TIMESTAMP  
);

INSERT INTO Transactions (TransactionID,TransactionType, Amount, TransactionDate)
VALUES
    (1,'Payment', 200.00, '2024-04-18 10 pm'),
    (2,'Payment', 300.00, '2024-04-19 11 am'),
    (3,'Payment', 600.00, '2024-04-20 15:45 am'),
    (4,'Payment', 450.00, '2024-06-05 09:00 pm');

CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Position VARCHAR(50) NOT NULL,
    Email VARCHAR(100),
    Phone VARCHAR(20)
);
INSERT INTO Employees (EmployeeID, FirstName, LastName, Position, Email, Phone)
VALUES
    (1, 'nikhil', 'joshi', 'Receptionist', 'nikhiljoshi112@gmail.com', '7302203074'),
    (2, 'shubham', 'adhikari', 'Manager', 'shubhamadk112@gmail.com', '9368757888');


SELECT * FROM Rooms;
SELECT * FROM Guests;
SELECT * FROM Transactions;
SELECT * FROM Employees;
