# Dealership Reviews Capstone Project

This project is a full-stack Dealership Review application developed as the final Capstone Project for the IBM Full-Stack Developer Professional Certificate.

## Architecture and Technology Stack

The application integrates multiple modern web technologies and microservices:

1. **Frontend (React)**: Dynamic user interface handling dealership listings, dealer details, and review submissions. Built with React and integrated into Django.
2. **Backend (Django)**: Core server-side application that handles authentication, user management, and acts as a proxy for external API requests. Features Django Admin integration for managing `CarMake` and `CarModel` database entries.
3. **Database Microservice (Express & MongoDB)**: A Node.js/Express server that interacts with a MongoDB database to serve dealership locations, metadata, and user reviews via RESTful endpoints.
4. **Sentiment Analysis Microservice (IBM Code Engine)**: A deployed Python microservice that analyzes review text and returns sentiment scores (Positive, Neutral, Negative).

## CI/CD & Deployment

- **GitHub Actions**: Automated continuous integration pipeline configured via `.github/workflows/main.yml` that lints all JavaScript (`jshint`) and Python (`flake8`) code upon push and pull requests.
- **Docker**: The Django application is fully containerized using a custom `Dockerfile` and setup via `entrypoint.sh`.
- **Kubernetes**: Configured for deployment on IBM Cloud using `deployment.yaml`.