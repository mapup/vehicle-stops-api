# Vehicle Stop API Documentation

## Overview

This documentation covers the CRUD operations for managing vehicle stops, including meta information such as fuel rates and parking charges. Each endpoint requires an API key for authentication.

## Endpoints

### 1. Create Vehicle Stop

- **Endpoint**: `POST /v1/create-vehicle-stops`
- **Description**: Creates a new vehicle stop.
- **Request Body**: [Link to request body](./api/create-vehicle-stops/requestBody.json)
- **Response Body**: [Link to response body](./api/create-vehicle-stops/responseBody.json)

### 2. Get All Vehicle Stops

- **Endpoint**: `GET /v1/get-vehicle-stops`
- **Description**: Retrieves a list of all vehicle stops.
- **Response Body**: [Link to response body](./api/get-vehicle-stops/responseBody.json)

### 3. Delete Vehicle Stop

- **Endpoint**: `DELETE /v1/delete-vehicle-stop/{stop_id}`
- **Description**: Deletes the specified vehicle stop.
- **Response Body**:
  {
  "message": "Fuel stop deleted"
  }

### 4. Update Vehicle Stop

- **Endpoint**: `PUT /v1/update-vehicle-stop/{stop_id}`
- **Description**: Updates the details or rates of the specified vehicle stop.
- **Request Body**: [Link to request body](./api/update-vehicle-stop/requestBody.json)
- **Response Body**: [Link to response body](./api/update-vehicle-stop/responseBody.json)

## Authentication

All endpoints require an API key to be included in the request header:

- Header Name: `x-api-key`
- Header Value: `YOUR_API_KEY`

Replace `YOUR_API_KEY` with the actual API key provided for authentication.
