# AWS Cognito Authentication Setup

This module handles user authentication for the Ayurveda App using AWS Cognito. It provides a secure authentication flow with features like user registration, login, and token management.

## Features

- User registration and login
- Email verification
- Password recovery
- JWT token management
- Secure session handling
- AWS Amplify integration
- Protected route handling

## Prerequisites

- AWS Account
- Node.js (v14 or higher)
- npm or yarn
- AWS CLI (optional, for configuration)

## AWS Cognito Setup

1. **Create User Pool**

   - Go to AWS Console > Cognito
   - Create a new User Pool
   - Configure required attributes
   - Set up app client
   - Note down Pool ID and Client ID

2. **Configure AWS Credentials**
   ```bash
   aws configure
   # Enter your AWS Access Key ID
   # Enter your AWS Secret Access Key
   # Enter your preferred region
   ```

## Environment Variables

Create a `.env` file:

```env
REACT_APP_AWS_REGION=your_aws_region
REACT_APP_USER_POOL_ID=your_user_pool_id
REACT_APP_CLIENT_ID=your_client_id
```

## Installation

```bash
# Install dependencies
npm install

# Start development server
npm start

# Build for production
npm run build
```

## Project Structure

```
src/
├── components/    # Authentication components
├── config/        # AWS configuration
├── hooks/        # Custom React hooks
└── App.js        # Main component
```

## AWS Amplify Configuration

The project uses AWS Amplify for Cognito integration. Configuration is in `src/index.js`:

```javascript
import { Amplify } from "aws-amplify";

Amplify.configure({
  Auth: {
    region: process.env.REACT_APP_AWS_REGION,
    userPoolId: process.env.REACT_APP_USER_POOL_ID,
    userPoolWebClientId: process.env.REACT_APP_CLIENT_ID,
  },
});
```

## Authentication Flow

1. **User Registration**

   - Email and password collection
   - Email verification
   - Profile completion

2. **User Login**

   - Credential validation
   - Token generation
   - Session management

3. **Token Management**
   - JWT token storage
   - Token refresh
   - Session persistence

## Integration with Main App

1. Configure environment variables
2. Import authentication components
3. Implement protected routes
4. Handle authentication state

## Security Considerations

- Secure token storage
- HTTPS enforcement
- Session timeout handling
- Password policies
- Rate limiting

## Available Scripts

- `npm start` - Start development server
- `npm test` - Run tests
- `npm run build` - Build for production

## Troubleshooting

Common issues and solutions:

1. **Configuration Errors**

   - Verify AWS credentials
   - Check environment variables
   - Validate User Pool settings

2. **Token Issues**

   - Clear local storage
   - Check token expiration
   - Verify refresh token flow

3. **CORS Problems**
   - Configure Cognito settings
   - Check API endpoints
   - Verify domain settings

## Contributing

1. Fork the repository
2. Create your feature branch
3. Install dependencies
4. Make your changes
5. Test thoroughly
6. Create a pull request
