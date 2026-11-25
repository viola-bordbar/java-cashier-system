# Java Cashier System

## Overview
A modular Java-based point-of-sale system developed as a university project at KTH Royal Institute of Technology. The application simulates the flow of a cashier transaction, from registering items and calculating totals to handling payment and generating a receipt.

## Features
- **Sale management:** Register items and quantities, and manage ongoing sales.
- **Price calculations:** Calculate running totals, VAT and change.
- **Discount handling:** Retrieve discounts based on customer IDs.
- **Payment processing:** Register customer payments and calculate change.
- **System integration:** Update inventory and accounting systems upon completion of a sale.
- **Receipt generation:** Generate and print receipts containing sale information.
- **Revenue tracking:** Track total revenue using observer-based updates, with revenue displayed and recorded to a file.
- **Error handling and logging:** Handle item lookup and registration failures and log relevant exceptions.

## Architecture
The application follows a modular architecture with separation of concerns between the following components:

- **Controller:** Coordinates the sale process and communicates with the model and integration components.
- **Model:** Represents sales, registered items and payments, and handles calculations and transaction logic.
- **View:** Simulates the user interaction and displays sale information.
- **DTOs:** Transfer item and sale information between components.
- **Integration:** Represents external systems, including inventory, accounting, discount handling and receipt printing.
- **Observer pattern:** Allows revenue observers to receive updates when a sale is completed.

## Technologies
- Java
- Object-oriented programming
- Design patterns, including the Observer pattern

## How to Run

Compile the source files (from the project root directory):

```powershell
New-Item -ItemType Directory -Force -Path out | Out-Null
javac -d out (Get-ChildItem -Path src/main/java -Recurse -Filter *.java | ForEach-Object { $_.FullName })
```

Run the program:

```powershell
java -cp out se.kth.iv1350.processSale.startup.Main
```
