# **FitTrack, your Workout Tracker**

**Live Demo:** [FitTrack](https://fittrack-nanith.vercel.app)

## **Table of Contents**

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)

## **Introduction**

The Workout Tracker is a web application designed to help you track your running and cycling workouts. It allows users to log various workout details such as distance, duration, and location, and visualize them on an interactive map. This project utilizes Leaflet for mapping and offers a simple and intuitive user interface for tracking fitness activities.

## **Features**

- **Add Workouts**: Log new running or cycling workouts with details like distance, duration, cadence for running, and elevation gain for cycling.
- **Interactive Map**: Display workouts on a map with markers and paths to visualize workout routes.
- **View Details**: View detailed metrics for each workout, including pace for running and speed for cycling.
- **Delete Workouts**: Remove workouts from the list and the map.
- **Local Storage**: Persist workout data across sessions using the browser's local storage.
- **Responsive Design**: Optimized for both desktop and mobile use.

## **Installation**

To set up the project locally, follow these steps:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/NANITH777/Workout-Tracker.git
   ```

2. **Navigate to the Project Directory**:

   ```bash
   cd workout-tracker
   ```

3. **Open `index.html`**:
   Open `index.html` in your browser to view the application.

   ```bash
   open index.html
   ```

   Alternatively, you can use a simple HTTP server like `Live Server` in Visual Studio Code to run the application.

## **Usage**

1. **Adding a Workout**:

   - Click on the map to select a location for your workout.
   - Fill out the form with details like distance, duration, and either cadence (for running) or elevation gain (for cycling).
   - Click `Enter` to add the workout. The workout will be displayed on the map as a marker and in the list below the map.

2. **Viewing Workout Details**:

   - Click on a workout in the list to center the map on the corresponding location.
   - Detailed workout metrics are displayed in the list and a popup on the map.

3. **Deleting a Workout**:

   - Click the delete button next to the workout in the list to remove it.
   - The workout will be removed from both the map and the list.

4. **Resetting the Application**:
   - Click the `Reset` button to clear all workouts and reset the application. This action will also remove data from local storage.

## **Code Structure**

- `index.html`: The main HTML file that provides the structure of the application.
- `style.css`: The CSS file for styling the application.
- `app.js`: The main JavaScript file containing the core logic of the application.

### **JavaScript Classes and Functions**

- **Workout**:
  - A base class for workouts, containing common properties and methods.
- **Running**:
  - A subclass for running workouts, which calculates the pace and sets the description.
- **Cycling**:
  - A subclass for cycling workouts, which calculates the speed and sets the description.
- **App**:
  - The main application class, managing the map, form interactions, and local storage.

### **Key Methods in `App` Class**:

- `_getPosition()`: Gets the user's current location and loads the map.
- `_loadMap(position)`: Loads and sets up the map using Leaflet.
- `_showForm(mapE)`: Displays the form for adding a new workout.
- `_hideForm()`: Hides the form after submission.
- `_newWorkout(e)`: Adds a new workout based on the form input.
- `_renderWorkoutMarker(workout)`: Renders a marker for the workout on the map.
- `_renderWorkout(workout)`: Renders workout details in the list.
- `_moveToPopup(e)`: Moves the map view to the selected workout.
- `_setLocalStorage()`: Saves workouts to local storage.
- `_getLocalStorage()`: Retrieves workouts from local storage.
- `_showMessage(message, type)`: Displays a confirmation or error message.

## **Technologies Used**

- **HTML**: Provides the structure for the web application.
- **CSS**: Used for styling the application.
- **JavaScript (ES6)**: The core logic of the application, including classes and event handling.
- **Leaflet**: A JavaScript library for interactive maps.
- **Local Storage**: A browser API for storing workout data persistently.

## **Contributing**

Contributions are welcome! To contribute:

1. Fork the repository.
2. Make your changes and commit them (`git commit -m 'Add new feature'`).
3. Push to the branch (`git push origin feature-branch`).
4. Create a pull request.
