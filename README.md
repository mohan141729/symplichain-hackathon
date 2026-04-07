# Symplichain Hackathon Submission

## Overview
This repository contains CI/CD pipeline configurations for automated deployment of the Symplichain platform.

## Features
- Automated deployment using GitHub Actions
- Separate workflows for staging and production
- Backend deployment on EC2 (Django)
- Frontend deployment on AWS S3

## Tech Stack
- Django (Backend)
- React (Frontend)
- AWS EC2, S3
- GitHub Actions (CI/CD)

## Workflows

### 1. Staging Deployment
- Trigger: Push to `staging` branch
- Deploys to staging EC2 and S3

### 2. Production Deployment
- Trigger: Push to `main` branch
- Deploys to production EC2 and S3
