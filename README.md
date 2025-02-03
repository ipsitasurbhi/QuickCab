# QuickCab 🚖  
QuickCab is a modern ride-booking service designed to make transportation easy and convenient. It provides separate login options for users and captains, allowing smooth and efficient interaction between passengers and drivers.  

---

## Features ✨

### For Passengers:
- **Real-Time Ride Requests:** Book rides and track drivers in real-time.
- **Fare Estimation:** View fare estimates before confirming the ride.
- **User Login and Registration:** Users can create an account or log in to book rides easily.
- **User-Friendly Interface:** A seamless frontend built with React JS ensures a smooth user experience.

### For Captains:
- **Ride Requests:** Accept or decline rides with a single tap.
- **Navigation:** Integrated maps for efficient route planning.
- **Profile Management:** Manage personal details, vehicle information, and availability.
- **Captain Login and Management:** Captains can log in to manage their availability and accept ride requests.

---

## 🛠️ Technology Stack  

### Frontend  
- **React JS**: For building a dynamic and responsive user interface.  

### Backend  
- **Node.js**: To handle server-side logic and API interactions.
- **Express.js**: For building APIs, handling routes, and middleware. 

### Database  
- **MongoDB**: A NoSQL database to store user and ride-related data efficiently.  

### Maps  
- Google Maps API / Mapbox for geolocation and navigation.
---

## 🏗️ Installation and Setup  

### Prerequisites  
- Node.js installed  
- MongoDB set up locally or with a cloud provider (e.g., MongoDB Atlas)
- API keys for Google Maps or Mapbox. 

### Steps  
1. Clone the repository:  
   ```bash  
   git clone https://github.com/ipsitasurbhi/quickcab.git  
2. Navigate to the project directory:
   ```bash
   cd quickcab  
3. Install dependencies for the backend:
   ```bash
   cd backend
   npm install  
4. Install dependencies for the frontend:
   ```bash
   cd ../frontend  
   npm install
5. Configure environment variables: Create a .env file and add the following:
   ```bash
   DB_URI=<your-database-uri>
   GOOGLE_MAPS_API_KEY=<your-google-maps-api-key>
   JWT_SECRET=<your-jwt-secret>
7. Start the development servers:
   ```bash
   npx nodemon # for backend
   npm run dev # for frontend
