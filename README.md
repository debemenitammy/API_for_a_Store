# API_for_a_Store
A Restful API for a store website

This Repository contains a REST API built with Nodejs, Express and MongoDB. This API has several routes and endpoints for different functions described as follows:
1. **Suggestion Route**: This route is found in the *suggestion.route.js* file in the *routes* folder and the following API endpoints are defined in the file: <br> 
- The `/suggest` endpoint: This route is used to suggest an Item in the following Categories described in the model.<br>
- The `/suggested` endpoint: This route is used to get all the suggestions that have been made by the client. <br>
- The `/suggested/:category` endpoint: This route is used to get suggestions according to the categories, that is, it gets all suggestions made for each category specified as a parameter in the URL. <br>

<br>

2. The **Authentication Route**: This route contains all the authentication in the `auth.route.js` file in the `routes` folder which includes the following routes: <br>
- The `/signup` route: This route implements the code defined in the `auth.controllers.js` file in the `controllers` folder. Bcrypt Library was used to authenticate the User's password and JSON WEB TOKEN was used to authorize the User. <br>
- The `/login` route: This route is implemented in the code defined in the `auth.controllers.js` file in the `controllers` folder and is used to ensure that the User is authenticated before allowing the User to sign up. <br>

3. The **Documentation Route**: This route's function is found in the `documentation.controller.js` file in the `controllers` folder and it contains a route handler that responds with the lonk to the API Documentation on Postman. <br>

<br>
**The Model Folder**: This folder cotains two files with their following description: <br>
- The Product.js file: In this file, Mongoose is used to create a Schema for the Item name, description, category, reason and the date the item was generated. <br>
- The User.js file: This file uses mongoose to create a Schema for the User's fullname, email, mobile number, address, gender, password and the date the User was generated. <br>

<br>
**The jwt_generator Folder**: This folder contains the `token.js` file which uses json web token and a secret token from the dotenv file to sign the user and set a time for the token to expire. <br>

<br>
**The verify_middleware Folder**: This folder contains `verify.token.js` file that uses the json web token and secret token to get the token from the header in the request and check if the token is valid and verifies the token. <br>

<br>
**The API Documentation can be found on postman via this link https://explore.postman.com/templates/15198/store**
