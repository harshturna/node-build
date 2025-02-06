# Node.js API Boilerplate

A production-ready Node.js REST API boilerplate with Express, MongoDB, and robust error handling set up.

## Features

- **RESTful API Architecture**
- **MongoDB Integration** with Mongoose ODM
- **Request Validation** using Joi
- **Error Handling** with custom API error
- **Logging System** using Winston and Morgan

## Prerequisites

- Node.js (v12 or higher)
- MongoDB
- npm or yarn

## Installation

1. Clone the repository
2. Install dependencies: `npm install`
3. Create a `.env` file in the root directory with:
   - DB_CONNECTION=your_mongodb_connection_string
   - PORT=3000
   - NODE_ENV=development

## Example API endpoints

- `GET /blogs` - Get all blogs
- `POST /blog` - Create a new blog

## Error Handling

The application includes a centralized error handling system that:

- Converts different error types to a consistent `ApiError` format
- Provides detailed error information in development
- Sanitizes error responses in production
- Logs errors appropriately

## Validation

Request validation is implemented using Joi:

- Request body validation
- Environment variables validation
- Custom validation middleware

## Logging

Two types of logging are implemented:

- **Winston**: For application-level logging
- **Morgan**: For HTTP request logging

Logs are stored in:

- Console output (development)
- `logs/access.log` file (HTTP requests)

## Development

Start the development server: `npm run start`
