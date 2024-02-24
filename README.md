<h1>REST API for Medical Clinic Database Project (Node JS & Express)</h1>

<img src="https://img.hotimg.com/Screenshot-2024-02-24-at-1.49.49AM.png" alt="Screenshot-2024-02-24-at-1.49.49AM.png" border="0" />

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
<img src="https://img.hotimg.com/Screenshot-2024-02-24-at-1.50.33AM.png" alt="Screenshot-2024-02-24-at-1.50.33AM.png" border="0" />
<br />
<br />
To install the necessary packages for our project, we'll utilize NPM, ensuring that Visual Studio Code is running with administrator privileges to execute PowerShell commands: <br/>
<img src="https://img.hotimg.com/Screenshot-2024-02-24-at-1.51.03AM.png" alt="Screenshot-2024-02-24-at-1.51.03AM.png" border="0" />
<br />
<br />
Create a js file named whatever, in our case index.js in your API folder directory. I then built a simple outline of the API running on localhost port 3000 which I will build on to. Use the command "nodemon index.js" to start the Node JS server.: <br/>
<img src="https://imgur.com/mYdDrgM.png" height="80%" width="80%" alt="set up"/>
<br />
<br />
Here is the outline of the API and its functionalities, as well as the use of Postman to send API request to our REST API (POST, PUT, DELETE, and GET). We will be using header for authentication and body for miscellaneous purposes (reason why I used bodyParser):  <br/>
<img src="https://imgur.com/IuvhRab.png" height="80%" width="80%" alt="set up"/>
<br />
<br />
Build the database for the medical records and the patients:  <br/>
<img src="https://imgur.com/9YZZJq1.png" height="80%" width="80%" alt="set up"/>
<br />
<br />
Now I will begin working on the functionalities, for the GET method there are a couple things we need to verify as shown below before we can provide the medical records. I've also logged the headers data from Postman to my server to test if the data is being recieved correctly:  <br/>
<img src="https://imgur.com/jKDTMRz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/bwIMDYd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then created a if statement which checks to verify that if the values in the "sin" header does not match then respond with a status 404 code using a JSON message "Patient not found".:  <br/>
<img src="https://imgur.com/edFEDXC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Then created another if statement to verify if the firstname and lastname match with the corresponding sin. If successfull return status 200 (OK) with the mediacal record and a JSON message, else return an error JSON message with status 401 (unauthorized):  <br/>
<img src="https://imgur.com/bGWNHPr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
:  <br/>
<img src="https://imgur.com/INiv9Ii.png" height="80%" width="80%" alt="Cyber Attack Event Management"/>
<br />
<br />
For the next function, We will use the POST method to create a new patient we want to be able to assert a new patient from the header to the database. So if the patients sin match equals the firstname, lastname, and phone. then add the patient to the database with a status 200 (OK):  
<br/>
<img src="https://imgur.com/W5alK8v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next create a funtion for updating a patients phone number, we need to verify the sin, verify if the first and last name match the sin, then we can use the PUT method to update the phone number and return the updated database in the body:  <br/>
<img src="https://imgur.com/TkkHxBu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Lastly we will create a funtion to delete patients and medical records, again we need to verify if the patients sin exists in the database, verify if the sin matches with the first and last name, then we are able to delete the patient or records from our database using the DELETE Method. Else return error code with JSON message indicating the credentials don't match the sin on file:  <br/>
<img src="https://imgur.com/vXCpzaR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<br />
This Concludes This REST API for a Medical Clinic Project!
NOTE: You can build on this and add more security layers and conditions as it would be in real life!  <br/>
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
