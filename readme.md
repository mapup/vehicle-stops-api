# Vehicle Stop API Documentation

## Overview

This documentation provides information on the CRUD operations for managing vehicle stops, including details for fuel stops, parking, rest areas, airport charges, and more. It also covers associated meta information such as fuel rates, parking charges, and airport pick-up/drop charges. Each endpoint requires an API key for authentication, and each API key is associated with specific stop information.

## Table of Contents

- [Endpoints](#endpoints)
  - [Create Vehicle Stop](#1-create-vehicle-stop)
  - [Get All Vehicle Stops](#2-get-all-vehicle-stops)
  - [Delete Vehicle Stop](#3-delete-vehicle-stop)
  - [Update Vehicle Stop](#4-update-vehicle-stop)
- [Authentication](#authentication)
- [Error Handling](#error-handling)
- [Examples](#examples)
- [Support](#support)

## Endpoints

### 1. Create Vehicle Stop

- **Endpoint**: `POST /v1/create-vehicle-stops`
- **Description**: Creates a new vehicle stop. The request body consists of two objects: `stop` and `metaData`.
  - **`stop`**: Contains the details of the vehicle stop, such as location, address, and amenities.
  - **`metaData`**: Contains the meta data of the stop, like fuel rates. This object is optional. If `metaData` is not present, only the stop is created. `metaData` can be added later using the update endpoint with the stop ID.
- **Request Body**: [View sample request body](./api-request-samples/create-vehicle-stops)
- **Response Body**: [View sample response body](./api-request-samples/create-vehicle-stops)

### 2. Get All Vehicle Stops

- **Endpoint**: `GET /v1/get-vehicle-stops`
- **Description**: Retrieves a list of all vehicle stops. The response includes details of each stop along with their associated `metaData` if available. If `metaData` is not present, it is not shown in the response.
- **Response Body**: [View sample response body](./api-request-samples/get-vehicle-stops)

### 3. Delete Vehicle Stop

- **Endpoint**: `DELETE /v1/delete-vehicle-stop/{stop_id}`
- **Description**: Deletes the specified vehicle stop. Deleting a stop will also delete the associated meta data.
- **Response Body**:
  ```json
  {
    "message": "Vehicle stop deleted"
  }
### 4. Update Vehicle Stop

- **Endpoint**: `PUT /v1/update-vehicle-stop/{stop_id}`
- **Description**: Updates the details or rates of the specified vehicle stop. The request body consists of two objects: `stop` and `metaData`.
  - **`stop`**: Contains the updated details of the vehicle stop.
  - **`metaData`**: Contains the updated meta data of the stop, like fuel rates. Either `stop`, `metaData`, or both can be updated using this endpoint.
- **Request Body**: [View sample request body](./api-request-samples/update-vehicle-stop)
- **Response Body**: [View sample response body](./api-request-samples/update-vehicle-stop)

## Authentication

Each request to the API requires an API key for authentication. Ensure your API key is included in the headers of your requests.

## Error Handling

The API uses standard HTTP status codes to indicate the success or failure of an API request. Common status codes include:

- `200 OK`: The request was successful.
- `201 Created`: The resource was successfully created.
- `400 Bad Request`: The request was invalid or cannot be otherwise served.
- `401 Unauthorized`: Authentication failed or user does not have permissions for the requested operation.
- `404 Not Found`: The requested resource could not be found.
- `500 Internal Server Error`: An error occurred on the server.

## Examples

For detailed examples of how to use each endpoint, [refer to the sample request and response bodies linked within each endpoint description](./api-request-samples).

## Support

For questions or support, please contact our support team at stop-api-support@mapup.ai
