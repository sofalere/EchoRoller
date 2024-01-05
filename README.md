# EchoRoller

## Overview

The EchoRoller is a full-stack application with an Express backend for managing phone numbers and a React frontend for seamless user interaction.

### Backend Deployment

1. **Create a New Web Service on Render:**
   - Visit [Render](https://render.com/) and create a new web service.
   - Ensure that your Express project is in the root directory of your repository.

2. **Build Instructions:**
   - Add the following build instructions in your Render web service settings:
     ```bash
     npm install
     ```

3. **Start Instructions:**
   - Add the following start instructions in your Render web service settings:
     ```bash
     npm start
     ```

4. **Update index.js:**
   - Change the `index.js` file to reflect the current PORT from environmental variables:
     ```javascript
     const PORT = process.env.PORT || 3001;
     app.listen(PORT, () => {
       console.log(`Server running on port ${PORT}`);
     });
     ```

### Frontend Deployment

1. **Change baseURL in services/persons.js:**
   - Update the `baseURL` in `services/persons.js` to:
     ```javascript
     const baseURL = '/api/persons';
     ```

2. **Build Frontend App:**
   - Run the following command in your frontend app:
     ```bash
     npm run build
     ```

3. **Add Build Folder to Backend App:**
   - Move the generated `build` folder from the frontend app to the root directory of the backend app.

4. **Static Middleware for Express:**
   - Add the following static middleware to your Express app to serve the static content:
     ```javascript
     app.use(express.static('build'));
     ```

### Accessing the Deployed App

- Backend API: [https://render-phonebook-8ggf.onrender.com/api/persons](https://render-phonebook-8ggf.onrender.com/api/persons)
