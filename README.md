# 🌍 Travel Bucket List Web Page

A full-stack travel app where users can build their personal list of dream destinations, explore attractions, upload travel photos, and manage profile settings. Designed with modern UI principles and integrated APIs for a rich experience.

## 📆 Project Overview

This application was developed as the final Capstone Project for a Software Development Bootcamp. It combines frontend and backend technologies, user authentication, RESTful API design, and third-party integrations.

### Key Objectives

- Demonstrate full-stack web development proficiency
- Showcase authentication, CRUD operations, API integration, and responsive UI/UX
- Practice professional-level code organization and deployment

## ✨ Features

### ✅ Core Functionality

- **User Authentication**

  - Secure registration with email verification
  - JWT-based login/logout
  - Forgot and reset password

- **Destinations Module**

  - Add/edit/delete destinations
  - Mark as wishlist or visited
  - Auto-fetch related images from Unsplash

- **Profile Management**

  - View stats: total places, favorites
  - Upload up to 12 profile pictures with captions
  - Edit profile info, including birthdate (for age calculation)

- **Explore Module**

  - Search cities and view nearby attractions (OpenTripMap API)
  - Group by categories: interesting places, restaurants, hotels
  - Add nearby places to favorites

- **Responsive Design**

  - Mobile-first layout using Tailwind CSS
  - Visual components via Heroicons and Lucide

- **Notifications**

  - Flash messages and toast notifications on actions

## 🧰 Tech Stack

| Frontend | Backend | Database | Third-Party APIs      |
| -------- | ------- | -------- | --------------------- |
| React    | Express | MongoDB  | OpenTripMap, Unsplash |

- **UI/UX:** Tailwind CSS, Heroicons, Lucide
- **Auth & Security:** JWT, bcrypt, protected routes
- **Environment Management:** dotenv
- **Deployment:** Render, GitHub

## 📁 Project Structure

```bash
├── backend/
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   ├── uploadMiddleware.js
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── destinationController.js
│   │   ├── favoritesController.js
│   │   ├── nearbyController.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Destination.js
│   │   ├── CityPlaces.js
│   │   └── Favorite.js
│   ├── routes/
│   │   ├── auth.js
│   │   ├── destinations.js
│   │   ├── external.js
│   │   ├── favorites.js
│   │   ├── geocode.js
│   │   ├── nearby.js
│   │   ├── quote.js
│   ├── utils/
│   │   ├── geocode.js
│   │   ├── validateDestination.js
│   │   └── validateEmail.js
│   ├── uploads/
│   ├── .env
│   └── server.js

├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── DestinationCard.jsx
│   │   │   ├── DestinationForm.jsx
│   │   │   ├── Loader.jsx
│   │   │   ├── Navbar.jsx
│   │   ├── context/
│   │   │   ├── AuthContext.jsx
│   │   ├── modals/
│   │   │   ├── ChangePasswordModal.jsx
│   │   │   └── PhotoModal.jsx
│   │   ├── pages/
│   │   │   ├── Destinations.jsx
│   │   │   ├── DestinationDetail.jsx
│   │   │   ├── EditDestination.jsx
│   │   │   ├── EditProfile.jsx
│   │   │   ├── Explore.jsx
│   │   │   ├── ForgotPassword.jsx
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── NewDestination.jsx
│   │   │   ├── NotFound.jsx
│   │   │   ├── Profile.jsx
│   │   │   ├── ProfileGallery.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── ResetPassword.jsx
│   │   │   ├── UploadPhoto.jsx
│   │   │   └── VerifyEmail.jsx
│   │   ├── services/
│   │   │   ├── api.js
│   │   │   ├── destinationService.js
│   │   │   └── unsplashService.js
│   │   ├── App.jsx
│   │   ├── index.css
│   │   ├── main.jsx
│   ├── .env
│   ├── eslint.config.js
│   ├── index.html
│   ├── package.json
│   ├── package-lock.json
│   └── vite.config.js

├── .gitignore
├── README.md
├── package.json
├── package-lock.json
└── node_modules/
```

## ⚡ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/jmcg1997/travel-webpage.git
cd travel-webpage
```

### 2. Environment Variables

Create a `.env` file in the backend folder:

```env
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
UNSPLASH_ACCESS_KEY=your_unsplash_key
UNSPLASH_API_URL=https://api.unsplash.com
```

Create a `.env` file in the frontend folder:

```env
VITE_API_URL=http://localhost:5001/api
```

### 3. Install Dependencies

```bash
# Backend
cd backend
npm install
node server.js

# Frontend
cd ../frontend
npm install
npm run dev
```

### 4. Access the App

- Frontend: `http://localhost:5173`
- Backend: `http://localhost:5001/api`

## 🧪 Usage

- Register a new account or log in with an existing one.
- Create, edit, or delete travel destinations.
- Upload travel photos and manage your personal profile.
- Use the Explore section to find nearby attractions.
- Mark destinations as favorites or visited.

## 🚀 Future Improvements

- Public profile sharing and user interactions
- Public sharing of destinations and photo galleries
- Social login integration (Google, GitHub)
- Continuous Deployment with GitHub Actions
- Progressive Web App (PWA) support
- Profile customization: allow users to choose background colors or upload background images
- Expand "Explore" categories:
  - Lodging (where to sleep)
  - Restaurants (where to eat)
  - Local events (concerts, festivals, sports, etc.)

### 🌐 Medium to Long-Term Vision
Introduce advanced social features and user-generated content:
- Follow or friend other users
- Like, comment on, and share destinations and galleries
- Public and private messaging between users
- Share short-form content (similar to Instagram Reels or TikToks)

## Manual Testing

- ✅ All forms validated (login, register, password reset, destinations)
- ✅ API integration tested manually with different user roles
- ✅ Responsiveness checked on mobile and desktop
- ✅ Common errors simulated (e.g. expired token, wrong password, missing data)

The application was also reviewed using Chrome DevTools and error boundaries in React.

## 🙏 Acknowledgements

- Bootcamp instructors and peers
- OpenTripMap API
- Unsplash API
- Tailwind CSS and Heroicons

## 👤 Author

**Jesus M. Camacho**\
[GitHub](https://github.com/jmcg1997)\
[LinkedIn](https://www.linkedin.com/in/jesus-m-camacho-gastelum-29b54118a?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app)

## 🔗 Live Demo

👉 [Visit the Live App](https://travel-webpage-1pyx.onrender.com)


## 📄 License

Educational use only. All API keys are kept secure and excluded from the repository.

