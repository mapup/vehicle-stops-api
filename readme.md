# Vehicle Stop API Documentation

## Overview

This documentation covers the CRUD operations for managing vehicle stops, including meta information such as fuel rates and parking charges. Each endpoint requires an API key for authentication.

## Endpoints

### 1. Create Vehicle Stop

- **Endpoint**: `POST /v1/create-vehicle-stops`
- **Description**: Creates a new vehicle stop. The request body consists of two objects: `stop` and `metaData`.
  - **`stop`**: Contains the details of the vehicle stop, such as location, address, and amenities.
  - **`metaData`**: Contains the meta data of the stop, like fuel rates. This object is optional. If `metaData` is not present, only the stop is created. `metaData` can be added later using the update endpoint with the stop ID.
- **Request Body**: [Link to request body](./api-request-samples/create-vehicle-stops)
- **Response Body**: [Link to response body](./api-request-samples/create-vehicle-stops)

### 2. Get All Vehicle Stops

- **Endpoint**: `GET /v1/get-vehicle-stops`
- **Description**: Retrieves a list of all vehicle stops. The response includes details of each stop along with their associated `metaData` if available. If `metaData` is not present, it is not shown in the response.
- **Response Body**: [Link to response body](./api-request-samples/get-vehicle-stops)

### 3. Delete Vehicle Stop

- **Endpoint**: `DELETE /v1/delete-vehicle-stop/{stop_id}`
- **Description**: Deletes the specified vehicle stop. Deleting a stop will also delete the associated meta data.
- **Response Body**:
  ```json
  {
    "message": "Fuel stop deleted"
  }
  ```

### 4. Update Vehicle Stop

- **Endpoint**: `PUT /v1/update-vehicle-stop/{stop_id}`
- **Description**: Updates the details or rates of the specified vehicle stop. The request body consists of two objects: `stop` and `metaData`.
  - **`stop`**: Contains the updated details of the vehicle stop.
  - **`metaData`**: Contains the updated meta data of the stop, like fuel rates. Either `stop`, `metaData`, or both can be updated using this endpoint.
- **Request Body**: [Link to request body](./api-request-samples/update-vehicle-stop)
- **Response Body**: [Link to response body](./api-request-samples/update-vehicle-stop)
