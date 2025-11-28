# Excel-Analytics-Platform
Upload your Excel files and generate interactive charts and graphs for your file.
<hr>

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Setup & Installation](#setup--installation)
- [Environment Variables](#environment-variables)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [License](#license)

---

## Features
- **Excel Upload & Parsing**: Upload Excel files, parse and view data interactively.
- **Data Visualization**: Multiple chart types (Bar, Line, Pie, Area, Bubble, Radar, Gauge, TreeMap) for analytics.
- **User Authentication**: Auth0 integration for secure login.
- **Saved Charts**: Save, view, and manage custom chart configurations.
- **Explore Charts**: Explore public charts shared by other users.
- **History Tracking**: View and manage file upload and chart history.
- **Notifications**: Real-time notifications for user actions and system events.
- **User Profiles & Settings**: Manage user profile and application settings.
- **Keep Alive**: Server keep-alive and health check endpoints.

## Tech Stack
- **Frontend**: React, Vite, CSS
- **Backend**: Node.js, Express
- **Database**: MongoDB (Atlas)
- **Authentication**: Auth0
- **Other**: ESLint, Render (deployment)

## Setup & Installation

### Prerequisites
- Node.js (v16+ recommended)
- pnpm (or npm/yarn)
- MongoDB Atlas account

### 1. Clone the Repository
```
git clone https://github.com/Harshit800-soni/Excel-Analytics-Platform.git
cd excel-analytics-platform
```

### 2. Install Dependencies
```
pnpm install
```

### 3. Configure Environment Variables
Create a `.env` file in the root directory with the following (see example below):
```
# OAuth Configuration
GITHUB_CLIENT_ID=your_github_client_id_here
GITHUB_CLIENT_SECRET=your_github_client_secret_here
GITHUB_CALLBACK_URL=http://localhost:5000/api/auth/github/callback

GOOGLE_CLIENT_ID=your_google_client_id_here
GOOGLE_CLIENT_SECRET=your_google_client_secret_here
GOOGLE_CALLBACK_URL=http://localhost:5000/api/auth/google/callback

MONGODB_URI= mongodb+srv://harshitsoni1155_db_user:C7RMDFUMbj1YNvgX@cluster0.ug6ihxf.mongodb.net/?appName=Cluster0
```

### 4. Start the Development Servers

#### Frontend
```
pnpm run dev
```

#### Backend
```
#open another terminal
cd server
npm install
node index.js
```

## Project Structure

```
excel-analytics-platform/
├── public/                # Static assets
├── server/                # Backend (Node.js/Express)
│   ├── models/            # Mongoose models
│   ├── routes/            # API routes
│   └── utils/             # Utility functions
├── src/                   # Frontend (React)
│   ├── components/        # React components
│   ├── pages/             # Page components
│   ├── utils/             # Frontend utilities
│   └── config/            # API config
├── .env                   # Environment variables
├── package.json           # Project metadata
└── README.md              # Project documentation
```

## Usage
- Upload Excel files and visualize data with interactive charts.
- Save and manage custom chart configurations.
- View upload and chart history.
- Manage notifications and user profile.

## API Endpoints
The backend exposes RESTful endpoints for file history, notifications, saved charts, user profiles, and health checks. See the `server/routes/` directory for details.

## Environment Variables
See `.env` for required variables. You will need to provide:

- **Auth0 configuration**: Sign up at [Auth0](https://auth0.com/), create an application, and copy your Domain and Client ID into the `.env` file.
- **MongoDB connection string**: Create a cluster at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas), add a database user, and copy your connection string (URI) into the `.env` file.

Do not commit secrets to version control. Refer to `.env.example` or project documentation for variable names and formats.

## License
This project is licensed under the MIT License.
