# Ayurveda App

A comprehensive Ayurvedic health analysis application that provides personalized health recommendations based on user data and questionnaire responses. The application uses modern web technologies and AI to deliver accurate Ayurvedic insights.

## Project Structure

The project is divided into three main components:

- [`/BACKEND`](./BACKEND) - Node.js backend server with API endpoints
- [`/FRONTEND/ayurveda-app-frontend`](./FRONTEND/ayurveda-app-frontend) - Main React frontend application
- [`/FRONTEND/cognitoAuthFolder`](./FRONTEND/cognitoAuthFolder) - AWS Cognito authentication implementation

## Features

- User Authentication using AWS Cognito
- Detailed health questionnaire
- Dosha analysis based on user responses
- AI-powered health recommendations using ChatGPT API
- Secure user data management
- Responsive web interface

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- AWS Account (for Cognito authentication)
- MongoDB database

### Setup Steps

1. **Backend Setup**

   ```bash
   cd BACKEND
   npm install
   # Configure environment variables (see Backend README)
   npm start
   ```

2. **Frontend Setup**

   ```bash
   cd FRONTEND/ayurveda-app-frontend
   npm install
   # Configure environment variables (see Frontend README)
   npm run dev
   ```

3. **Cognito Authentication Setup**
   - Follow the setup instructions in the Cognito Auth README
   - Configure AWS credentials
   - Update authentication configuration

## Application Flow

1. **User Authentication**

   - Sign up/Sign in via AWS Cognito
   - Complete user profile information

2. **Health Assessment**

   - Fill out the comprehensive questionnaire
   - Submit responses for analysis

3. **Analysis & Recommendations**
   - Receive dosha analysis results
   - Get personalized health recommendations

## Documentation Links

- [Backend API Documentation](./BACKEND/readme.md)
- [Frontend Application Guide](./FRONTEND/ayurveda-app-frontend/README.md)
- [Authentication Setup Guide](./FRONTEND/cognitoAuthFolder/myapp/README.md)

## Development

- Backend runs on: `http://localhost:5000`
- Frontend runs on: `http://localhost:5173`
- Cognito Auth app runs on: `http://localhost:3000`

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
