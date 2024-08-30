# Server_DPT

This repository contains the code to setup a B2B application using Node.js and served through Nginx. In this project a multi-stage Docker setup is used to build and deploy the application efficiently.

# Prerequisites
Before you begin, ensure you have the following installed on your local machine:
- Docker
- Node.js (if building locally without Docker)

# B2B Project Structure
b2b-frontend/
├── dist/                   # Built frontend assets
├── src/                    # Source code
├── nginx.conf              # Custom Nginx configuration
├── Dockerfile              # Dockerfile for building the image
├── package.json            # Node.js dependencies and scripts
└── README.md               # Project documentation

## Setup and Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/b2b-frontend.git
2. **Change into the project directory**
    ```bash
   cd b2b-frontend
3. **Install the necessary Node.js dependencies**
    ```bash
   npm install
4. **Build the frontend application**
    ```bash
   npm run build
5. **Build the Docker image**
    ```bash
   docker build -t b2b-frontend:latest
6. **Run the Docker container, serving the application on `http://localhost`**
    ```bash
   docker run -p 80:80 b2b-frontend:latest
