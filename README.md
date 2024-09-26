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








