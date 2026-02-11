📘 README.md

Multi-PC System Monitoring Dashboard with ML-Ready Architecture

⸻

📌 Project Overview

This project is a Multi-PC System Monitoring Dashboard designed to monitor multiple computers simultaneously in real time.
Each monitored PC runs a lightweight client script that collects system metrics and sends them to a centralized backend server.
The backend stores this data in MongoDB Atlas and exposes APIs for a web-based dashboard built using React.

The system is scalable, automated, and ML-ready, making it suitable for labs, organizations, or educational institutions.

⸻

🎯 Problem Statement

In many labs and organizations, system monitoring is performed manually, which:
	•	Consumes time and manpower
	•	Fails to detect performance issues early
	•	Lacks centralized visibility of system health

This project solves these problems by providing:
	•	Automated data collection
	•	Centralized monitoring
	•	Real-time visualization
	•	Support for future Machine Learning enhancements

⸻

🏗 System Architecture

The project follows a three-tier architecture:

Client (PCs) → Backend (API Server) → Frontend (Dashboard)

1️⃣ Client Layer (Node.js)
	•	Installed on each PC to be monitored
	•	Collects system information periodically
	•	Sends data to backend via REST API

2️⃣ Backend Layer (Express + MongoDB)
	•	Receives and stores system data
	•	Manages multiple PCs
	•	Handles inactive system cleanup
	•	Provides APIs to frontend

3️⃣ Frontend Layer (React.js)
	•	Displays all monitored PCs
	•	Shows system usage graphs
	•	Indicates online/offline status
	•	Provides centralized visibility

⸻

📂 Project Folder Structure

🔹 Backend

backend/
│
├── models/
│   └── SystemInfo.js
│
├── routes/
│   └── systemData.js
│
├── server.js
├── package.json
├── package-lock.json
└── README.md

🔹 Client Script

client/
│
├── Client.js
├── package.json
└── package-lock.json

🔹 Frontend

frontend/
│
├── build/
│   ├── static/
│   ├── asset-manifest.json
│   └── index.html
│
├── public/
│   └── index.html
│
├── src/
│   ├── components/
│   │   ├── Dashboard.js
│   │   ├── OverviewChart.js
│   │   └── PCCard.js
│   │
│   ├── utils/
│   │   └── api.js
│   │
│   ├── App.js
│   ├── index.js
│   ├── App.css
│   └── index.css
│
├── package.json
└── package-lock.json


⸻

⚙ Technologies Used

Layer	Technology
Client	Node.js, systeminformation
Backend	Node.js, Express.js
Database	MongoDB Atlas
Frontend	React.js
Deployment (Frontend)	Vercel
Deployment (Backend)	Render
Communication	REST APIs
Charts	Chart.js / Recharts


⸻

📊 Data Collected from Each PC
	•	OS Name
	•	CPU Usage
	•	RAM Usage
	•	Disk Usage
	•	System Uptime
	•	24-Hour Usage Trends
	•	Last Updated Timestamp

⸻

🔄 Data Flow
	1.	Client script collects system metrics
	2.	Data is sent to backend API at fixed intervals
	3.	Backend stores data in MongoDB Atlas
	4.	Frontend fetches data and displays it visually
	5.	Inactive systems are automatically handled

⸻

🧹 Inactive System Handling

To avoid displaying old or unused PCs:
	•	Each system update stores a lastSeen timestamp
	•	Systems are categorized as:
	•	Online
	•	Offline
	•	Inactive
	•	Systems inactive beyond a defined threshold are:
	•	Hidden from dashboard
	•	Automatically deleted from database

This ensures a clean and accurate dashboard.

⸻

🤖 Machine Learning Readiness

The project is designed to support Machine Learning features such as:

ML Feature	Purpose
Usage Prediction	Forecast CPU/RAM usage
Anomaly Detection	Detect abnormal spikes
System Clustering	Group similar PCs
Health Classification	Predict system risk
Idle Detection	Identify unused systems

The historical data stored in MongoDB enables easy ML model integration using Python or Node.js ML libraries.

⸻

🚀 Deployment Details
	•	Frontend: Deployed on Vercel
	•	Backend: Deployed on Render
	•	Database: MongoDB Atlas (Cloud)

The system supports monitoring 40–50+ PCs without architectural changes.

⸻

🧪 Testing
	•	Tested with multiple PCs simultaneously
	•	Verified real-time updates
	•	Confirmed automatic cleanup of inactive systems
	•	Dashboard performance optimized for scalability

⸻

🔮 Future Enhancements
	•	Email / notification alerts
	•	Role-based authentication
	•	ML-based predictive maintenance
	•	Automated system actions
	•	Admin control panel

⸻

👨‍💻 Conclusion

This project provides a robust, scalable, and automated solution for monitoring multiple PCs in real time.
Its modular architecture and ML-ready design make it suitable for real-world deployment and academic evaluation.

⸻
