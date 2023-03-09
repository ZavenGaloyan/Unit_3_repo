
# Unit 3 Project: Gym logging application
 # Criteria A:
 ## Problem definition
My client wants an application that can track their gym progress and workouts in a user-friendly and efficient way. The app should allow users to create a profile, set fitness goals, log their daily exercises, and monitor their progress over time. The user should be able to view and analyze their workout data, including the number of reps, and weights lifted for each exercise. The app should also provide workout recommendations based on the user's fitness level, goals, and progress. The app should be available on both python supporting platforms, and it should have a clean and modern user interface that is easy to use and navigate. The app should be secure and protect users' personal information and workout data.
 ## Success Criteria
1.The app should provide a secure login and sign-up system, allowing users to create a new account or log in using an existing account.

2.The app should provide a clear and organized menu system, allowing users to access different features and functions of the app easily.

3.The app should allow users to easily log their workouts, including the date, time, exercise, reps, and weights lifted.

4.The app should provide detailed statistics and visualizations of users' workout data, including progress over time, improvements in strength.

5.The app should include a calendar system, allowing users to view their workout logs by date during the current month so that they can plan and track their workouts.

6.The app should provide a suggested or explore workout page, allowing users to discover new exercises or workouts to add to their routine.

 ## Rationale for Proposed Soultion
Python is a great programming language for building a workout tracking application as it's known for its simplicity, readability, and ease of use. Python's versatility enables developers to create the logic of the application, such as processing user input, calculating metrics from data, and data visualization. Python's object-oriented programming features allow developers to create reusable code, enhancing maintainability and scalability of the application.

SQL databases can handle the vast amount of data generated by workout logs, including exercises performed, and weight lifted. SQL provides advanced querying capabilities, allowing users to filter and sort their workouts by different criteria such as dates and exercise types. SQL databases also ensure that data is always consistent and accurate. Developers can use an ORM like SQLAlchemy to create and manage a database and easily perform CRUD operations.

Kivy is a Python framework for building graphical user interfaces (GUIs). Its cross-platform support allows for easy development and deployment of the application across multiple platforms such as desktops, tablets, and mobile devices. Kivy provides a range of widgets and tools for building interactive and user-friendly GUIs, such as buttons, labels, text inputs, and drop-down lists. Kivy's graphics engine is based on OpenGL, providing fast and smooth animations and transitions. Kivy also supports touchscreens and multi-touch input, making it ideal for further development of mobile applications. Developers can use the KivyMD library to create a modern-looking interface for their workout tracking application.

Combining Python, SQL databases, and Kivy can provide an efficient and flexible way to build a workout tracking application with a user-friendly GUI interface. Developers can use Python to create the logic of the application, SQL databases to store and manage the workout data, and Kivy to build an interactive and user-friendly GUI. The combination of these tools provides an efficient and scalable way to build a modern-looking application that can help clients achieve their fitness goals by tracking and analyzing their workout progress. Additionally, these tools have a large community and support, providing developers with a wide range of resources and documentation to help them build and maintain the application.
 # Criteria B:
 ## Flow Chart
 <p align="center">
  <img src="https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/Unit_3_flow.drawio%20(2).drawio.png" alt="Example image">
</p>
 
 **Fig-1**: The flow chart above depicts the process that the python program does to enter information that is inputed by the user into the database. The differance in symbols and colors are differant properties and processes that allow the program to compelete the process of entering information. It also includes validation so that the program is less likely to malfunction from the user inputs.  
 ## System Diagram
 ![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/System_diagram.png)
 
  **Fig-2**: The image above shows the system diagram of how the overall program function along with the computer system it was developed upon. It shows the imput deices and the computer hardware. Which are both used to run the python programming language, kivy library, and sql databases. It shows the process by which the computer runs and what aspects of the system it uses to execute the output screen.   
 ## WireFrame Diagram
 ![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/wireframes.jpg)
 
  **Fig-3**: The Wireframe diagram shown above is a visual representation of the layout and design of a user interface. It is a skeletal framework that shows the basic structure of the application without including specific design elements such as colors, fonts, or images. It only shows the user inputs and which screens they lead to with black arrows seen above. If the user where to click on a given button it would correspond to the screen that the arrow is pointing to.  
 ## UML Diagram
  <p align="center">
  <img src="https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/UML.drawio.png" alt="Example image">
</p>
 
  **Fig-4**: The UML (Unified Modeling Language) diagram shown above is a visual representation of the system used in the program by using standardized symbols and notation. The diagram above is a Class diagram to be specific, which is a diagram that shows the structure of a system by defining its classes, attributes, methods, and relationships. it also shows how these classes are connected with the black arrows seen above. 
  ## ER Diagram
 ![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/ER.drawio.png)
 
  **Fig-5**: The ER (Entity-Relationship) diagram above is a type of database diagram that illustrates the relationships between entities in a database. It is used to model the data in a given database and show how the entities in that specifc database are organised and there respective datatypes.  
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
 # Criteria C: Development:
  ## Techniques Used:
  - Kivy
  - Python
  - Matplotlib
  - Relational Databases
  - Datetime
  - Pbkd2f

 ```.py
 class database_worker:
    def __init__(self, name):
        self.connection = sqlite3.connect(name)
        self.cursor = self.connection.cursor()

    def search(self, query):
        result = self.cursor.execute(query).fetchall()
        return result

    def run_save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()
```
**Fig-6**:The code above defines a class called database_worker that provides methods for working with a SQLite database. The search method executes a SQL query using the cursor's execute method and retrieves the results as a list of tuples using the fetchall method. The run_save method executes a SQL query using the cursor's execute method and commits the changes to the database using the connection's commit method. The close method closes the connection to the database using the connection's close method. Overall, this class provides a simple interface for searching and modifying data in a SQLite database.This is a vital part of the program and will be used all throughout the program for simiplifying the process of working with the databases.
```.py
class HomeScreen(MDScreen):
    def open_info(self):
        self.parent.current = "ViewInfo"

    def open_Statistics(self):
        self.parent.current = "Statistics"

    def open_Calender(self):
        self.parent.current = "Calender"
    def open_Explore(self):
        self.parent.current = "Explore"
 ``` 
 **Fig-7**:The code above code defines the class called HomeScreen that inherits from the MDScreen class. It provides four methods:open_info, open_Statistics, open_Calender, and open_Explore, that change the current screen in the app to one of the screens named ViewInfo, Statistics, Calender, or Explore, respectively. The open_info, open_Statistics, open_Calender, and open_Explore methods use the parent attribute to access the parent widget (which is the screen manager) and set the current attribute to the name of the target screen. This causes the app to switch to the target screen, displaying it to the user. This allows for a simple and user frendly home screen for the program.
 ```.kv
 ScreenManager:
    LoginScreen:
        name: "LoginScreen"

    RegistrationScreen:
        name: "RegistrationScreen"

    HomeScreen:
        name: "HomeScreen"

    ViewInfo:
        name: "ViewInfo"
    AddInfo:
        name: "AddInfo"

    Calender:
        name: "Calender"

    Statistics:
        name: "Statistics"

    Explore:
        name: "Explore"
```  
 **Fig-7(2)**: The code above is in the kivy file that works in unison along with the python file. The kivy aboves is what connects with the python code in Fig-7 to manage the screens of the program
 ```.py
 class LoginScreen(MDScreen):

    result = None
    def try_login(self):
        print("User tried to login")
        # Get the input username and password and print it
        uname = self.ids.uname.text
        passwd = self.ids.passwd.text
        hash_test = encrypt_password(passwd)
        if uname != "" and passwd != "":
            query = f"SELECT * from users WHERE username='{uname}' and password='{passwd}'"
            db = database_worker("db_login.db")
            result = db.search(query=query)
            print(result)
            LoginScreen.result = result
            db.close()
            if len(result)==1:
                print("Login successful")
                self.parent.current = "HomeScreen"
                self.ids.uname.text = ""
                self.ids.passwd.text = ""
            else:
                self.ids.welcome.text = "Login incorrect"
        else:
            self.ids.welcome.text = "Fill in all required text boxes"

    def Clear(self):
        self.ids.uname.text = ""
        self.ids.passwd.text = ""
 ```
  **Fig-8**:The code seen above defines the class called LoginScreen that inherits from the MDScreen class. It provides two methods named try_login and Clear, which handle user login attempts and clearing of input fields. The try_login method first retrieves the user input for username and password, and encrypts the password using the encrypt_password function. It then constructs a SQL query to search for a user with matching username and password in a SQLite database called "db_login.db". The query is executed using the database_worker class which was previosly discussed in by Fig-6, and the result is stored in a class-level variable called result. If the query returns exactly one row, the user is considered to have successfully logged in, and the app switches to the "HomeScreen" screen. Otherwise, an error message is displayed.The Clear method is from a button that simply clears the input fields for the username and password, making it easier for the user to put new login credentials.
  
 ```.py
 class RegistrationScreen(MDScreen):
    def try_register(self):
        uname = self.ids.uname.text
        email = self.ids.email.text
        passwd = self.ids.passwd.text
        passwd_check = self.ids.passwd_check.text
        hash = encrypt_password(passwd)
        if uname != "" and passwd != "" and email != "" and passwd != "" and passwd_check != "":
            if len(passwd) > 5:
                if passwd != passwd_check:
                    self.ids.passwd_check.error = True
                else:
                    db = database_worker("db_login.db")
                    query = f"INSERT into users (email, password, username, HASH) values('{email}', '{passwd}','{uname}','{hash}')"
                    db.run_save(query)
                    db.close()
                    print("Registration completed")
                    self.parent.current = "LoginScreen"
                    self.ids.uname.text = ""
                    self.ids.email.text = ""
                    self.ids.passwd.text = ""
                    self.ids.passwd_check.text = ""
            else:
                self.ids.passwd.error = True
        else:
            self.ids.uname.error = True
            self.ids.passwd.error = True
            self.ids.passwd_check.error = True
            self.ids.email.error = True
 ```
 **Fig-9**:The code given above defines a class called RegistrationScreen that inherits from the MDScreen class. It provides a single method called try_register that handles user registration attempts. The try_register method first retrieves the user input for username, email, password, and password confirmation. It then checks if all required fields are filled out and if the password meets the minimum length requirement. If the input passes these checks, the method verifies that the password and password confirmation fields match. If the input passes all checks, the method constructs an SQL query to insert the user's information into a SQLite database called "db_login.db". The query is executed using the database_worker class, and the method switches the app to the LoginScreen screen so that it is easier to log in once the registration has been completed. If any of the input fields fail to pass the required checks, the method highlights the corresponding fields with an error indication. As an added sequrity measure the password is hashed with Pbkd2f SHA256 to encrypt the password when entered into the database
```.kv
<LoginScreen>:
    FitImage:
        source:"gym_background.jpg"
    MDCard:
        size_hint: .6, .8
        pos_hint: {"center_x":.5, "center_y":.5}
        orientation: "vertical"

        MDLabel:
            size_hint: 1,.2
            font_style: "H2"
            text: "Login"
            halign: "center"
            spacing: 0
        MDLabel:
            id: welcome
            size_hint: 1,.1
            font_style: "H2"
            text: "Welcome to your Personalised Gym ledger"
            font_size: "20sp"
            halign: "center"
            spacing: 0

        MDTextField:
            id: uname
            hint_text: "Enter Username or Email"
            icon_right: "account"
            size_hint: .8, .1
            pos_hint: {"center_x":.5}

        MDTextField:
            id:passwd
            hint_text: "Enter password"
            icon_right: "eye-off"
            password: True
            size_hint: .8, .1
            pos_hint: {"center_x":.5}

        MDBoxLayout:
            size_hint: 1,.1

            MDRaisedButton:
                id: login
                text: "Login"
                md_bg_color: "##d50000"
                on_press: root.try_login()
                size_hint: .5, .8
            MDRaisedButton:
                text: "Clear"
                md_bg_color: "#ed8000"
                on_press: root.Clear()
                size_hint: .2, .3
                pos_hint: {"center_y":.99}

            MDRaisedButton:
                text: "Register"
                md_bg_color: "#d50000"
                on_press: root.parent.current = "RegistrationScreen"
                size_hint: .5, .8



<RegistrationScreen>:
    FitImage:
        source:"gym_background.jpg"
    MDCard:
        size_hint: .6, .8
        pos_hint: {"center_x":.5, "center_y":.5}
        orientation: "vertical"

        MDRaisedButton:
            id: Go_back
            text: "Back"
            icon_left: "arrow-left-circle-outline"
            md_bg_color: "#d50000"
            on_press: root.parent.current = "LoginScreen"
            size_hint: .2, .05
            pos_hint: {"center_x":.1, "center_y":1}

        MDLabel:
            size_hint: 1,.1
            font_style: "H4"
            text: "Register"
            halign: "center"

        MDTextField:
            id: uname
            hint_text: "Enter Username "
            icon_right: "account"
            size_hint: .8, .1
            pos_hint: {"center_x":.5}
            helper_text_mode: "on_error"
            helper_text: "Fill in all required boxes(MUST BE MORE THAN 5 CHARACTERS)"


        MDTextField:
            id: email
            hint_text: "Enter email"
            icon_right: "email"
            size_hint: .8, .1
            pos_hint: {"center_x":.5}
            helper_text_mode: "on_error"
            helper_text: "Email must contain @"

        MDTextField:
            id:passwd
            hint_text: "Enter password"
            icon_right: "eye-off"
            password: True
            size_hint: .8, .1
            pos_hint: {"center_x":.5}
            helper_text_mode: "on_error"
            helper_text: "Fill in all required boxes(MUST BE MORE THAN 5 CHARACTERS)"


        MDTextField:
            id:passwd_check
            hint_text: "Re-enter password"
            icon_right: "eye-off"
            password: True
            size_hint: .8, .1
            pos_hint: {"center_x":.5}
            helper_text_mode: "on_error"
            helper_text: "Password DOES not Match"



        MDBoxLayout:
            size_hint: 1,.1

            MDRaisedButton:
                text: "Register"
                md_bg_color: "#d50000"
                on_press: root.try_register()
                size_hint: 1, 1
```
**Fig-10**: The code above is the front end kivy code that correlates to the python code for the login and registration as seen in Fig-8 and Fig-9.
```.py
class ViewInfo(MDScreen):
    #LoginScreen().try_login()
    data_table = None
    def update(self):
        result1 = LoginScreen.result
        user_id = result1[0][0]
        print(user_id)
        db = database_worker("Logging_info.db")
        query = f"SELECT * FROM Data_log WHERE user_id = '{user_id}'"
        data = db.search(query)
        db.close()
        self.data_table.update_row_data(None, data)

    def on_pre_enter(self, *args):
        self.data_table = MDDataTable(
            size_hint=(.7, .7),
            pos_hint={"center_x": .5, "center_y": .55},
            use_pagination=True,
            check=True,
            column_data=[("PersonID", 30), ("Exercise", 20), ("Weight", 20), ("Reps", 20), ("Date", 20), ("User_id",20)]
        )

        self.data_table.bind(on_row_press=self.row_pressed)
        self.data_table.bind(on_check_press=self.check_pressed)
        self.add_widget(self.data_table)
        self.update()

    def row_pressed(self, table, row):
        print("a row was checked ", row.text)
        row.md_bg_color = '#FFFFFFF'

    def check_pressed(self, table, row):
        print("a row was pressed ", row)

    def delete(self):
        rows_checked = self.data_table.get_row_checks()
        print(rows_checked)
        db = database_worker("Logging_info.db")
        for r in rows_checked:
            id = r[0]
            query = f"delete from Data_log where PersonID={id}"
            db.run_save(query)
        db.close()
  ```
**Fig-11**: The code seen above contains the ViewInfo class with connects that inherits from the MDScreen class. It allows the user to interact with a data table that is displayed on the screen. The MDDataTable widget from the KivyMD package is used to create the table. The methods update(), on pre enter(), row pressed(), check pressed(), and delete are all part of the ViewInfo class and are their own respective functions. Using a SQL query, the update() method fetches data from a database and inserts the new values into the table's data. As the screen is about to be displayed, the on pre enter() method is called, which creates the MDDataTable widget, binds its events to the appropriate methods, and adds it to the screen. Essentialy displaying all of the data in the SQL database for the user to interact with.
class Calender(MDScreen):
```.py
    def on_pre_enter(self):
        result1 = LoginScreen.result
        user_id = result1[0][0]
        db = database_worker("Logging_info.db")
        query1 = f"SELECT Dates FROM Data_log WHERE Exercise = 'Squat'AND user_id = '{user_id}'"
        data1 = db.search(query1)
        db.close()
        Squat_days = [datetime.strptime(row[0], '%m/%d/%Y').strftime('%e').lstrip() for row in data1]
        print(Squat_days)
        for d in Squat_days:
            self.ids[f"{d}_day"].md_bg_color = (1, 0, 1, 0.5)
 ```
 **Fig-12(A)**
 ```.kv
 <Calender>:
    FitImage:
        source:"gym_background.jpg"
    MDCard:
        size_hint: .9, .9
        pos_hint: {"center_x":.5, "center_y":.5}
        orientation: "vertical"
    MDLabel:
        size_hint: 1,.1
        font_style: "H2"
        text: "Calendar"
        halign: "center"
        pos_hint: {"center_x":.5, "center_y":.95}
        background_color: (1, 1, 1, 1)
        canvas.before:
            Color:
                rgba: self.background_color
            Rectangle:
                size: self.size
                pos: self.pos
    MDRaisedButton:
        id: Go_back
        text: "Back"
        icon: "account-arrow-left"
        md_bg_color: "#d50000"
        on_press: root.parent.current = "HomeScreen"
        size_hint: .1, .05
        pos_hint: {"center_x":.93, "center_y":.95}
    MDFloatLayout:
        MDGridLayout:
            size_hint: .7, .7
            pos_hint: {'center_x': .5, 'center_y': .5}
            cols: 7
            rows: 7

            # Add a label to each cell of the grid layout
            MDLabel:
                bold: True
                text: "Mon"
                halign: 'center'
            MDLabel:
                bold: True
                text: "Tue"
                halign: 'center'
            MDLabel:
                bold: True
                text: "Web"
                halign: 'center'
            MDLabel:
                bold: True
                text: "Thu"
                halign: 'center'
            MDLabel:
                bold: True
                text: "Fri"
                halign: 'center'
            MDLabel:
                bold: True
                text: "Sat"
                halign: 'center'
            MDLabel:
                bold: True
                text: "Sun"
                halign: 'center'
            MDLabel
                text:''
            MDLabel
                text:''
            MDLabel:
                id: 1_day
                text: '1'
                halign: 'center'
                background_color: (0, 0, 0, 0)
			    canvas.before:
                    Color:
                        rgba: self.background_color
                    Rectangle:
                        size: self.size
                        pos: self.pos
 ```
 
 **Fig-12(B)**
 
**Fig-12**: The code abvoe in Fig-12(A) defines a Calender class that inherits from MDScreen.  The on_pre_enter function is called when the screen is navigated to. It retrieves the user_id from the LoginScreen and queries the Logging_info.db database to retrieve all dates that the user has logged the "Squat" exercise. It then extracts the day of each date and stores them in a list called Squat_days. Finally, the function changes the background color of the MDLabel widgets representing the days in the calendar that the user logged the "Squat" exercise using the md_bg_color attribute of the widget. The code is repeated for all other exerceise in the database. This is why kivy is such an amazing library for such product due to its versitility in tools and methods that can be used(As seen in the kivy code in Fig-12(B).It shows how the kivy is structured with days of the week and number of the day. It repeats for every day in the week). It allowed me to create exactly what the client wanted with zero compremises in a relativtly logical manner. 
```.py
class Statistics(MDScreen):
    def __init__(self, *args, **kwargs):

        super().__init__(*args, **kwargs)
        self.exercise = None


    def spinner_click(self, value):
        print(value.text)
        self.exercise = value.text

    def stat_graph(self):
        result1 = LoginScreen.result
        user_id = result1[0][0]
        if self.exercise == "Bench Press":
            Benchpress = []
            db = database_worker("Logging_info.db")
            query4 = f"SELECT Weight FROM Data_log WHERE Exercise = 'Bench Press' AND user_id = '{user_id}'"
            data4 = db.search(query4)
            db.close()
            Benchpress.append(data4)
            flat_list = []
            for item in Benchpress[0]:
                value = item[0]  # extract the first (and only) element of the tuple
                flat_list.append(value)

            self.bench_list = flat_list
            print(self.bench_list)

            print(flat_list)
            plt.ion()
            plt.plot(flat_list)
            plt.title('Bench Press Progression')
            plt.xlabel('Overall Entries')
            plt.ylabel('WEIGHT(KG)')
            plt.show(block=True)
        if self.exercise == "Squat":
            Squat = []
            db = database_worker("Logging_info.db")
            query4 = f"SELECT Weight FROM Data_log WHERE Exercise = 'Squat'AND user_id = '{user_id}'"
            data4 = db.search(query4)
            db.close()
            Squat.append(data4)
            flat_list1 = []
            for item in Squat[0]:
                value = item[0]  # extract the first (and only) element of the tuple
                flat_list1.append(value)
            print(flat_list1)
            plt.ion()
            plt.plot(flat_list1)
            plt.title('Squat Progression')
            plt.xlabel('Overall Entries')
            plt.ylabel('WEIGHT(KG)')

            plt.show(block=True)
```
**Fig-13(A)**


![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/Screenshot%202023-03-09%20225236.png)

**Fig-13(B)**

**Fig-13**:The Statistics class shown above inherits from the MDScreen. First It initializes with no assigned value to the exercise variable. Then there is a spinner_click method that takes in a value argument which is equal to the option chosen in the program and assigns its text attribute to the exercise variable. This was down so that the value of the exercise variable can be inherited later.Then there is a stat_graph method that fetches data from a database based on the exercise variable value. If exercise is "Bench Press", it fetches the weight data of bench press exercises and saves it in a bench_list variable. Then, it plots the bench_list values on a matplotlib graph titled 'Bench Press Progression'. This is the particular code if exercise is equal to "Squat", it fetches the weight data of squat exercises and saves it in a flat_list1 variable. This is done for every exercise in the database similary to the method used in(Fig-12). Then, it plots the flat_list1 values on a matplotlib graph titled 'Squat Progression'(Seen above in Fig-13(B)). Both graphs have Overall Entries on the x-axis and WEIGHT(KG)' on the y-axis. The plt.show(block=True) line at the end of each conditional statement ensures that the graph stays open and visible until the user closes it.

 # Criteria D:
 ## Citation

 https://www.muscleandstrength.com/articles/arnold-schwarzenegger-superset-workout:
Muscle and Strength. "Arnold Schwarzenegger Superset Workout Program." Accessed on March 9, 2023.

https://revolutionaryprogramdesign.com/ronnie-coleman-training-program/:
Revolutionary Program Design. "Ronnie Coleman Training Program." Accessed on March 9, 2023.

https://www.shape.com/celebrities/celebrity-workouts/i-worked-out-dwayne-rock-johnson#:~:text=The%20Rock's%20Workout%20Routine,and%20seven%20are%20rest%20days.:
Shape. "I Worked Out Like Dwayne 'The Rock' Johnson for 3 Weeks—Here's What Happened." Accessed on March 9, 2023.

https://gymtalk.com/rich-piana-8-hour-arm-workout/:
GymTalk. "The Rich Piana 8 Hour Arm Workout." Accessed on March 9, 2023.

https://www.sportskeeda.com/health-and-fitness/cbum-workout-split-olympia-winner-chris-bumstead-s-training-split-explained:
Sportskeeda. "CBum Workout Split: Olympia Winner Chris Bumstead's Training Split Explained." Accessed on March 9, 2023.

https://chat.openai.com/chat:
OpenAI. "OpenAI Chat." Accessed on March 9, 2023.

https://stackoverflow.com/questions/37422382/python-kivy-underline-not-working-in-label:
Stack Overflow. "Python Kivy Underline Not Working in Label." Accessed on March 9, 2023.

https://stackoverflow.com/questions/48347569/kivy-limit-values-on-inputtext:
Stack Overflow. "Kivy Limit Values on InputText." Accessed on March 9, 2023.

https://stackoverflow.com/questions/44403466/kivy-how-to-add-padding-to-a-text-input:
Stack Overflow. "Kivy: How to Add Padding to a Text Input." Accessed on March 9, 2023.

https://www.geeksforgeeks.org/python-popup-widget-in-kivy/:
GeeksforGeeks. "Python | Popup Widget in Kivy." Accessed on March 9, 2023.

https://www.w3schools.com/python/python_inheritance.asp:
w3schools. "Python Inheritance." Accessed on March 9, 2023.

https://realpython.com/python-sqlite-sqlalchemy/:
Real Python. "Python SQLite: A Thorough Guide." Accessed on March 9, 2023.

https://www.programiz.com/python-programming/datetime:
Programiz. "Python Datetime Module." Accessed on March 9, 2023.

https://docs.python.org/3/library/datetime.html:
Python Software Foundation. "datetime — Basic Date and Time Types." Accessed on March 9, 2023.


 <p align="center">
  <img src="https://user-images.githubusercontent.com/111752809/222432502-b2e72ffb-a37d-43f1-8a2e-28ebd6752da8.gif" alt="Example image">
</p>


