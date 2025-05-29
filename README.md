🌍 StreetSense

StreetSense is a smart community platform built to help citizens report, track, and manage public issues. It features a clean UI, powerful user roles, and seamless Google authentication to ensure a smooth experience for both users and administrators.

🚀 Features

- User login with Email/Password or Google  
- Report creation with title, description, image, and location  
- Admin dashboard to accept or reject reports  
- Real-time status tracking for submitted reports  
- Multilingual support (English & Sinhala)  
- Role-based access control (Admin, Volunteer, Citizen)  
- Firebase Authentication & Firestore integration  
- Fully responsive design for all devices  

🛠️ Tech Stack

- React.js with Vite  
- Tailwind CSS for styling  
- Firebase Authentication  
- Firebase Firestore (NoSQL database)  
- Firebase Storage (for report images)  
- Firebase Hosting (optional for deployment)  

📦 How to Run Locally

1. Clone the repository:  
2. Install dependencies:  
   npm install

3. Add your Firebase config to a firebase.js file or .env file.

4. Start the development server:  
   npm run dev

🔧 Firebase Configuration Steps

1. Create a Firebase project at https://console.firebase.google.com  
2. Enable Authentication (Email/Password and Google Sign-In)  
3. Enable Firestore Database  
4. Enable Firebase Storage  
5. Add your Firebase credentials into the project:

   const firebaseConfig = {  
   apiKey: "YOUR_API_KEY",  
   authDomain: "YOUR_PROJECT.firebaseapp.com",  
   projectId: "YOUR_PROJECT_ID",  
   storageBucket: "YOUR_PROJECT.appspot.com",  
   messagingSenderId: "XXXXXXX",  
   appId: "YOUR_APP_ID"  
   };

🔒 Firestore Rules (Basic Example)

rules_version = '2';  
service cloud.firestore {  
  match /databases/{database}/documents {  

    match /users/{userId} {  
      allow read, write: if request.auth != null && request.auth.uid == userId;  
    }

    match /reports/{reportId} {  
      allow read, write: if request.auth != null;  
    }

  }  
}

🌐 Live Demo

You can view the project live at:  
https://streetsense-b945c.web.app/

👨‍💻 Built By

LAB Developers  
Crafting smart solutions for communities.  
GitHub: https://github.com/IT22089304  
Website: https://lab-developers.web.app/

📄 License

This project is licensed under the MIT License.
