# 02-09-2024-Full-Stack-App
-------------------------- OUT PUT IN MONGOSH TERMINAL -------------------------------


PS C:\Users\Admin\OneDrive\Desktop\Full-Stack> mongosh
Current Mongosh Log ID: 66d6e7255f2c5ac36a2710bb
Connecting to:          mongodb://127.0.0.1:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+2.3.0
Using MongoDB:          7.0.12
Using Mongosh:          2.3.0

For mongosh info see: https://www.mongodb.com/docs/mongodb-shell/

------
   The server generated these startup warnings when booting
   2024-09-03T12:21:15.434+05:30: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
------

test> use mydatabase
switched to db mydatabase


----------------------------------------- TO FIND ALL USER'S -------------------------------------------------
mydatabase> db.users.find()
[
  {
    _id: ObjectId('66d6b74ae6e7c6f4e0baec7c'),
    username: 'Sai ',
    email: 'sai@gmail.com',
    dateOfBirth: ISODate('2002-05-06T00:00:00.000Z'),
    role: 'Explorer',
    location: 'valsad',
    password: 'Sai12563',
    __v: 0
  },
  {
    _id: ObjectId('66d6b7b52839cdca44be950d'),
    username: 'Jay',
    email: 'jay@gmail.com',
    dateOfBirth: ISODate('2002-06-10T00:00:00.000Z'),
    role: 'Admin',
    location: 'Vapi',
    password: 'Jay543',
    __v: 0
  },
  {
    _id: ObjectId('66d6d0067f45fa1b6156559a'),
    username: 'Roshan',
    email: 'roshan@gmail.com',
    dateOfBirth: ISODate('2007-06-04T00:00:00.000Z'),
    role: 'Explorer',
    location: 'Surat',
    password: 'roshan543',
    __v: 0
  }
]

---------------------------------------- TO FIND ONLY ONE USER BY ID ---------------------------------------------

mydatabase> db.users.findOne({_id: ObjectId("66d6b7b52839cdca44be950d")});
{
  _id: ObjectId('66d6b7b52839cdca44be950d'),
  username: 'Jay',
  email: 'jay@gmail.com',
  dateOfBirth: ISODate('2002-06-10T00:00:00.000Z'),
  role: 'Admin',
  location: 'Vapi',
  password: 'Jay543',
  __v: 0
}


-------------------------------- TO FIND ONLY ONE USER BY NAME ----------------------------------

mydatabase> db.users.find({username:"Roshan"}).toArray();
[
  {
    _id: ObjectId('66d6d0067f45fa1b6156559a'),
    username: 'Roshan',
    email: 'roshan@gmail.com',
    dateOfBirth: ISODate('2007-06-04T00:00:00.000Z'),
    role: 'Explorer',
    location: 'Surat',
    password: 'roshan543',
    __v: 0
  }
]
mydatabase>
# Home Page
![img_20240902](https://github.com/user-attachments/assets/4f0649e6-251e-4e41-9019-d01bd0030eec)
# About Page
![img_20240902(2)](https://github.com/user-attachments/assets/3d28fab1-52e1-44c0-9d8f-15d1d97ee2a0)
# Sign Up Page
![img_20240902(3)](https://github.com/user-attachments/assets/b6a35fd4-f96f-4f0c-b6d6-fc5995a85b8c)
# Login Page
![img_20240902(1)](https://github.com/user-attachments/assets/8d5fa46e-ea74-4fcf-9cd8-3bc2999477a0)
# Output 
![img_20240903](https://github.com/user-attachments/assets/15401e0a-946b-4943-ba09-1c3ac14168bd)


1. **Project Overview**:
   The project is a simple web application with several key functionalities, such as user authentication (login and signup). It consists of various web pages, like a homepage, an about page, a signup page, and a login page.

2. **Backend (Server-Side)**:
   - The backend is built using **Node.js** with the **Express.js** framework. Express helps to define different routes that handle HTTP requests from the client (web browser).
   - The server interacts with **MongoDB**, a NoSQL database, to store and retrieve user information, such as email and password, as part of the user authentication system.
   - **Bcrypt** is used to securely hash user passwords before storing them in the database to ensure security.

3. **User Authentication**:
   - The project includes two key features: **user signup** and **user login**. 
   - During **signup**, users submit their details (like username, email, password, etc.), and the password is hashed before being stored in the MongoDB database.
   - In the **login** process, the user's email and password are validated. The stored hashed password is compared with the one provided by the user to authenticate them. If successful, the user is logged in.

4. **Frontend (Client-Side)**:
   - The web pages are created with **HTML** and **CSS**. The application includes the following key pages:
     - **Home Page**: Welcomes users to the application and provides an overview.
     - **About Page**: Explains the purpose of the project and its key features.
     - **Signup Page**: Allows new users to register by entering details like username, email, password, etc.
     - **Login Page**: Enables registered users to log in by entering their email and password.

5. **Routing**:
   - The server uses various routes to handle requests. For example, when a user navigates to `/signup`, the server responds by rendering the signup page.
   - For **user-specific actions**, there are routes for registering new users, listing all users, and updating or deleting users by their ID.

6. **Error Handling and Validation**:
   - The system ensures that required fields like email and password are provided during login and signup.
   - It checks for issues like **password mismatch** (during signup) and **invalid login credentials** (during login).
   - Errors during server operations (e.g., database connection issues) are handled, and appropriate error messages are displayed.

7. **File Structure**:
   - The public-facing HTML files (like `index.html`, `about.html`, etc.) are served from the `public` directory.
   - Static assets like stylesheets (`style.css`) and images are also stored and served from this directory.








