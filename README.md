# **Donor Queue**

A real-time blood donation management system built using the **MERN stack** (MongoDB, Express.js, React.js, Node.js) with responsive and modern user interfaces. This platform provides tailored experiences for donors, organizations, and hospitals to efficiently manage the blood donation process.

## **Features**

- **Donor Interface**: Allows donors to track their donation history and upcoming donation events.
- **Organization Interface**: Enables organizations to manage blood collection processes, view donor data, and schedule drives.
- **Hospital Interface**: Hospitals can monitor blood consumption, check availability, and maintain detailed records of blood usage.
- **Responsive Design**: The user interface is built using **Tailwind CSS** and **Ant Design**, ensuring it works seamlessly across devices.
- **Secure Authentication**: **JWT** (JSON Web Token) is used for secure user authentication.
- **State Management**: The application state is managed using **Redux Toolkit** for efficient handling of complex user actions.

## **Technology Stack**

- **Frontend**: React.js, Tailwind CSS, Ant Design
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT
- **State Management**: Redux Toolkit

## **Installation and Setup**

### **Prerequisites**

Make sure you have the following installed:

- Node.js (v14 or above)
- npm or yarn
- MongoDB

### **Clone the repository**

```bash
git clone https://github.com/Chavi02/DonorQueue.git
cd donor-queue
```

### **Backend Setup**

1. Navigate to the backend directory:

   ```bash
   cd server
   ```

2. Install the required dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the `server` directory and add the following environment variables:

   ```plaintext
   MONGO_URI=your-mongodb-connection-string
   JWT_SECRET=your-jwt-secret
   ```

4. Start the backend server:

   ```bash
   npm start
   ```

   The backend will run on `http://localhost:5000`.

### **Frontend Setup**

1. Navigate to the frontend directory:

   ```bash
   cd client
   ```

2. Install the required dependencies:

   ```bash
   npm install
   ```

3. Start the frontend development server:

   ```bash
   npm start
   ```

   The frontend will run on `http://localhost:3000`.

## **Usage**

1. Open the frontend at `http://localhost:3000`.
2. Users can sign up or log in as **Donors**, **Organizations**, or **Hospitals**.
3. **Donors** can track their donations and receive notifications about upcoming donation drives.
4. **Organizations** can manage blood collection schedules and access donor information.
5. **Hospitals** can view and manage blood supply levels and access detailed records of blood consumption.

## **File Structure**

```plaintext
.
├── client                   # Frontend (React.js)
│   ├── src
│   │   ├── components
│   │   ├── pages
│   │   ├── App.js
│   │   └── ...
│   └── package.json
├── server                   # Backend (Node.js, Express.js)
│   ├── controllers
│   ├── models
│   ├── routes
│   ├── middleware
│   ├── app.js
│   ├── server.js
│   ├── .env
│   └── package.json
└── README.md
```

## **API Endpoints**

### **POST /api/auth/login**

- **Description**: User login with JWT authentication.
- **Request Body**: JSON object containing email and password.
- **Response**: JSON object with a JWT token.

### **POST /api/donations**

- **Description**: Add a new donation record.
- **Request Body**: JSON object with donation details (e.g., donor, date, blood type).
- **Response**: JSON object confirming the donation record has been saved.

## **Environment Variables**

- `MONGO_URI`: MongoDB connection string.
- `JWT_SECRET`: Secret key for signing JWT tokens.

Create a `.env` file in the `server` directory and set up your environment variables:

```plaintext
MONGO_URI=your-mongodb-connection-string
JWT_SECRET=your-jwt-secret
```

## **Future Improvements**

- **Notifications**: Integrate real-time notifications for donors about upcoming blood drives.
- **Analytics Dashboard**: Add an analytics dashboard for organizations and hospitals to view blood donation and consumption trends.
- **Multi-Language Support**: Provide support for multiple languages to make the platform more accessible globally.
