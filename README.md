# COMP3810SEF GROUP PROJECT
## Project Information
- Project name: Flight Dashboard
- Group no: 19
- Group memebers: 
  1. 14022297 Lee Sheung Lam
  2. 14011314 Li Kam Yeung
  3. 14078011 Chan Long Hin
  4. 13175765 Mo Yuen Yi
  5. 13218978 Miao Qin Yin

# Project File Introduction
## The Node.js is a Flight Management System with the following functionalities:

### 1. Authentication
- User Registration & Login with username and password

- Session management with express-session

- Login-required middleware for protected routes

### 2. Flight CRUD Operations
- Create: Add new flights with form data and optional photo upload

- Read: View flight list with search functionality & detailed flight views

- Update: Edit existing flight information

- Delete: Remove flights from the system

### 3. Features
- Search: Find flights by flight number, destination, airline, or airports

- File Upload: Store flight photos as base64 in MongoDB

- User Isolation: Each user only sees their own flights

- Sorting: Flights displayed by creation date (newest first)

### 4. RESTful API
- Full CRUD API endpoints 
  ```
  /api/flights
  ```

- Supports JSON responses for integration

- Same authentication requirements as web interface

### 5. Technical Stack
- Backend: Express.js with EJS templating

- Database: MongoDB with MongDB driver

- Middleware: Form handling, session management, method override

- Security: Password hashing, session-based auth

### 6. Pages & Routing
- Main flight listing with search
    ```
    /list
    ```
- Individual flight details
    ```
    /details
    ```
- Flight editing form
    ```
    /edit
    ```
- API testing interface
    ```
    /api-test
    ```
- Authentication pages 
    ```
    /login
    ```
    ```
    /register
    ```
    ```
    /logout
    ```
## Here are the dependencies for this Flight Management System on the PACKAGE.JSON
### Core Dependencies
- Web framework for Node.js
  ```
  "express": "^4.19.2"
  ```
- Template engine for rendering HTML views
  ```
  "ejs": "^3.1.10"
  ```
- MongoDB driver for database operations
  ```
   "mongodb": "^6.8.0"
  ```
### Authentication & Security
- Password hashing for secure authentication
  ```
  "bcrypt": "^5.1.1"
  ```
- Session management for user login state
  ```
  "express-session": "^1.18.0"
  ```
### Form Handling & Middleware
- Form data parsing and file upload handling
  ```
  "express-formidable": "^1.2.0"
  ```
- Allows HTTP verbs like PUT/DELETE in forms
  ```
  "method-override": "^3.0.0"
  ```
### Application Type
- Backend: Express.js server
- Frontend: EJS templates with server-side rendering
- Database: MongoDB
- Architecture: MVC-like pattern with routes, views, and data models

## Public folder
### There are the photos of the airline company

![image](https://github.com/shawnlee0907-source/COMP3810SEF-Group19/blob/main/public/fxZdlMZeDeRFqfNmxEpOoQtLppgppsqszcPcoMpWHrsQItYMWJuRIAasuVwVilCS.png)

![image](https://github.com/shawnlee0907-source/COMP3810SEF-Group19/blob/main/public/Cathay_Pacific_Ltd._logo.svg.png)


### CSS Files
- Main stylesheet
- JavaScript
- Images & Assets
- Fonts & Icons
- Key Styling Features
#### The public folder serves all client-side assets that are referenced in the EJS templates, providing the visual presentation and interactive functionality for the Flight Management System.

## Views folder
- api-test.ejs
- create.ejs
- details.ejs
- edit.ejs
- info.ejs
- list.ejs
- login.ejs
- register.ejs

# Cloud-Based server URL
```
https://comp3810sef-group19-vubv.onrender.com/login
```
# Operation guides 
## login(press URL and use demo account username: 4321 password: 4321)
   
   ![image](https://github.com/mosandesu/createcode/blob/main/pt/loginpage.png)
   ![image](https://github.com/mosandesu/createcode/blob/main/pt/inputuserpassword.png)

## After login(can see the flight info)
   ![image](https://github.com/mosandesu/createcode/blob/main/pt/afterloginpage.png)

## Detail button
   ![image](https://github.com/mosandesu/createcode/blob/main/pt/detail.png)
   After pressing the detail button, and can press the edit button)
   ![image](https://github.com/mosandesu/createcode/blob/main/pt/detailedit.png)
   can edit the flight info
   ![image](https://github.com/mosandesu/createcode/blob/main/pt/detaileditpage.png)
   For example, you can change the flight time
   ![image](https://github.com/mosandesu/createcode/blob/main/pt/detaileditpage(chagethetime).png)
   Change the time then press Update Flight button
   ![image](https://github.com/mosandesu/createcode/blob/main/pt/detaileditpage(chagethetime)forupdate.png)
   Now, can see the updated info (also, you can press "Back to Dashboard" to go back to the homepage)
   ![image](https://github.com/mosandesu/createcode/blob/main/pt/detaileditpage(chagethetime)forupdate(new).png)

## Update
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/edit.png)
  press the button (same function with the detail edit part)
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/edit2.png)

## Delete
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/delet.png)
  after press delete button
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/deletedOK.png)

## Create
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/add.png)
  inter the flight info
  ![iamge](https://github.com/mosandesu/createcode/blob/main/pt/add2.png)
  New flight info inserted
  ![iamge](https://github.com/mosandesu/createcode/blob/main/pt/add3.png)

## Read
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/search.png)
  After press the Search button(come out all the "cathay pacific")
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/search2.png)
  search Hong Kong Airline
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/search3.png)
  press the button
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/search4.png)
  show out all of the Hong Kong Airline

## Logout 
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/logout.png)
  After press the button will go back to login page
  ![image](https://github.com/mosandesu/createcode/blob/main/pt/logout2.png)
  
  
# RESTful CRUL
## Login
```
curl -c cookie.txt -X POST https://comp3810sef-group19-vubv.onrender.com/login \
     -F "username=4321" \
     -F "password=4321"
```
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/login.png)


## Read1
```
curl -b cookie.txt https://comp3810sef-group19-vubv.onrender.com/api/flights | jq
```
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/show1.png)
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/show2.png)
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/show3.png)


## Create
```
curl -b cookie.txt -X POST https://comp3810sef-group19-vubv.onrender.com/api/flights \
     -F "flightNumber=CX225" \
     -F "airline=Cathay Pacific" \
     -F "departureAirport=HKG" \
     -F "arrivalAirport=NRT" 
```
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/create.png)

### Read2(After create)
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/after%20create.png)

### check the CX225(new data)
```
curl -b cookie.txt https://comp3810sef-group19-vubv.onrender.com/api/flights/CX225 | jq
```
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/after%20create2.png)


## Update
```
curl -b cookie.txt -X PUT https://comp3810sef-group19-vubv.onrender.com/api/flights/CX225 \
     -F "status=Delayed" \
     -F "gate=71A"
```
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/update.png)

### Check CX225 after update
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/after%20update.png)

## Delete
```
curl -b cookie.txt -X DELETE https://comp3810sef-group19-vubv.onrender.com/api/flights/CX225
```
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/delete.png)

### check CX255 after deleted
![image](https://github.com/mosandesu/createcode/blob/main/CURL%20pt/after%20delete%20update.png)
