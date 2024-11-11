# Sprint Project APIs

This project provides APIs for managing assets and packs for an illustration and 3D illustration website. It includes endpoints for asset and pack upload, update, retrieval, and deletion, as well as user authentication APIs. The project is built with Django and includes API documentation through Postman.

## Technologies Used

Backend: Django ,Django REST Framework
Documentation: Postman
Authentication: JWT-based authentication

## Table of Contents

1. Installation and Setup
2. Authentication Endpoints
3. Dashboard Endpoints

## Installation and Setup

1. Clone the repository. 

2. Create a virtual environment and install dependencies

    ```bash
   python -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt 
    ```

3. Run migrations.
     ```bash
    python manage.py migrate
    ```
4. start server
    ```bash
    python manage.py runserver

    ```
  
## Authentication Endpoints

The following endpoints manage user registration, login, profile, and password management.

  - Register a User: POST /register/
  - Register a Creator: POST /creator-register/
  - User Login: POST /login/
  - User Profile: GET /profile/ (requires authentication)
  - Change Password: POST /changepassword/ (requires authentication)
  -  Send Password Reset Email: POST /send-reset-password-email/
  - Reset Password: POST /reset-password/<uid>/<token>/
  - Verify Email: GET /verify-email/<uidb64>/<token>/
  - Token Refresh: POST /api/token/refresh/

## Dashboard Endpoints
These endpoints manage assets and packs on the dashboard. They enable uploading, updating, retrieving, and deleting assets and packs, as well as filtering by title and tags.

### Asset Endpoints

- Upload Asset: POST /upload-asset/
- Delete Asset: DELETE /delete-asset/
- Update Asset: PUT /update-asset/
- Get All Assets: GET /get-all-assets/
- Get Assets by Title and Tag: GET /get-assets-by-title-and-tag/
- Create from Existing: POST /create-from-existing/

###  Pack Endpoints

- Upload Pack: POST /upload-pack/
- Delete Pack: DELETE /delete-pack/
- Update Pack: PUT /update-pack/
- Get All Packs: GET /get-all-packs/
- Get Packs by Title and Tag: GET /get-packs-by-title-and-tag/

### Additional Endpoints

- Get Tags and Categories: GET /get-tags/
- Get Selected Existing Assets/Packs: GET /get-selected-existing/
