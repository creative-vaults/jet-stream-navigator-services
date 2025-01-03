# Jet Stream Navigator Backend

## Overview

The Jet Stream Navigator app is designed to enhance the travel experience by providing comprehensive navigation and real-time updates within airport terminals. This backend system supports various functionalities, including managing terminal maps, user profiles, flights, weather data, and reviews.

## Features

- **Interactive Maps**: Manage and provide data for detailed terminal maps, including locations of gates, shops, and services.
- **User Profiles**: Handle user registration, login, and profile management.
- **Flight Information**: Manage flight schedules, statuses, and notifications.
- **Weather Updates**: Provide real-time weather updates and alerts for both the current location and destination.
- **Points of Interest**: Offer information on shops, restaurants, and services within the airport, along with user reviews and ratings.

## Technologies Used

- **Java 17**
- **Spring Boot 3**
- **PostgreSQL**
- **Maven**
- **Hibernate (JPA)**
- **RESTful API**

## Prerequisites

Ensure you have the following installed:

- **JDK 17+**
- **Maven 3.8+**
- **PostgreSQL 13+**
- **Git**

## Environment Variables

### Database Configuration

Set the following environment variables to configure the database:

- `DB_URL`: `jdbc:postgresql://localhost:5432/jetStreamNavigatorDB`  
  Your database URL
- `DB_USERNAME`: `jet-stream-navigator`  
  Your database username
- `DB_PASSWORD`: `admin12345`  
  Your database password

## Database Setup

### Creating the PostgreSQL Database using pgAdmin

To set up the PostgreSQL database for the Jet Stream Navigator backend, follow these steps:

1. **Open pgAdmin** and connect to your PostgreSQL server.

2. **Create a Role**:
    - In the pgAdmin navigation panel, expand the "Login/Group Roles" node.
    - Right-click on "Login/Group Roles" and select "Create" > "Login/Group Role".
    - Enter `jet-stream-navigator` as the role name.
    - Under the "Definition" tab, set the password to `admin12345`.
    - Under the "Privileges" tab, enable all privileges.
    - Click "Save" to create the role.

3. **Create a New Database**:
    - In the navigation panel, right-click on the "Databases" node.
    - Select "Create" > "Database…".
    - Enter `jetStreamNavigatorDB` as the database name.
    - Under "Owner," select `jet-stream-navigator` from the dropdown menu.
    - Click "Save" to create the database.

## Service Definitions

The following table outlines the services in the Jet Stream Navigator backend:

| Service Name             | Description                | Profile |
|--------------------------|----------------------------|---------|
| **API Gateway**          | Gateway service            | local   |
| **User Service**         | Handles user logic         | local   |
| **Charts Service**       | Provides airports maps     | local   |
| **Flight Service**       | Manages flight data        | local   |
| **Notification Service** | Handles notifications      | local   |
| **POI Service**          | Manages points of interest | local |
| **Review Service**       | Handles user reviews       | local   |
| **Weather Service**      | Provides weather data      | local   |
