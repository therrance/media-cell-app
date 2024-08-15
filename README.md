# Media Cell API Application

This repository contains a full-stack application that includes:

- **Backend**: A FastAPI application that serves an API for querying actions based on codewords and retrieving codewords associated with action IDs.
- **Frontend**: A React-based web UI that allows users to interact with the API by looking up actions by codeword and codewords by action ID.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
  - [Clone the Repository](#clone-the-repository)
  - [Setting Up the Backend](#setting-up-the-backend)
  - [Setting Up the Frontend](#setting-up-the-frontend)
- [Running the Application](#running-the-application)
- [Running Tests](#running-tests)
- [Deployment](#deployment)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)

## Features

- **Lookup Action by Codeword**: Input a codeword to retrieve the associated action ID.
- **Lookup Codewords by Action ID**: Input an action ID to retrieve the associated codewords.
- **CORS Support**: Configured to allow communication between the frontend and backend when served from different origins.
- **Responsive Design**: The frontend UI is built with Tailwind CSS for a modern and responsive design.

## Requirements

- **Python 3.7+**: Required for the FastAPI backend.
- **Node.js 14+**: Required for the React frontend.
- **pip**: Python package installer.
- **npm**: Node package manager (comes with Node.js).

## Installation

### Clone the Repository

To get started, first clone this repository:

```bash
git clone --recurse-submodules https://github.com/your-username/media-cell-app.git
cd media-cell-app
```

### Setting Up the Backend

1. **Navigate to the Backend Directory**:

   ```bash
   cd backend
   ```

2. **Create a Virtual Environment** (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install Backend Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Backend**:

   ```bash
   uvicorn main:app --reload --host 0.0.0.0 --port 3000
   ```

   The backend API will be available at `http://localhost:3000`.

### Setting Up the Frontend

1. **Navigate to the Frontend Directory**:

   ```bash
   cd ../frontend
   ```

2. **Install Frontend Dependencies**:

   ```bash
   npm install
   ```

3. **Run the Frontend**:

   ```bash
   npm start
   ```

   The frontend will be available at `http://localhost:3000`.

## Running the Application

Once both the frontend and backend are set up and running, you can access the application by navigating to `http://localhost` in your web browser.

### Frontend

- **Access**: `http://localhost`
- **Features**:
  - Input a codeword to retrieve the associated action ID.
  - Input an action ID to retrieve the associated codewords.

### Backend

- **API Base URL**: `http://localhost:3000`
- **Endpoints**:
  - `GET /action/{codeword}`: Retrieve the action ID associated with a given codeword.
  - `GET /codewords/{action_id}`: Retrieve the codewords associated with a given action ID.

## Running Tests

### Backend Tests

To run the backend tests:

1. **Navigate to the Backend Directory**:

   ```bash
   cd backend
   ```

2. **Run the Tests**:

   ```bash
   pytest
   ```

### Frontend Tests

To run the frontend tests:

1. **Navigate to the Frontend Directory**:

   ```bash
   cd frontend
   ```

2. **Run the Tests**:

   ```bash
   npm test
   ```

## Deployment

### Frontend

You can build the frontend for production and deploy it to any static hosting service:

1. **Build the Frontend**:

   ```bash
   npm run build
   ```

2. **Deploy the `build` Directory**:

   Use the contents of the `build` directory to deploy on platforms like Netlify, Vercel, GitHub Pages, etc.

### Backend

The backend can be deployed to any platform that supports Python web applications, such as:

- **Heroku**
- **AWS Elastic Beanstalk**
- **Google Cloud Run**
- **Azure App Service**

Ensure that your CORS settings are properly configured for your production environment.

## Troubleshooting

### Common Issues

1. **CORS Issues**:

   - Ensure that CORS is properly configured in the FastAPI backend to allow requests from the frontend origin.

2. **Environment Variables**:

   - Make sure environment variables (like API base URLs) are correctly set up in both the frontend and backend.

3. **Port Conflicts**:
   - Verify that no other applications are using the same ports (`3000` for the backend and frontend).

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request. Contributions are welcome!
