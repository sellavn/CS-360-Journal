# CS-360-Journal

### Project Goals & Requirements
The requirements of the project was to make an Android application from one of three project ideas, the one I chose being a weight tracker application. The app required functional code to allow for
- Logging in and registration
  - Saving this data to a database
- Developing a functional database shell utilizing SQLite
  - Used to store and display user information on a seperate screen as a grid
  - User being able to use CRUD operations on the data
- Prompting SMS and granting user permission to do so
  - If user denies function the app should continue to work
- Employing industry standard coding practices

The project's goals were slightly different. Ideally, I wanted to have a consistent interface, extra features such as milestones, weight goals, and data visualization other than the database, but I could only implement the requirements aligned above and the main purpose of the app, which is to log weight and view it. 

### Screens
There are 5 screens present. Each has a distinct function, the initial being a login and registration screen. This screen has all the relevant UI elements to facilitate a secure login and registration, such as a textfield that hides the password, and an option to switch between registration and logging in. 
Once inside the app, the dashboard is the landing screen - and this continues once the user is logged in. It shows the current weight in large text towards the center, and just below it is a button that prompts the user to log their weight.
On the bottom is a dock, and that hosts all the relevant screens, Dashboard, Weight Log, Settings and SMS. Each has an icon with the title, and pressing on an icon will lead to that screen.
The SMS and settings screens are the simplest, with the SMS screen asking for permissions to send notifications, and giving options of which notifications to send. The settings screen gives the option to logout or delete the account.
The weight tracking screen shows all the current weight logging data in a grid, as well as the interface to add a new weight entry with an optional comment towards the bottom.

Each screen was made to have a consistent color scheme, typeface, and accesible UI elements so they can be navigated as intended. The dashboard has indentifiable elements and works as intended. The application overall was made to be navigable by every intended user via ease of use and readability.

### Coding
Coding was the final iteration of the project. The project was refactored from the previous iteration which only used the UI elements, I first started with addressing the user authentication by creating classes to manage SQLite operations. Most of this is found in the MainActivity and DatabaseHelper. Then I properly implemented the database for weight tracking, expanding DatabaseHelper further.
The most lengthy part was implementing all the relevant CRUD operations as well as the UI elements for the database operations and ensuring data persistence. The classes are found as WeightEntry and WeightDataActivity.
Next was the SMS notification system, which involved creating permission handling and implementing the SMS sending functionality. I created logic for notification triggers, but ultimately none of them are used since those features weren't implemented. Either way, the app works no matter what the status is.
Lastly were the UI revisions and additions. I added a settings screens to have the ability to logout and remove the login data from the database - deleting the account. I also revised the UI of the dashboard, and made sure the data displayed was the latest from the database. 

### Innovation and Success

The biggest innovation I had to make was moreover deciding to omit features to have a more polished product in the end. Certain features such as the milestones contributed to the goal of the app, but were either not functioning how I expected or degrading the performance of the app - leading to a worse user experience and confusing codebase. I felt that an aspect that was particularily succesful was fulfilling the primary purpose which is weight tracking, and having a clean interface to navigate through.
