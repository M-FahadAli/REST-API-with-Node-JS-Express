<h1>REST API for Medical Clinic Database Project (Node JS & Express)</h1>

<img src="1_eb5oE6h-djckn-zp_O1Gvw.jpg" alt="1_eb5oE6h-djckn-zp_O1Gvw.jpg" border="0" />

<h2>Description</h2>
In this comprehensive project, we'll be setting up a RESTful API to manage a database of medical clinics, focusing on patient information. Utilizing a stack comprised of Python and JSON within Visual Studio Code, alongside Node.js and Express for server implementation, we'll create endpoints enabling functionalities like retrieval, creation, updating, and deletion of patient records. To facilitate testing and interaction with our API, we'll leverage Postman, a robust tool for sending and managing data requests. This guide will walk you through each step in detail, ensuring a thorough understanding and seamless execution of the project. So, let's dive in and embark on this journey together!
<br />

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Python</b>
- <b>JSON</b>

<h2>Environments Used </h2>

- <b>Virtual Studio Code</b>
- <b>Postman</b>
- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<p align="center">
To kickstart our project, we'll begin by installing essential packages required for its completion. We'll initialize the Node Package Manager (NPM) by executing the command "npm init", which will guide us through the creation of a package.json file, facilitating dependency management throughout the project. NPM serves as a crucial tool for managing project dependencies, ensuring smooth integration of various components. Let's proceed with the initialization process: <br/>
<img src="Screenshot 2024-02-21 203448.jpg" alt="Screenshot 2024-02-21 203448.jpg" border="0" />
<br />
<br />
To install the necessary packages for our project, we'll utilize NPM, ensuring that Visual Studio Code is running with administrator privileges to execute PowerShell commands: <br/>
<img src="Screenshot 2024-02-21 203751.jpg" alt="Screenshot 2024-02-21 203751.jpg" border="0" />
<br />
<br />
To get started, create a file named index.js in your API folder. This will serve as your Node.js server's entry point. Within index.js, define your API's basic structure, including importing modules and setting up routes. Install nodemon globally or locally to enable automatic server restarts upon file changes. Navigate to the directory containing index.js in your terminal, then run "nodemon index.js" to start the server. It'll run on localhost:3000 by default. With the server running, you can proceed to build your API by adding endpoints and handling requests: <br/>
<img src="Screenshot 2024-02-21 204408.jpg" alt="Screenshot 2024-02-21 204408.jpg" border="0" />
<br />
<br />
Below is the initial outline of our API along with its functionalities. We'll utilize Postman for sending requests to our REST API, including POST, PUT, DELETE, and GET methods. Authentication will be handled via headers, while the request body will serve various purposes (hence the use of bodyParser).  <br/>
<img src="Screenshot 2024-02-21 204809.jpg" alt="Screenshot 2024-02-21 204809.jpg" border="0" />
<br />
<br />
Construct the database for managing medical records and patient information.
 <br/>
<img src="Screenshot 2024-02-21 205523.jpg" alt="Screenshot 2024-02-21 205523.jpg" border="0" />
<br />
<br />
Next, I'll focus on implementing the functionalities. For the GET method, there are specific checks we need to perform before providing the medical records. I've also implemented logging of headers data from Postman to the server to ensure proper data reception.  <br/>
<img src="Screenshot 2024-02-21 210041.jpg" alt="Screenshot 2024-02-21 210041.jpg" border="0" />
<img src="Screenshot 2024-02-21 210342.jpg" alt="Screenshot 2024-02-21 210342.jpg" border="0" />
<br />
<br />
Following that, I've implemented an if statement to validate whether the values in the "sin" header match. If there's no match, the server responds with a status code 404 along with a JSON message stating "Patient not found".  <br/>
<img src="Screenshot 2024-02-21 210507.jpg" alt="Screenshot 2024-02-21 210507.jpg" border="0" />
<br />
<br />
Subsequently, I created another if statement to cross-verify if the provided first name and last name match with the corresponding sin. If successful, the server responds with a status code 200 (OK), providing the medical record along with a JSON message. Otherwise, an error JSON message is returned with status code 401 (Unauthorized).  <br/>
<img src="Screenshot 2024-02-21 202638.jpg" alt="Screenshot 2024-02-21 202638.jpg" border="0" />
<br />
<br />
:  <br/>
<img src="Screenshot 2024-02-21 202837.jpg" alt="Screenshot 2024-02-21 202837.jpg" border="0" />
<br />
<br />
For the next function, we'll utilize the POST method to create a new patient. We aim to verify the new patient's information provided in the header against existing data in the database. If the patient's SIN matches the provided first name, last name, and phone number, the patient will be added to the database with a status code 200 (OK).
<br/>
<img src="image.png" alt="image.png" border="0" />
<br />
<br />
Next, let's create a function to update a patient's phone number. We'll start by verifying the SIN provided in the request. Then, we'll confirm if the first and last names match the SIN in the database. Upon successful verification, we'll utilize the PUT method to update the phone number. Finally, we'll return the updated database in the response body. <br/>
<img src="image.png" alt="image.png" border="0" />
<br />
<br />
Finally, let's implement a function to delete patients and their associated medical records. We'll begin by verifying if the patient's SIN exists in the database. Then, we'll confirm if the provided SIN matches the first and last name associated with it. If the credentials match, we can proceed to delete the patient and their records using the DELETE method. Otherwise, we'll return an error code along with a JSON message indicating that the credentials don't match the SIN on file.
<br/>
<img src="image.png" alt="image.png" border="0" />
<br />
<br />

<br />
In conclusion, the project involved the development of a REST API for a Medical Clinic. Key functionalities included handling GET, POST, PUT, and DELETE methods to manage patient records. Verification checks were implemented to ensure data accuracy and security. Throughout the project, emphasis was placed on robustness and adherence to RESTful principles.  
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
