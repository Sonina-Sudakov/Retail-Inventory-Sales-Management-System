# Retail Inventory Sales Management System

Coursework project for the Database Systems course, 3rd year.

The developed application for managing warehouse inventory and a network of stores automates key business processes, improving the efficiency of retail management, reducing operational costs, and supporting better management decisions.

### Project Goal

The goal of this coursework project is to develop an information system for automating inventory management in the warehouse and across the stores of a retail company.

The system is designed to:

* manage product inventory and stock levels;
* track the availability and movement of goods;
* create replenishment orders;
* provide up-to-date information about products and their availability;
* support inventory management across multiple stores and a central warehouse.

## Features

The system supports three user roles with different levels of access and responsibilities.

**Administrator**

* Manage user profiles and store information;
* Manage products and warehouse storage locations;
* View information about requests, deliveries, and sales;
* Generate reports.

**Warehouse Employee**

* View and manage warehouse inventory;
* Record incoming goods;
* Manage warehouse storage locations;
* View store replenishment requests;
* Create and process deliveries to stores;
* Generate warehouse inventory reports.

**Store Employee**

* View store inventory;
* Create requests for product replenishment from the warehouse;
* Record received goods;
* View sales information;
* Generate store inventory reports.

**System Features**

* Inventory tracking across the warehouse and stores;
* Automatic stock updates after sales and deliveries;
* Product quantity analysis;
* Data validation and error handling;
* Role-based access control;
* Transaction management to maintain data consistency;
* Protection against invalid operations, such as selling more products than are available in stock;
* Prevention of deleting records that are referenced by other system entities.

## Technologies
**Backend**

* Python - the primary programming language used to implement the application’s business logic;
* FastAPI - a framework for developing the REST API, handling HTTP requests, routing, and communication between the client and the database;
* SQLAlchemy - an ORM library for interacting with the database;
* PostgreSQL - a relational database management system used to store information about users, products, stores, sales, deliveries, and other system entities;
* Alembic - a database migration tool used to track changes to the database schema and apply migrations;
* Pydantic - a data validation library used to define DTO models for API requests and responses;
* Uvicorn - an ASGI server used to run the FastAPI application.

**Frontend**

* JavaScript - the primary programming language used for the client side;
* React - a library for building the user interface;
* Vite - a build tool and development server for the frontend application;
* Ant Design (Antd) - a library of ready-to-use UI components;
* Axios - a library used to make HTTP requests to the server API.

## Architecture

The application follows a client-server architecture. The frontend communicates with the backend through a REST API, while the backend handles business logic and interaction with the PostgreSQL database.

```text
React + Vite
      │
      │ HTTP / REST API
      ▼
FastAPI
      │
      │ SQLAlchemy
      ▼
PostgreSQL
```

## System Class Diagram

The class diagram represents the main classes of the application and their relationships, reflecting the structure of the implemented system.
<img width="2009" height="1568" alt="image" src="https://github.com/user-attachments/assets/b42974d2-b8bc-4a0b-8d29-a8840122e8ad" />

## Domain Model

The domain model describes the main entities involved in the management of products, stores, warehouse operations, sales, orders, and shipments.
<img width="1682" height="751" alt="image" src="https://github.com/user-attachments/assets/bc8524b4-2506-484a-8ea2-ee3ab9aabc8d" />

## Database Design

The database is designed to manage products, warehouse and store inventory, sales, replenishment requests, and deliveries between the warehouse and stores.

The main entities include:

* User - system users and their roles;
* Shop - stores within the retail network;
* Product - products managed by the system;
* WarehouseStock - product quantities stored in the warehouse;
* ShopStock - product quantities available in each store;
* Order - store requests for product replenishment;
* Shipment - deliveries from the warehouse to stores;
* Sale - completed sales and their items.

The diagram below shows the main entities and relationships between them.
<img width="1280" height="1010" alt="image" src="https://github.com/user-attachments/assets/7dc43d1c-73dd-4d66-a636-9044a0551048" />

