# Ayurveda App Frontend

A modern React application built with Vite for the Ayurveda health analysis system. This frontend provides an intuitive interface for users to complete health assessments and receive Ayurvedic recommendations.

## Features

- Modern React with Vite build system
- AWS Cognito integration for authentication
- Responsive design
- Interactive questionnaire interface
- Real-time validation
- Dashboard for health insights
- User profile management

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Backend server running
- AWS Cognito configuration

## Environment Variables

Create a `.env` file in the root directory:

```env
VITE_API_URL=http://localhost:5000
VITE_AWS_REGION=your_aws_region
VITE_COGNITO_USER_POOL_ID=your_user_pool_id
VITE_COGNITO_CLIENT_ID=your_client_id
```

## Installation

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Project Structure

```
src/
├── assets/        # Static assets
├── components/    # Reusable components
├── pages/         # Page components
├── services/      # API services
├── styles/        # CSS styles
├── App.jsx        # Main component
└── main.jsx       # Entry point
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Development

The application uses:

- React for UI components
- Vite for build tooling
- ESLint for code quality
- CSS modules for styling
- Axios for API calls

## Pages

1. **Login/Signup**

   - User authentication
   - Registration flow

2. **Dashboard**

   - User profile
   - Health status overview
   - Recommendations

3. **Questionnaire**
   - Multi-step health assessment
   - Progress tracking
   - Validation

## API Integration

The frontend communicates with the backend through the `apiService.js` module. All API calls are authenticated using JWT tokens from Cognito.

## Contributing

1. Fork the repository
2. Create your feature branch
3. Install dependencies
4. Make your changes
5. Test thoroughly
6. Create a pull request
