# Kitchen Nightmares
Kitchen Nightmares is an application that serves Dartmouth students, other Hanover residents’, Dartmouth Dining Services (DDS), and restaurant owners in Hanover by storing data about students and residents’ eating habits and summarizing and visualizing that data for users and DDS/restaurant owners. Hereafter we refer to all establishments where students or Hanover residents can purchase food as ‘restaurants.’ The application provides unique accounts for each user and lets users create, update, and view data about their food purchases they’ve made at restaurants in Hanover. The application provides all users visualizations of where they eat weighted by how often they eat at each restaurant or how much money they spend at each restaurant.

### Requirements
* TkInter
* Access to Data (unfortunately it is hosted on my school's private network)

### Implementation
Users can either log in as a regular user or a restaurant owner. Regular users will log each meal they eat, recording the foods they ate, which food category it belongs to, the restaurant, and the date of their meal. These foods are connected to restaurants/dining establishments both on and off campus. We assume that the users are paying with cash only, and thus transaction costs will be calculated with dollar amounts. Each restaurant may be associated with one user designated the restaurant owner for that restaurant. Restaurant owners are able to add foods to their restaurant’s menu, ‘delete’ foods (by taking them “off menu” without deleting them from the database), and change food items’ prices. Regular users are able to register a new account, however new restaurant owners are only added by the database administrator. 

Implementation is divided at a high level between the frontend, the GUI and data visualization, and the backend API and server. The frontend includes a python graphic user interface written with the TkInter python library and a custom visualization class that uses the matlibplot and seaborn python libraries. The backend is composed of a Node/Express RESTful API and server that connect to our own schema on the sunapee database.

### Example
The user login page
![login](photos/UserLogin.png)

The different options a user has
![options](photos/DifferentSelections.png)

An example of adding a meal
![Meal](photos/AddingMeal.png)

An example Data Visualization
![Data](photos/DataVisualization.png)