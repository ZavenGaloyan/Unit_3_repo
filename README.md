# Unit 3 Project: Gym logging application
![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/atthegym.jpg)

 # Criteria A:
 ## Problem definition
My client wants an application that can track their gym progress and workouts in a user-friendly and efficient way. The app should allow users to create a profile, set fitness goals, log their daily exercises, and monitor their progress over time. The user should be able to view and analyze their workout data, including the number of reps, and weights lifted for each exercise. The app should also provide workout recommendations based on the user's fitness level, goals, and progress. The app should be available on both python supporting platforms, and it should have a clean and modern user interface that is easy to use and navigate. The app should be secure and protect users' personal information and workout data.
 ## Success Criteria
1.The app should provide a secure login and sign-up system, allowing users to create a new account or log in using an existing account.

2.The app should provide a clear and organized menu system, allowing users to access different features and functions of the app easily.

3.The app should allow users to easily log their workouts, including the date, time, exercise, reps, and weights lifted.

4.The app should provide detailed statistics and visualizations of users' workout data, including progress over time, improvements in strength.

5.The app should include a calendar system, allowing users to view their workout logs by date and track their progress over time.

6.The app should provide a suggested or explore workout page, allowing users to discover new exercises or workouts to add to their routine.

 ## Rationale for Proposed Soultion
Python is a great programming language for building a workout tracking application as it's known for its simplicity, readability, and ease of use. Python's versatility enables developers to create the logic of the application, such as processing user input, calculating metrics from data, and data visualization. Python's object-oriented programming features allow developers to create reusable code, enhancing maintainability and scalability of the application.

SQL databases can handle the vast amount of data generated by workout logs, including exercises performed, and weight lifted. SQL provides advanced querying capabilities, allowing users to filter and sort their workouts by different criteria such as dates and exercise types. SQL databases also ensure that data is always consistent and accurate. Developers can use an ORM like SQLAlchemy to create and manage a database and easily perform CRUD operations.

Kivy is a Python framework for building graphical user interfaces (GUIs). Its cross-platform support allows for easy development and deployment of the application across multiple platforms such as desktops, tablets, and mobile devices. Kivy provides a range of widgets and tools for building interactive and user-friendly GUIs, such as buttons, labels, text inputs, and drop-down lists. Kivy's graphics engine is based on OpenGL, providing fast and smooth animations and transitions. Kivy also supports touchscreens and multi-touch input, making it ideal for further development of mobile applications. Developers can use the KivyMD library to create a modern-looking interface for their workout tracking application.

Combining Python, SQL databases, and Kivy can provide an efficient and flexible way to build a workout tracking application with a user-friendly GUI interface. Developers can use Python to create the logic of the application, SQL databases to store and manage the workout data, and Kivy to build an interactive and user-friendly GUI. The combination of these tools provides an efficient and scalable way to build a modern-looking application that can help clients achieve their fitness goals by tracking and analyzing their workout progress. Additionally, these tools have a large community and support, providing developers with a wide range of resources and documentation to help them build and maintain the application.
 # Criteria B:
 ## Flow Chart
 ![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/Unit_3_flow.drawio.png)
 ## Record of tasks
|    | Planned Action                                            | Planned Outcome                                                                                                                                         | Design Cycle      | Time Estimate      | Completion Date | Criteria |
|----|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|--------------------|-----------------|----------|
| 1  | First meeting with myy client                             | Understand the clients issue and their  needs and requirements                                                                                          | Planning          | 15 minutes         | Feb 17,         | A        |
| 2  | Create a Problem Defintion                                | To have all of the requirements of the client written down                                                                                              | Planning          | 45 minutes         | Feb 17,         | A        |
| 3  | Create a Success Criteria                                 | Create a set of goals for the project to accomplish it successfully                                                                                     | Planning          | 20 minutes         | Feb 18,         | A        |
| 4  | Second meeting with client                                | To update and changes that need to be made on the succes criteria                                                                                       | Planning          | 15 minutes         | Feb 20,         | A        |
| 5  | Complete Rationale for the Proposed solution and Criteria | How understand the resoning behind the project and resources required                                                                                   | Planning          | 30 minutes         | Feb 21,         | A        |
| 6  | Creating flowcharts                                       | To create a flow chart describing a certain aspect of the code with sudo code                                                                           | Solution Overview | 1  hour            | Feb 23,         | B        |
| 7  | Creating wireframe diagram                                | To create a wire frame diagram to show the app works with the differant screens                                                                         | Solution Overview | 1 hours 30 minutes | Feb 24,         | B        |
| 8  | Creating system diagram                                   | To show how the overall apps works with the computer system that it is operating on                                                                     | Solution Overview | 1 hour             | Feb 24,         | B        |
| 9  | Creating ER diagram                                       | To show an entity relation diagram of the code                                                                                                          | Solution Overview | 30 minutes         | Feb 25,         | B        |
| 10 | Creating UML diagram                                      | It is used for visually representing a system along with its main actors, roles, actions, artifacts or classes                                          | Solution Overview | 1 hour 45          | Feb 26 ,        | B        |
| 11 | Adding descriptions to Criteria B                         | This will explain all of the aspects of Criteria B so it is easy to understand for the user                                                             | Solution Overview | 1 hour             | Feb 26 ,        | B        |
| 12 | Creating Test Plan                                        | This will be used to test the functionality of the product that I have come up with                                                                     | Solution Overview | 2 hours            | Feb 27 ,        | B        |
| 13 | Login and registration                                    | To have a functional GUI Login and registration system that connected to an SQL database                                                                | Development       | 2 hours            | march 4,        | C        |
| 14 | Create a Home screen that contains the nessisary criteria | How have a user friendly UI for the client to navigate                                                                                                  | Development       | 30 minutes         | march 4,        | C        |
| 15 | Creating a logging page                                   | This provides a space for the client to see their gmy logs directly from the database. To which they may add logs through and add information page      | Development       | 3 hours            | march 4,        | C        |
| 16 | Creating a Calender Page                                  | This will allow the user to visualize what workout they completed during that month and the specific days they happened.                                | Development       | 3 hours            | march 4,        | C        |
| 17 | Connecting database to Calendar                           | This will sync any inputs in the logs to a calendar                                                                                                     | Development       | 4 hours            | march 5,        | C        |
| 18 | Explore page                                              | This is a place where users can come to see their favorite influencers training programs and see if they would like to implement them in their training | Development       | 2 hours            | march 5,        | C        |
| 19 | Adding astetics to the page                               | To make overall app more visaully apealing                                                                                                              | Development       | 30 min             | march 5,        | C        |
| 20 | Validation regarding user inputs                          | To make sure that he app doesn't encounter an error if it were to crash                                                                                 | Development       | 3 hours            | march 5,        | C        |
| 21 | Statistics page written stats                             | To create written statistics based off of the user inputs on their gym progress                                                                         | Development       | 2 hours            | march 6,        | C        |
| 22 | Statistics page visaul stats                              | Providing a visul representaion of the users progression in working out based off of their inputs                                                       | Development       | 2 hours       
 
![curls-gym](https://user-images.githubusercontent.com/111752809/222432502-b2e72ffb-a37d-43f1-8a2e-28ebd6752da8.gif)

 ## SOURCE
 https://www.pngegg.com/it/png-zugos
 https://www.muscleandstrength.com/articles/arnold-schwarzenegger-superset-workout
 https://revolutionaryprogramdesign.com/ronnie-coleman-training-program/
 https://www.shape.com/celebrities/celebrity-workouts/i-worked-out-dwayne-rock-johnson#:~:text=The%20Rock's%20Workout%20Routine,and%20seven%20are%20rest%20days.
 https://gymtalk.com/rich-piana-8-hour-arm-workout/
 https://www.sportskeeda.com/health-and-fitness/cbum-workout-split-olympia-winner-chris-bumstead-s-training-split-explained
