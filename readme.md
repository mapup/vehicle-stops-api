# Vehicle Stops CRUD API Documentation

## Overview

This API provides CRUD (Create, Read, Update, Delete) operations for managing vehicle stops and associated meta-information such as fuel rates, parking charges, and other details. Each endpoint requires an API key for authentication.

## API Endpoints

### Create a Vehicle Stop

- **URL**: `/create-vehicle-stops`
- **Method**: `POST`
- **Headers**:
  - `x-api-key: your_api_key`
  - `Content-Type: application/json`

### Get Vehicle Stops

- **URL**: `/get-vehicle-stops`
- **Method**: `GET`
- **Headers**:
  - `x-api-key: your_api_key`

### Update a Vehicle Stop

- **URL**: `/update-vehicle-stop/:stop_id`
- **Method**: `PUT`
- **Headers**:
  - `x-api-key: your_api_key`
  - `Content-Type: application/json`

### Delete a Vehicle Stop

- **URL**: `/delete-vehicle-stop/:stop_id`
- **Method**: `DELETE`
- **Headers**:
  - `x-api-key: your_api_key`

## Authentication

All endpoints require an API key for authentication. The API key must be included in the request headers:

- **Header**: `x-api-key: your_api_key`
