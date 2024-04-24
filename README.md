# LEADTOREV---Assignment
LEADTOREV  - Assignment 

# Product Catalogue REST API

This project implements a RESTful API for a structured product catalogue system using Java, Spring Boot, Hibernate, and MySQL. The API allows for managing products with complex nested data structures, including CRUD operations, searching, pagination, sorting, and rating functionality.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Setup Instructions](#setup-instructions)
- [Endpoints](#endpoints)
- [Data Model](#data-model)
- [Database Setup](#database-setup)
- [Deployment](#deployment)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

## Features

- Create, retrieve, update, and delete products
- Search products with filters for name, category, and attributes
- Pagination and sorting in product list retrieval
- Rate products and update ratings
- Clear and comprehensive API documentation

## Technologies Used

- Java
- Spring Boot
- Hibernate
- MySQL
- Maven

## Getting Started

### Prerequisites

Before running the application, make sure you have the following installed:

- Java Development Kit (JDK)
- MySQL Server
- Maven

### Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/your_username/product-catalogue.git
   ```

2. Navigate to the project directory:

   ```bash
   cd product-catalogue
   ```

3. Configure MySQL database:
   - Create a MySQL database named `SPC` (or any preferred name).
   - Update the database connection settings in `hibernate.cfg.xml`.

4. Build the project using Maven:

   ```bash
   mvn clean install
   ```

5. Run the application:

   ```bash
   java -jar target/product-catalogue.jar
   ```

## Endpoints

- **POST /products**: Create a new product.
- **GET /products/{id}**: Retrieve a product by ID.
- **PUT /products/{id}**: Update a product.
- **DELETE /products/{id}**: Delete a product.
- **GET /products**: Retrieve a list of products with optional filters, pagination, and sorting.
- **POST /products/{id}/ratings**: Rate a product.

For detailed request and response formats, refer to the API documentation.

## Data Model

The Product entity has the following attributes:

- id (String)
- name (String)
- description (String)
- price (double)
- categories (List<String>)
- attributes (List<Map<String, String>>)
- availability (Availability)
- ratings (List<Rating>)

For a detailed data model diagram, see [DataModel.png](DataModel.png).

## Database Setup

- Create a MySQL database named `SPC`.
- Update the database connection settings in `hibernate.cfg.xml`.
- Run the application to automatically create database tables based on entity mappings.

## Deployment

The application can be deployed to any cloud platform or your own server. Ensure MySQL is accessible from the deployed environment.

## Testing

Test the API endpoints using tools like Postman or cURL. Verify functionality including CRUD operations, search, pagination, sorting, and rating.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for any improvements or new features.

