# Much-To-Do Application (My-react-app)

This repository contains the frontend and backend components for the Much-To-Do application.

## Project Structure
- `frontend/`: React application built with Vite.
- `backend/`: Golang API service with Docker support.
- `.github/workflows/`: CI/CD pipelines for automated testing and deployment.

## CI/CD Pipeline
This project uses GitHub Actions for CI/CD:
- **Frontend CI/CD**: Automatically builds the React app and deploys to AWS S3.
- **Backend CI/CD**: Builds the Docker image and deploys to AWS EC2.

## Deployment Instructions
### Frontend
1. Navigate to `/frontend`
2. Run `npm install`
3. Run `npm run build`

### Backend
1. Navigate to `/backend`
2. Run `go build -o main .`
3. To build the container: `docker build -t much-to-do-backend .`

## Architecture
This application follows a decoupled architecture, with the frontend served via S3/CloudFront and the backend running as a containerized service on EC2.
