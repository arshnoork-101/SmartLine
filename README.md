# SmartLine

## Project Overview

The **SmartLine** is a C++ application designed to simulate a factory production environment. The system manages multiple workstations along an assembly line, where each workstation processes customer orders based on the availability of items. This project showcases real-world factory automation principles, such as inventory management, order processing, and work-in-progress management, all while adhering to object-oriented programming (OOP) principles.


## Project Objective

The goal of this project is to build a modular system that:
1. Simulates the processing of customer orders across a series of assembly line workstations.
2. Handles the assembly of products using dynamic inventory and product tracking systems.
3. Supports full-stack order management, including order fulfillment, item tracking, and output reporting.

The simulation will mimic real-world factory workflows, automating product assembly and managing inventory levels to ensure efficient production.


## Key Features

- **Modular Design**: The project is structured into multiple modular components, each responsible for a different aspect of the assembly line process. The primary modules include:
  - `Utilities` for parsing input and setting up configurations.
  - `Station` to manage items and inventory at each workstation.
  - `CustomerOrder` to represent customer requests and manage order status.
  - `Workstation` to simulate the processing of customer orders at each station.
  - `LineManager` to manage the flow of orders across the assembly line.

- **Testing**: Testing ensures isolated and easier issue detection. It is separated into distinct modules to verify individual components:
- **Tester #1**: Tests Utilities and Station.
- **Tester #2**: Tests CustomerOrder.
- **Tester #3**: Tests Workstation and LineManager.

- **Order Fulfillment**: Each workstation checks for available items in its inventory and processes them as part of the customer orders. The line manager coordinates the flow of orders and keeps track of whether an order has been completed or is still pending.

- **Dynamic Inventory**: The `Station` module manages the quantity of items available at each workstation, with the ability to update inventory levels as products are processed.

- **Order Tracking and Reporting**: The system tracks each order as it moves through the assembly line, providing a report on which orders have been completed and which are still in progress. Completed orders are flagged, while incomplete orders are passed to the next station for further processing.


## Technical Details

- **Modules and Classes**:
  - **Utilities**: Manages input parsing and formatting, ensures consistency in data input across the system.
  - **Station**: Represents a specific station in the assembly line. It holds an item, manages inventory, and provides functionality for item processing.
  - **CustomerOrder**: Encapsulates an individual customer order. It handles order details like item names, quantities, and processing statuses.
  - **Workstation**: Inherits from `Station` and represents an active workstation on the assembly line. It handles a queue of customer orders and processes them in sequence.
  - **LineManager**: Coordinates the movement of orders through the entire assembly line, ensuring that items are processed, and orders are fulfilled.

- **Memory Management**: The project utilizes dynamic memory management to handle customer orders, ensuring no memory leaks occur during runtime. The use of smart pointers and move semantics ensures efficient memory usage.


## Directory Structure

.
├── src

│   ├── CustomerOrder.cpp / .h

│   ├── LineManager.cpp / .h
│   ├── Station.cpp / .h
│   ├── Utilities.cpp / .h
│   ├── Workstation.cpp / .h
├── data
│   ├── Station1.txt
    ├── Station2.txt
│   ├── CustomerOrder.txt
│   └── AssemblyLine.txt
├── testers
│   ├── tester_1.cpp
│   ├── tester_2.cpp
│   └── tester_3.cpp
├── output
│   ├── tester_1_output.txt
│   ├── tester_2_output.txt
│   └── tester_3_output.txt
├── README.md


### **Project Structure Organization**

To improve the maintainability and clarity of the **SmartLine** project, I have organized the project files into distinct directories based on their roles. This structuring is intended to logically separate different types of files, making the project easier to navigate and manage as it grows. However, despite this folder-based division, the entire application runs as a combined system, ensuring the seamless execution of all components together.


## Conclusion

The **SmartLine** Factory Assembly Line Simulator demonstrates how a factory's production process can be effectively managed using object-oriented programming techniques. The project emphasizes modularity, dynamic memory management, and efficient processing, providing a comprehensive simulation of an assembly line that can be expanded or modified to suit various industrial applications.
