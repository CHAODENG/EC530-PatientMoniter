# Project2-Patient Monitor Platform
## Mission
Designing a system that could help patients and doctors communicate with each other. Such platform should be used to monitor patients' information and make appointment with doctors.

## 1. User Story
* As Patient
  * Patients could use the system to add or edit their information.
  * Patients could make or edit the appointment through the platform.
  * Patients could get to know about the doctors' information by using Doctor id.
  * Patients could talk to doctors' face-to-face through this platform.
 
* As Doctor
  * Doctors could add or edit their information on the platform.
  * Doctors could check and modify the appointment made by other Patients.
  * Doctors could view Patients' information and help them make appointment on the platform.
  * Doctors could search previous patients' info by using Patient id.
  * Doctors could chat with their patients through the platform.
 
* As Admin
  * Admin could enter the system to get or change the patients' or doctors' information.
  * Admin could help the patients make an appointment with specific doctor.
  * Admin could help the doctors get the information of their patients.
  * Admin could assign the doctor or the device for a patient.
  * Admin could chat with all doctors or all patients.  

## General Data Schema
![image](https://user-images.githubusercontent.com/90479627/156250698-459cf901-0c75-469c-b2f8-ad9c4451bf2a.png)

## Modules
### Device Module
Define Interface for devices to ingest data into the system.  

    Data Fields (including knowing how to attribute the data to a patient).
    Error Conditions.
    Make sure you include Temperature, blood pressure, pulse, oximeter, weight and Glucometer and data your system can handle.
    
At the beginning of the design, I create two .csv file as the database which should be read or written. Below is the core code in these file:  

<img width="960" alt="image" src="https://user-images.githubusercontent.com/90479627/156253726-fb2ad763-4bef-4e7a-8473-a8d6832cfef9.png">
<img width="967" alt="image" src="https://user-images.githubusercontent.com/90479627/156254125-99a86a63-7f59-4325-aa1c-0e2437f582d0.png">

And I write the test code to test the data written from the csv file is correct like below:

<img width="324" alt="image" src="https://user-images.githubusercontent.com/90479627/156255096-ca892839-0d5e-44e7-a768-bdb2d60fa543.png"><img width="445" alt="image" src="https://user-images.githubusercontent.com/90479627/156255131-48a9a8b2-769b-4978-97c4-e38bc55ab452.png">  

### Simple web application
This part is using the flask restful api to design a simple web based on the data used before. Through the web, it could be used to add new patients or new doctors in system and also make the appointment between the doctors and patients. And below is what the home page I have deisgned looks like:  

<img width="1430" alt="image" src="https://user-images.githubusercontent.com/90479627/156257072-192c6992-471f-4a76-a852-1a2342fecb37.png">

* On the platform, patients and doctors could be added to lists:

<img width="800" alt="image" src="https://user-images.githubusercontent.com/90479627/156259189-8a1324d8-89fa-4661-9083-a7f272e14147.png"><img width="800" alt="image" src="https://user-images.githubusercontent.com/90479627/156259244-d59d86bc-f4c3-4043-babd-6c7c0a44821c.png">

* Also all people could make an appointment throught the platform:
<img width="595" alt="image" src="https://user-images.githubusercontent.com/90479627/156259475-0c2a56f7-d4e4-4437-a1ac-23821d80da45.png">

### Chat Module
Designing a person-to-person chat platform so the patients and doctors could communicate with each other more conveniently.

The system is built fully in Django Framework in back-end and HTML, CSS in front-end. The database is using from sqlite3 which is a powerful tool. And all registered users are listed so that all people could talk with each other including patients and doctors:

* The new user could register for their new account.
* The user could talk with anyone on the platform.
* The user could see the chat history by scrolling up the screen.
* The admin could manage all the Chats and Users.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/90479627/157138095-df96301f-b9be-4895-9dba-b4e2ffee0e30.png"><img width="500" alt="image" src="https://user-images.githubusercontent.com/90479627/157138107-10235363-5f16-43b3-ad69-b60556dc1c83.png">


## Todo
Later on...
* Trying to add more attributes for patients and doctors
* Trying to improve the implemented function
* Trying to complete the system based on the user story.

