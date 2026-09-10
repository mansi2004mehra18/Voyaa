# Voyaa 🌍

Voyaa is a full-stack travel accommodation platform where users can explore,
create, update, and review travel listings.

The application provides user authentication, listing management,
image uploads, location-based maps, reviews, and persistent data storage.

## 🔗 Live Demo

https://voyaa-ew9a.onrender.com

## ✨ Features

- 🔐 User Authentication
  - User signup and login
  - Logout functionality
  - Session-based authentication using Passport.js
  - Password authentication using Passport Local Mongoose

- 🏠 Listing Management
  - View all available listings
  - Create new listings
  - View detailed listing information
  - Edit listings created by the owner
  - Delete listings created by the owner

- 🖼️ Image Upload
  - Upload listing images
  - Cloudinary integration for image storage
  - Image validation for supported formats

- 📍 Location & Maps
  - Location geocoding using Mapbox
  - Interactive Mapbox map for each listing
  - Listing coordinates stored using GeoJSON

- ⭐ Reviews & Ratings
  - Authenticated users can add reviews
  - 1–5 star ratings
  - Users can delete their own reviews
  - Reviews are associated with their authors

- 🛡️ Authorization & Validation
  - Only authenticated users can create listings and reviews
  - Only listing owners can edit or delete their listings
  - Only review authors can delete their reviews
  - Joi validation for listings and reviews

- 💬 User Feedback
  - Flash messages for successful actions and errors
  - Custom error handling

- 📱 Responsive UI
  - Bootstrap-based responsive interface
  - Font Awesome icons
  - Custom CSS styling

## 🛠️ Tech Stack

### Frontend
- HTML
- CSS
- JavaScript
- EJS
- Bootstrap
- Font Awesome

### Backend
- Node.js
- Express.js
- Express Session
- Passport.js
- Passport Local

### Database
- MongoDB
- MongoDB Atlas
- Mongoose

### APIs & Cloud Services
- Mapbox
- Cloudinary

### Validation & Middleware
- Joi
- Multer
- Method Override
- Connect Mongo
- Connect Flash

### Deployment
- Render

## 🏗️ Project Structure

```text
Voyaa/
│
├── controllers/
│   ├── listings.js
│   ├── reviews.js
│   └── users.js
│
├── models/
│   ├── listing.js
│   ├── review.js
│   └── user.js
│
├── routes/
│   ├── listing.js
│   ├── review.js
│   └── user.js
│
├── views/
│   ├── layouts/
│   ├── listings/
│   ├── users/
│   └── includes/
│
├── public/
│   ├── css/
│   └── js/
│
├── controllers/
├── init/
├── utils/
│
├── app.js
├── middleware.js
├── schema.js
├── cloudConfig.js
├── package.json
└── README.md
```

## 🔑 Core Functionality

### Listings

Each listing contains:

- Title
- Description
- Price
- Location
- Country
- Image
- Owner
- Reviews
- GeoJSON coordinates

Listings are stored in MongoDB using Mongoose.

### Authentication

- Voyaa uses Passport.js with Passport Local Mongoose for authentication.
- Authenticated users can create listings and reviews.
- Authorization middleware ensures that users can only modify or delete resources they own.

### Image Upload

- Listing images are uploaded using Multer and stored on Cloudinary.

### Maps

- Mapbox Geocoding converts a listing's location into geographic coordinates.
- These coordinates are then used to display the listing location on an interactive Mapbox map.

### Reviews

- Users can leave a rating from 1 to 5 stars along with a comment.
- Reviews are associated with both the listing and the user who created them.

## ⚙️ Installation & Setup

### 1. Clone the repository

    git clone https://github.com/mansi2004mehra18/Voyaa.git
    cd Voyaa

### 2. Install dependencies

    npm install

### 3. Create a `.env` file

Add the following environment variables:

    ATLASDB_URL=your_mongodb_atlas_connection_string
    SECRET=your_session_secret
    MAP_TOKEN=your_mapbox_token
    CLOUD_NAME=your_cloudinary_cloud_name
    CLOUD_API_KEY=your_cloudinary_api_key
    CLOUD_API_SECRET=your_cloudinary_api_secret

### 4. Start the application

    node app.js

The application will run on:

    http://localhost:3000

## 🌐 Deployment

The project is deployed using Render.

The production environment uses environment variables for sensitive credentials such as the MongoDB connection string, session secret, Mapbox token, and Cloudinary credentials.

## 🔒 Security

- Sensitive credentials are stored using environment variables.
- Authentication is handled using Passport.js.
- Authorization middleware protects listing and review operations.
- Joi validates incoming listing and review data.
- Session data is stored using MongoDB.

## 📌 Future Improvements

- Implement functional destination search
- Implement listing category filters
- Add booking functionality
- Add user profile pages
- Add wishlist/favorites
- Add advanced search and filtering
- Add pagination for listings
- Improve UI/UX
- Add better image optimization
- Add automated tests

## 👩‍💻 Author

**Mansi Mehra**
