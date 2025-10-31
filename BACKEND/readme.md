# Ayurveda App Backend

The backend server for the Ayurveda App, built with Node.js, Express, and MongoDB. It provides API endpoints for user management, health questionnaires, and Ayurvedic analysis.

## Features

- User authentication with AWS Cognito
- RESTful API endpoints
- MongoDB database integration
- ChatGPT API integration for analysis
- JWT token-based authorization
- Secure user data handling

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- AWS Account with Cognito setup
- ChatGPT API key

## Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
AWS_REGION=your_aws_region
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
COGNITO_USER_POOL_ID=your_cognito_user_pool_id
COGNITO_CLIENT_ID=your_cognito_client_id
OPENAI_API_KEY=your_chatgpt_api_key
```

## Installation

```bash
# Install dependencies
npm install

# Start the server
npm start

# For development with auto-reload
npm run dev
```

## API Endpoints

### Authentication

- `POST /auth/signup` - Register a new user
- `POST /auth/signin` - User login
- `POST /auth/verify` - Verify user email

### User Information

- `POST /user/complete-info` - Complete user profile
- `GET /user/profile` - Get user profile
- `PUT /user/update` - Update user information

### Questionnaire

- `POST /questionnaire/submit` - Submit health questionnaire
- `GET /questionnaire/get` - Get questionnaire details

### Analysis

- `POST /analysis/dosha` - Get dosha analysis
- `GET /analysis/recommendations` - Get health recommendations

## Project Structure

```
backend/
├── config/         # Configuration files
├── controllers/    # Request handlers
├── middleware/     # Custom middleware
├── models/         # Database models
├── routes/         # API routes
└── server.js       # Entry point
```

## Error Handling

The API uses standard HTTP status codes:

- 200: Success
- 400: Bad Request
- 401: Unauthorized
- 403: Forbidden
- 404: Not Found
- 500: Server Error

## Security

- JWT token authentication
- AWS Cognito integration
- Request validation
- Error handling
- Rate limiting

## Development

1. Fork and clone the repository
2. Install dependencies
3. Set up environment variables
4. Run in development mode
5. Test endpoints using Postman or similar tools

## Documentation

For detailed API documentation, refer to the endpoint comments in the route files or the Postman collection (if available).
