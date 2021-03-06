
# Software Requirements Specification for SchoolBook

**Prepared by:** 

Clayton R Samson, Justin A Bougere, Nicholas A Dugal, Sean M Marino, Soh Guo Hao Steffano, Zachary J Robicheaux

**Date Prepared: 10/19/2016**


| Table of Contents         |
| --- |
| **1. Introduction**                 |
|      1.1        Purpose        |
|      1.2        Document Conventions        |
|      1.3        Intended Audience and Reading Suggestions        |
|      1.4        Product Scope        |
|      1.5        References        |
| **2. Overall Description**   |
|      2.1        Product Perspective        |
|      2.2        Product Functions        |
|      2.3        User Classes and Characteristics        |
|      2.4        Operating Environment        |
|      2.5        Design and Implementation Constraints        |
|      2.6        User Documentation        |
|      2.7        Assumptions and Dependencies        |
| **3. External Interface Requirements** |
|      3.1        User Interfaces        |
|      3.2        Hardware Interfaces        |
|      3.3        Software Interfaces        |
|      3.4        Communications Interfaces        |
| **4. System Features** |
|      4.1.1        Registration       |
|      4.1.2        Login        |
|      4.1.3        Password Reset        |
|      4.2.1        Update Profile        |
|      4.2.2        Add Course        |
|      4.2.3        Register as Tutor        |
|      4.3.1        Create Study Group         |
|      4.3.2        Search for study Group        |
|      4.3.3        Join Study Group        |
|      4.3.4        Leave Study Group        |
|      4.4.1        Upload Notes        |
|      4.4.2        Search for Notes        |
| **5. Other Non-Functional Requirements** |
|      5.1        Performance Requirements        |
|      5.2        Safety Requirements        |
|      5.3        Security Requirements        |
|      5.4        Software Quality Attributes        |
|      5.5        Business Rules        |
| **Appendix A: Analysis Models**         |
| **Appendix B: To Be Determined List**         |



Revision History

| Name | Date | Reason for Changes | Version |
| --- | --- | --- | --- |
|   |  |   |   |
|   |  |  |   |


# 1.Introduction

## 1.1Purpose

The product that will have its requirements specified in this document is SchoolBook. This document will be specifying version 1.0 of SchoolBook.

## 1.2Document Conventions

Functional requirements are denoted by FR4.x.x. For example:
1. FR4.1.x : Registration/Login Management
2. FR4.2.x : User Profile Management
3. FR4.3.x : Study Group Management
4. FR4.4.x : Notes Management


Use Cases are denoted by UC4.x.x. For example:
1. UC4.1.x : Registration/Login Management
2. UC4.2.x : User Profile Management
3. UC4.3.x : Study Group Management
4. UC4.4.x : Notes Management

Non-Functional Requirements are denoted by NF-x For example::
1. NF- 5.3.1: Security requirements for sensitive information.


## 1.3Intended Audience and Reading Suggestions

This document is intended solely for the developers of SchoolBook. It is recommended that developers read through this doc in order to gain a full understanding of the system. The rest of the document is organized in this respective order: An overall description, external interface requirements, a list and explanation of features, non-functional requirements, and other requirements.

## 1.4Product Scope

SchoolBook was produced to augment the studies of college students. This was done by providing students easy access to study groups and other students notes.

## 1.5References

There are no documents that this SRS document refers to.

# 2.Overall Description

## 2.1Product Perspective

SchoolBook is a new, self-contained product that was developed by a group of LSU Computer Science students.

## 2.2Product Functions

| **no.** | **Functions** |
| --- | --------- |
|4.1.1.   |Registration - Users register an account to SchoolBook                                                         |
|4.1.2.   |Login - Users enter their email and password to enter the SchoolBook application                               |
|4.1.3.   |Password Reset - Users enter their email in order to receive their new password                                |
|4.2.1.   |Update Profile - Users enter/edit their account information after a password prompt                            |
|4.2.2.   |Add Course - Users click the add button on a course, which adds said course to the users course list           |
|4.2.3.   |Register as Tutor - During registration a user can choose to be a tutor rather than a student                  |
|4.3.1.   |Create Study Group - Users enter class, location and meeting times to create a study group                     |
|4.3.2.   |Search for Study Group - Users will enter the class number and will be to a list of Study Groups for said class|
|4.3.3.   |Join Study Group - User is added to a list of users in the study group                                         |
|4.3.4.   |Leave Study Group - User is removed from the list of users in that study group                                 |
|4.4.1    |Upload Notes - Users can either drag and drop or browse through their system for notes to upload               |
|4.4.2    |Search for Notes - Users will enter a keyword, then will be brought to a list of notes that have that keyword  |

## 2.3User Classes and Characteristics

| **User** | **Description** |
|   ---       |    ---------    |
| Students   | A Student User will create an account with SchoolBook & consume the various services that are provided by School Book, a Student user will interact with the system through the web application |
| Student Tutor | A Student tutor extends from a student, after submitting proof / verification, a student may be a tutor for a certain course that he or she has completed, a Student Tutor user will interact with the system through the web application |
| Administrator | An administrator will have direct access to the database so that they are able to access and approve tutor applications submitted by student user, an administrator will be running scripts from the database workbench to perform the validation |

## 2.4Operating Environment

Since SchoolBook is a webapp, this application can be used by any OS, as long as the Internet browser is up to date.

## 2.5Design and Implementation Constraints

SchoolBook is to be developed as a web application using ASP.NET 4.0 Frame Work and programmed in c#, it should be programmed to be uniform across different browsers.

Schoolbook is to be designed to maximize interactivity by using HTML, CSS, JavaScript & jQuery.

## 2.6User Documentation

There are no user documents currently.

## 2.7Assumptions and Dependencies

It is assumed that all developers will have access to Visual Studios 2015 & MySQL community server 5.7 to develop this application.

# 3.External Interface Requirements

## 3.1User Interfaces
All objects' layout properties are percentage values set according to the resolution of the user’s screen. This allows each screen's contents to self-arrange themselves for any given screen size. All objects are given minimum dimension constraints to avoid being too small for a user. The structure and display for each screen follows W3C's HTML and CSS guidelines. Errors messages and notifications follow the MSDN guidelines. User Interfaces are needed for registration, login, tutor registration, uploading and searching notes, password reset, joining, searching, and leaving study groups, updating profile, and creating study group. Fig 1.1 below is the introductory page of School Book.

![alt tag](https://raw.githubusercontent.com/ndugal6/SchoolBook/master/SRSimgs/SS_min.png)
Fig 1.1

## 3.2Hardware Interfaces
SchoolBook is able to run on any device with a browser supporting HTML5 and CSS3. The site can receive both physical and touch input. The backend database is run on a Linux server using MYSQL 5.7.17. SchoolBook will allow notes stored on the server to be downloaded to user's local machines. 

## 3.3Software Interfaces
SchoolBook's front-end is developed on Xamarin Studio 6.1.1 using HTML5 and CSS3 libraries for display and content structure. The front-end uses a .cs file to connect and transfers data to the backend Linux server using MYSQL 5.7.17. The front-end sends user credentials for authentication to the server. If user is authorized, then the server relays and populates the client with information surrounding the user's study groups - Date/Time, location, students, and student tutors - and available notes - course ID/Name, upload date, upload user. If the user isn't authorized then the front-end .cs file sends user data needed for student creation to the server: email, password, university, current courses. 

## 3.4Communications Interfaces
Schoolbook will communicate with the server using HTTP protocols. The database uses .cs files to retrieve data from the HTML front-end. Data traffic will follow AES standards for security. The .cs communicate line allows the source code to be hidden from clients.

# 4.System Features

In this section, the various system features of SchoolBook will be explained, SchoolBook is separated into the following:
1. 4.1.x : Login/Registration Management
2. 4.2.x : User Profile Management
3. 4.3.x : Study Group Management
4. 4.4.x : Notes Management.

Each portion will be explained in the following format:

a. Description and priority of the system feature

b. How the interaction between User and server will take place, stimulus from the User and response for the server.

c. Functional requirements table

d. Use Case for the System Feature

## 4.1.1 Registration

a. Description and Priority

Allows new users to register an account with SchoolBook to gain access to the various functions and information available. This Requirement should be of high priority as users would need to have an account before they are able to consume any services from SchoolBook.

b. Stimulus/Response Sequences
1. User Visits SchoolBook URL www.SchoolBook.com.
2. System displays introductory page which contains the Registration Button.
3. User Clicks on the Registration button.
4. System will respond by displaying the registration form.
5. User fills up registration form with fields: Email-Address, Password, Confirm Email-Address, Confirm Password, Date of Birth, Full      Name, Gender and University.
6. User Clicks on register button after form is filled.
7. System will check input data for error.
8. System will display success / failure message; a confirmation email will be sent to user upon success.

c. Functional Requirements

| **Title**        |  **Description** |
|  ----            |     -----               |
| **Item**         |  FR-4.1.1: Registration |
| **Summary**      | The system should provide a Registration feature to allow users to create an account with SchoolBook |
| **Rational**     | The system will be used to aid students in studying. Thus it is important for students to have an account so that the system will be able to display information of most use to them.|
| **Requirements** | The System should provide a registration form and a submit button for users to enter account details and submit their registration request, System should verify that the account details inserted by the user is in accordance with table REG6.1. Once the user clicks the register button, system will display success message to the user, system will display failure message if data inserted by user is not in accordance with table REG6.1   |
| **References**   | REG6.1: User account data input requirements      |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.1.1: Registration |
| **Summary**     |  The system should provide a Registration feature to allow users to create an account with SchoolBook |   
| **Rational** |The system will be used to aid students in studying. Thus it is important for students to have an account so that the system will be able to display information of most use to them.|    
| **Users** | Anyone  |
| **Pre-Conditions** | Email Provided is not already Registered with SchoolBook |
| **Basic Course Of Events** |<ol><li>User Visits SchoolBook URL www.SchoolBook.com.</li><li>System displays introductory page which contains the Registration Button.</li><li>User Clicks on the Registration button.</li><li>System will respond by displaying the registration form.</li><li> User fills up registration form with fields: Email-Address, Password, Confirm Email-Address, Confirm Password, Date of Birth, Full      Name, Gender and University.</li><li>User Clicks on register button after form is filled.</li><li>System will check input data for error.</li><li> System will display success / failure message, a confirmation email will be sent to user upon success.</li></ol> |
| **References** | REG6.1: User account data input requirements |

## 4.1.2 Login

a. Description and Priority

Allows Registered users to gain access to the system. This Requirement should be of high priority as this is the first step a user needs to satisfy before being able to gain access to the services provided by SchoolBook.

b. Stimulus/Response Sequences
1. User Visits SchoolBook URL www.SchoolBook.com.
2. System Displays introductory page which contains the Login form.
3. User keys in Email Address & Password and clicks Login Button.
4. System compares input values with UserAccounts database table and checks if input data exists in the database.
5. System will redirect user to the Login Homepage on successful verification.
6. System will display error message on verification failure.

c. Functional Requirements

| **Title**        |  **Description** |
|  ----            |     -----               |
| **Item**         |  FR-4.1.2: Login |
| **Summary**      | The system should provide a Login feature to allow users to access their account and consume services provided by SchoolBook |
| **Rational**     | The system will need retrieve unique user-specific information from the database so that relevant information can be displayed to the logged-in user.|
| **Requirements** | The System should provide a Login form and a Login button for users to enter account details and submit their Login request, System should verify that the account details inserted by the user Exists in the SchoolBook Database, upon successful verification, user will be redirected to the user Homepage, upon verification failure, system will display error message   |
| **References**   |  -Nil-    |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.1.2: Login |
| **Summary**     |  The system should provide a Login feature to allow users to access their account and consume services provided by SchoolBook |   
| **Rational** |The system will need retrieve unique user-specific information from the database so that relevant information can be displayed to the logged-in user.|    
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User must have a registered account with School Book |
| **Basic Course Of Events** |<ol><li>User Visits SchoolBook URL www.SchoolBook.com.</li><li>System Displays introductory page which contains the Login form.</li><li>User keys in Email Address & Password and clicks Login Button.</li><li>System compares input values with UserAccounts database table and checks if input data exists in the database.</li><li> System will redirect user to the Login Homepage on successful verification.</li><li>System will display error message on verification failure.</li></ol> |
| **References** | UC-4.1.1: Registration |


## 4.1.3 Password Reset

a. Description and Priority

Allows Registered users to gain access to reset their password in an event that they forgot their password. This Requirement should be of middle priority as this event may not necessary occur.

b. Stimulus/Response Sequences
1. User Visits SchoolBook URL www.SchoolBook.com.
2. System Displays introductory page which contains the Forgot Password Link.
3. User keys in Email Address and clicks Retrieve Button.
4. System checks if email address exists in SchoolBook database & if it exists, sends an email containing a link to user email            account, if email does not exist, system displays error message.
5. User accesses email and click on link sent.
6. System displays Password Reset Page
7. user keys in new password in accordance to table REG6.1 password field and clicks submit.
8. System will display success message, update account password and send confirmation email to user email. User will be redirected to        introductory page with Login Form.
9. if password entered is not in accordance with table REG6.1, system will display error message.

c. Functional Requirements

| **Title**        |  **Description** |
|  ----            |     -----               |
| **Item**         |  FR-4.1.3: Password Reset |
| **Summary**      | The system should provide a Password Reset feature to allow users to Reset their password in any event that they forgot their password. |
| **Rational**     | The System should allow users to reset their password if users forget it so that user can still keep their accounts with their previous data.|
| **Requirements** | The System should provide a Password Reset form and a Submit button for users to enter new Password and submit their Password Reset request, System should verify that the New Password inserted by the user is in accordance to table REG6.1's password format, if in accordance, system will update account password, display success message, send email to user and user will be redirected back to introductory page with Login form, if password is not in accordance, system will display error message.   |
| **References**   |  REG6.1: User account data input requirements   |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.1.3: Password Reset |
| **Summary**     |  The system should provide a Password Reset feature to allow users to Reset their password in any event that they forgot their password. |   
| **Rational** |The System should allow users to reset their password if users forget it so that user can still keep their accounts with their previous data.|    
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User must have a registered account with School Book |
| **Basic Course Of Events** |<ol><li>User Visits SchoolBook URL www.SchoolBook.com.</li><li>System Displays introductory page which contains the Forgot Password Link.</li><li>User keys in Email Address and clicks Retrieve Button.</li><li> System checks if email address exists in SchoolBook database & if it exists, sends an email containing a link to user email            account, if email does not exist, system displays error message.</li><li>User accesses email and click on link sent.</li><li>System displays Password Reset Page</li><li>user keys in new password in accordance to table REG6.1 password field and clicks submit.</li><li>System will display success message, update account password and send confirmation email to user email. User will be redirected to        introductory page with Login Form.</li><li>if password entered is not in accordance with table REG6.1, system will display error message.
</li></ol> |
| **References** | UC-4.1.1: Registration |

## Update Profile
a. Description and Priority 

Allows existing users to edit, update or add their user information within their Schoolbook account. This requirement should be considered a middle priority as this event may not occur. 

b. Stimulus/Response Sequences
1. User Visits SchoolBook URL www.SchoolBook.com
2. System displays login page. 
3. User keys in their username/password and clicks Login Button
4. System will direct user to the Homepage after successfully logging in. 
5. User select their profile account.
6. User selects edit profile. 

c. Functional Requirements

|**Title**        |  **Description** |
| ----            |     -----               |
| **Item**        |   FR-4.2.1: Update Profile |
| **Summary**     |   The system should allow the user to update, edit or add information to their already existing account. 
|
| **Rational**    |   The system should allow the user to change anything on their profile in the event of preexisting information that is now invalid (ex. transfer of schools, new email address).   |
| **Requirements**|   The user must have a preexisting account. The user must be successfully logged into the system The user must present all profile information completed after deleting or changing profile information before saving changes. |
| **References**  |   REG6.1: User account data input requirements. |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.2.1: Update Profile |
| **Summary**     |  The system should allow the user to update, edit or add information to their already existing account.  |   
| **Rational** |The system should allow the user to change anything on their profile in the event of preexisting information that is now invalid(ex. transfer of schools, new email address).|    
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User Must Be Logged in |
| **Basic Course of Events** |<ol><li>User Visits SchoolBook URL www.SchoolBook.com</li><li>System displays login page. </li><li>User keys in their username/password and clicks Login Button</li><li>System will direct user to the Homepage after successfully logging in. </li><li>User select their profile account.</li><li>User selects edit profile.</li></ol> |
| **References** | UC-4.1.1: Registration, REG6.1: User account data input requirements, FR-4.2.1: Update Profile, UC-4.1.2: Login  |

## 4.2.2 Add Course
a. Description and Priority 

Allow users to add courses to their profiles, which gains them access to that specific course’s notes, classmates and tutors. This requirement should be of high priority as users would need to add courses in order to gain access to the courses’ tools and information. 

b. Stimulus / Response Sequences
1. User visits Schoolbook URL www.schoolbook.com.
2. System displays introductory page which contains the login form. 
3. User keys in username/password and clicks Login button. 
4. System displays home page.
5. User clicks add course on the home page.
6. System checks user’s profile based on the college the student is enrolled in.
7. System will upload courses offered at college after successful validation.
8. System will display course department, number and section. 

c. Functional Requirements 

|**Title**        |  **Description** |
| ----            |     -----               |
| **Item**        |   FR-4.2.2 Add Course |
| **Summary**     |   The system allows the user to add single or multiple courses to their profile. 
|
| **Rational**    |  The system should allow the user to select any course offered at the attached university established in their profile  |
| **Requirements**|   In order for the user to add courses, the user must first establish which school they attend in the registration page and/or update profile to their current school. After selecting a school, the user will then have access to add single or multiple courses that are offered by the school.  |
| **References**  |   REG6.1: User account data input requirements. |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.2.2 Add Course |
| **Summary**     |  The system allows the user to add a single or multiple courses to their profile.   |   
| **Rational** |The system should allow the user to select any course offered at the attached university established in their profile | 
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User Must Be Logged in |
| **Basic Course of Events** |<ol><li>User visits Schoolbook URL www.schoolbook.com.</li><li>System displays introductory page which contains the login form.</li><li>User keys in username/password and clicks Login button.</li><li>System displays home page. </li><li>User clicks add course on the home page.</li><li> System checks user’s profile based on the college the student is enrolled in.</li><li>System will upload courses offered at college after successful validation.</li><li>System will display course department, number and section. </li></ol> |
| **References** | UC-4.1.2: Login  |

## 4.2.3 Register as Tutor
a. Description and Priority

The register as tutor feature will allow users to setup their profile as a tutor to specific courses. The profile will go through a manual verification process by allowing the user to upload their past grades in the related course. This requirement should be of high priority as the best tutors will be vital to each courses' study group. 

b. Stimulus / Response Sequences
1. User visits Schoolbook URL www.schoolbook.com.
2. System displays introductory page which contains the login form. 
3. User keys in username/password and clicks Login button. 
4. System displays home page. 
5. User selects a course. 
6. User selects and clicks on 'Register as tutor'. 
7. System will prompt user to upload a file of the users grades to the related course. 
8. System will display success message after file has been upload. 
9. User's file will be screened by a site DBM or Schoolbook admin. 
10. User will be approved or denied as a tutor. 

c. Functional Requirements

|**Title**        |  **Description** |
| ----            |     -----               |
| **Item**        |   FR-4.2.3 Register as tutor |
| **Summary**     |   The system allows the user to register their profile as a tutor for a study group and course.  
|
| **Rational**    |  The system should allow the user to select any course offered at the attached university established in their profile. The user then should be able to select register as tutor and upload their verification files.  |
| **Requirements**|   In order for the user to add courses, the user must first establish which school they attend in the registration page and/or update profile to their current school. After selecting a school, the user will then have access to add single or multiple courses that are offered by the school. Once the user has established a course, they are able to select register as a tutor for that course. The system presents the user with a screen to upload their past grades in a predetermined format. The system will display a success or failure message after the user uploads the file. The user must be prompted on if they have been approved or denied as a tutor. |
| **References**  |  UC-4.1.2: Login  |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.2.3 Register as tutor |
| **Summary**     |   The system allows the user to register their profile as a tutor for a study group and course.     |   
| **Rational** |The system should allow the user to select any course offered at the attached university established in their profile. The user then should be able to select register as tutor and upload their verification files.  | 
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User Must Be Logged in, User must provide justification for the course he / she is registering to be a tutor as |
| **Basic Course Of Events** |<ol><li>User visits Schoolbook URL www.schoolbook.com.</li><li>System displays introductory page which contains the login form. </li><li>User keys in username/password and clicks Login button. </li><li>System displays home page.  </li><li>User selects a course. </li><li>User selects and clicks on 'Register as tutor'. </li><li>System will prompt user to upload a file of the users grades to the related course. </li><li>System will display success message after file has been upload. </li><li>User's file will be screened by a site DBM or Schoolbook admin.</li><li>User will be approved or denied as a tutor. </li></ol> |
| **References** |  FR-4.2.3 Register as tutor , UC-4.1.2: Login  |

## 4.3.1 Create Study Group
a. Description and Priority

The create study group feature will allow users to setup a study group by specifying a location, time, course, and if a tutor will be requested.  Once all study group information is entered correctly the users will be presented with a confirmation / failure message and returned to their home screen.

b. Stimulus / Response Sequences
1. A verified user is successfully logged into the system.
2. From either the home page menu or a specific course page's menu the user selects the setup study group function.
3. The system presents the user with the setup study group page.
4. User specifies what course, location, time, and if they request a tutor or not.
5. System will check input data for errors.
6. System will display success / failure message, and returns them to the home screen.

c. Functional Requirements

| **Title**        |  **Description** |
|  ----            |     -----               |
| **Item**         |  FR-4.3.1: Setup Study Group |
| **Summary**      | The system will provide a setup study group feature that will allow students to setup study groups with their classmates. |
| **Rational**     | The system is a way for students to be better connected with their classmates, setting up and attending study groups is an important part of a student’s education. Therefore, it is an important component to this system.  |
| **Requirements** | The user must be successfully logged into the system, and selected setup study group form either the home page menu or the course page's menu.  The system presents the user with a study group setup screen, the user specifies the course, location, time, and whether or not they want a tutor to attend. The system will display a success or failure message after checking the input data.  |
| **References**   | UC-4.1.2: Login    |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.3.1: Setup Study Group |
| **Summary**     |   The system will provide a setup study group feature that will allow students to setup study groups with their classmates.    |   
| **Rational** |The system is a way for students to be better connected with their classmates, setting up and attending study groups is an important part of a student’s education. Therefore, it is an important component to this system.  | 
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User Must Be Logged in |
| **Basic Course Of Events** |<ol><li> A verified user is successfully logged into the system.</li><li>From either the home page menu or a specific course page's menu the user selects the setup study group function.</li><li>The system presents the user with the setup study group page.</li><li>User specifies what course, location, time, and if they request a tutor or not.</li><li>System will check input data for errors.</li><li>System will display success / failure message, and returns them to the home screen.</li></ol> |
| **References** |  UC-4.1.2: Login  |

## 4.3.2 Find Study Group
a. Description and Priority

The search for study group feature will allow uses to search for study groups based on the course department and ID.  The system will present the user with a list of the upcoming scheduled study groups for that course.

b. Stimulus / Response Sequences
1. A verified user is successfully logged into the system.
2. From either the home page menu or a specific course page menu the user selects the find study group function.
3. The system presents the user with a find study group screen.
4. The user specifies the course's department and course ID.
5. The system displays a list of upcoming scheduled study groups for the specified course and its details.
6. The user selects a study group from the list.
7. System displays a screen showing the details of the study group and a join study group option. 

c. Functional Requirements

| **Title**        |  **Description** |
|  ----            |     -----               |
| **Item**         |  FR-4.3.2: Find Study Group |
| **Summary**      | The system will provide a find study group feature that will allow students to find study groups for the courses they are enrolled in. |
| **Rational**     | The system provides a setup study group function, so the system must include a find study group function for users to find study groups that have already been setup.  |
| **Requirements** | The user must be successfully logged into the system, and selected find study group form either the home page menu or the course page's menu. The user provides a course department and course ID. The system presents the user with a list of upcoming scheduled study groups for the specified course. |
| **References**   |  FR4.3.1: Create Study Group    |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.3.2: Find Study Group|
| **Summary**     |   The system will provide a find study group feature that will allow students to find study groups for the courses they are enrolled in.    |   
| **Rational** |The system provides a setup study group function, so the system must include a find study group function for users to find study groups that have already been setup.   | 
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User Must Be Logged in |
| **Basic Course Of Events** |<ol><li>A verified user is successfully logged into the system.</li><li>From either the home page menu or a specific course page menu the user selects the find study group function.</li><li>The system presents the user with a find study group screen.</li><li>The user specifies the course's department and course ID.</li><li>The system displays a list of upcoming scheduled study groups for the specified course and its details.</li><li>The user selects a study group from the list.</li><li>System displays a screen showing the details of the study group and a join study group option. 
</li></ol> |
| **References** |  UC-4.1.2: Login  |

## 4.3.3 Join Study Group
a. Description and priority

The join study group feature will allow users to join study groups from the find study group search results screen.

b. Stimulus / Response Sequences
1. A verified user has selected a specific study group from the find study group function results.
2. System displays a screen showing the details of the study group and a join study group option.
3. User selects the join study group option.
4. System displays a success / failure message and returns the user to the study group's details page.

c. Functional Requirements

| **Title**        |  **Description** |
|  ----            |     -----               |
| **Item**         |  FR-4.3.3: Join Study Group |
| **Summary**      | The system will provide a join study group feature that will allow students to join study groups for the courses they are enrolled in. |
| **Rational**     | The system provides a setup study group function, so the system should include a join study group function for users to join study groups that have already been setup.  |
| **Requirements** | The user must be successfully logged into the system, and selected join study group form the study group's details page, the system displays a success / failure message and returns the user to the study group's details page. |
| **References**   |  FR4.3.2: Find Study Group    |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.3.3: Join Study Group |
| **Summary**     |   The system will provide a join study group feature that will allow students to join study groups for the courses they are enrolled in.  |   
| **Rational** |The system provides a setup study group function, so the system should include a join study group function for users to join study groups that have already been setup.   | 
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User Must Be Logged in |
| **Basic Course Of Events** |<ol><li>A verified user has selected a specific study group from the find study group function results.</li><li>System displays a screen showing the details of the study group and a join study group option.</li><li>User selects the join study group option.</li><li>System displays a success / failure message and returns the user to the study group's details page.</li></ol> |
| **References** |  UC-4.1.2: Login  |

## 4.3.4 Leave Study Group
a. Description and priority

The leave study group feature will allow users to leave study groups that they have previously joined.

b. Stimulus / Response Sequences
1. A verified user has successfully logged into the system and joined a study group.
2. The user selects the leave study group feature from the home page menu.
3. The system displays a list of the study groups that the user has previously joined.
4. The user selects the study group that they intend to leave from the list.
5. The system displays a confirmation message asking if the user intends to leave the selected course displaying the study group’s details.
6. If the user confirms the action the system removes the user from the study group, displays a success / failure message and returns the user to the home page. If the user denies the action the system returns the user back to the list of study groups they can leave without removing the user from the study group.

c. Functional Requirements

| **Title**        |  **Description** |
|  ----            |     -----               |
| **Item**         |  FR-4.3.4: Leave Study Group |
| **Summary**      | The system will provide a leave study group feature that will allow students to leave study groups they have previously joined. |
| **Rational**     | The system provides a setup study group function, and a join study group function, so the system should also provide a leave study group function.  |
| **Requirements** | The user must be successfully logged into the system, have previously used the find and join study group functions to join a study group. The user selects the leave study group function from the home page menu.  The system displays list of the study groups that the user has previously joined. The user selects the study group they wish to leave from the list. The system presents a confirmation message to the user.  If the user confirms the action the user is removed from the study group, the system presents a success / failure message and returns the user to the home page. If the user denies the action the user is not removed from the study group and is returned to the leave study group page containing the list of study groups they have previously joined. |
| **References**   |  FR4.3.3: Join Study Group    |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.3.4: Leave Study Group|
| **Summary**     |   The system will provide a leave study group feature that will allow students to leave study groups they have previously joined.  |   
| **Rational** |The system provides a setup study group function, and a join study group function, so the system should also provide a leave study group function.    | 
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User Must Be Logged in, User Must be part of an existing Study Group |
| **Basic Course Of Events** |<ol><li>A verified user has successfully logged into the system and joined a study group.</li><li>The user selects the leave study group feature from the home page menu.</li><li>The system displays a list of the study groups that the user has previously joined.</li><li>The user selects the study group that they intend to leave from the list.</li><li>The system displays a confirmation message asking if the user intends to leave the selected course displaying the study group’s details.</li><li>If the user confirms the action the system removes the user from the study group, displays a success / failure message and returns the user to the home page. If the user denies the action the system returns the user back to the list of study groups they can leave without removing the user from the study group.</li></ol> |
| **References** |  UC-4.1.2: Login  |

## 4.4.1 Uploading Notes

a. Description and Priority

Allows users to upload documents, class notes, and study tools for a specific course. Users will be able to access these notes by accessing the course page for which the notes were uploaded for. 

b. Stimulus/Response Sequences
1. User Visits SchoolBook URL www.SchoolBook.com.
2. User logs in and accesses student profile.
3. User is brought to their own personal page if previously registered. 
4. Select the course and semester/year in which the notes are being used for.
5. By clicking the upload button, notes are added to the selected course page. 

c. Functional Requirements

| **Title**        |  **Description** |
|  ----            |     -----               |
| **Item**         |  FR-4.4.1: Uploading Notes |
| **Summary**      | The system provides the user with the ability to add notes for specific courses for a specific semester |
| **Rational**     | The main purpose for 'SchoolBook' is to allow students to access notes and study aids from other students in need of help. In order for students to access notes, an upload feature is needed.|
| **Requirements** | In order for the user to upload notes, the user must first register as a student at a specific university. After registering for SchoolBook, the user will then be able to upload the notes of their choice for the specific course.   |
| **References**   | -Nil-   |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.4.1: Uploading Notes  |
| **Summary**     |  The system provides the user with the ability to add notes for specific courses for a specific semester |   
| **Rational** |The main purpose for 'SchoolBook' is to allow students to access notes and study aids from other students in need of help. In order for students to access notes, an upload feature is needed.|    
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User Must Be logged in |
| **Basic Course of Events** |<ol><li>User Visits SchoolBook URL www.SchoolBook.com.</li><li>User logs in and accesses student profile.</li><li>User is brought to their own personal page if previously registered. </li><li>Select the course and semester/year in which the notes are being used for.</li><li> By clicking the upload button, notes are added to the selected course page. </li></ol> |
| **References** | UC-4.1.2: Login |

## 4.4.2 Searching for Notes

a. Description and Priority

The search feature will allow students to search and filter throughout the database for specific courses. The search results will allow the user to select that course in which then a list of previously uploaded notes will appear for that specific course. 

b. Stimulus/Response Sequences
1. User Visits SchoolBook URL www.SchoolBook.com.
2. User logs in and accesses student profile.
3. User is brought to their own personal page if previously registered. 
4. The top bar of the main page will provide users with a search bar.
5. By typing into the search bar, results will reveal a list of courses throughout the database.
6. By selecting a course in the list, the user will be provided with a list of previously uploaded notes for that specific course.

c. Functional Requirements

| **Title**        |  **Description** |
|  ----            |     -----               |
| **Item**         |  FR-4.4.2: Searching for Notes |
| **Summary**      | The system will provide users with the ability to search for courses throughout the database and select from a list of list of previously uploaded documents |
| **Rational**     | The search bar is used to search for courses offered at the University, therefore the user must search for a valid course in order to access notes. |
| **Requirements** | The user must search for a course offered at the University of their choice in order to access notes.  |
| **References**   |  -Nil-    |

d. Use Case

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        |  UC-4.4.2: Searching for Notes  |
| **Summary**     |  The system will provide users with the ability to search for courses throughout the database and select from a list of list of previously uploaded documents |   
| **Rational** |The search bar is used to search for courses offered at the University, therefore the user must search for a valid course in order to access notes.|    
| **Users** | Students & Student Tutors |
| **Pre-Conditions** | User Must Be logged in |
| **Basic Course of Events** |<ol><li>User Visits SchoolBook URL www.SchoolBook.com.</li><li>User logs in and accesses student profile.</li><li>User is brought to their own personal page if previously registered. </li><li>The top bar of the main page will provide users with a search bar.</li><li>  By typing into the search bar, results will reveal a list of courses throughout the database.</li><li>By selecting a course in the list, the user will be provided with a list of previously uploaded notes for that specific course.</li></ol> |
| **References** | UC-4.1.2: Login |

# 5.Other Nonfunctional Requirements

## 5.1Performance Requirements
| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        | NF- 5.1.1: Performance requirements for searching |
| **Summary**     | The search function must have a worst case runtime of O(n log n).
| **Rational**    | Finding notes and groups should be quick and easy. Students in a rush don't have time to waste |
| **Reference**   | FR-4.3.2 FR-4.4.2 | 

| **Item**        | NF- 5.1.2: Performance requirements for uploading and downloading |
| **Summary**     | Uploading and downloading should time-out if duration of individual object exceeds 60 seconds.
| **Rational**    | Excessively long times are a nuisance and may indicate connectivity issues. Best to time out and have the user try again later |
| **Reference**   | FR-4.4.2 FR-4.4.1 |


## 5.2 Safety Requirements
| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        | NF- 5.2.1: Safety requirements for tutors |
| **Summary**     | Tutor's must undergo an application process and background check in accordance with EEOC and FTC guidelines. Only after approval shall a tutor be available to students. |
| **Rational**    | This protects the students from people with harmful intentions or who are under qualified |
| **Reference**   | FR-4.2.3 | 

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        | NF- 5.2.2: Safety requirements for registration |
| **Summary**     | All individuals that register must do so with a .edu email. |
| **Rational**    | This protects the students from people with harmful intentions or who don't belong. |
| **Reference**   | FR-4.1.1 |


## 5.3Security Requirements

| **Title**       | **Description**  |
| -------------   |-------------     |
| **Item**        | NF- 5.3.1: Security requirements for sensitive information |
| **Summary**     | All data containing user information must follow the Advanced Encryption Standard(AES). |
| **Rational**    | This protects the students from hackers and identity theft. |
| **Reference**   | FR-4.1.1, FR-4.1.2, FR-4.1.3, FR-4.2.1 |

## 5.4Software Quality Attributes
Site should be portable and usable with mobile and desktop screens. The tutor vetting process must be reliable with preference for increased security over increased ease of acceptance. 


## 5.5Business Rules

Guest users may register to be a student but may not access any material. Students may manage profile information, manage current courses, create and leave study groups, view and manage notes, and register to be a tutor. Tutor users have all student privileges plus ability to join groups of courses they aren't taken if they're an accepted tutor for the course. 

# 6.Other Requirements

## REG6.1 - User account data input requirements
| Field Name            | Requirements                                                                                      | 
| ---                   | ---                                                                                               |
| E-Mail Address        | Characters in the format of xxxxxx@xxxxx.xx (x == characters)                                     |
| Password              | minimum of 12 alphanumeric characters, compulsory use of a number and an alphabet                  |
| Confirm Email-Address | Must be exactly the same as what was entered in E-Mail Address field                               |
| Confirm Password      | Must be exactly the same as what was entered in password field                                    |
| Date of Birth         | entered in the format of MM/DD/YYYY, the value entered must be of a valid Gregorian calendar date |
| Full Name             | Maximum of 40 characters                                                                          |
| Gender                | Radio Button, with display value of Male & Female, only able to select one                        |
| University            | Drop-down list of all the available universities, user only able to select one                    |

# Appendix A: Analysis Models

## Use-Case Diagram
![alt tag](https://raw.githubusercontent.com/ndugal6/SchoolBook/master/SRSimgs/SchoolBookUseCaseDiagram.gif)

## Entity-Relation Diagram
![alt tag](https://raw.githubusercontent.com/ndugal6/SchoolBook/master/SRSimgs/ERDiagramSchoolBook.gif)

## Tutor Application Dataflow Diagram
![alt tag](https://raw.githubusercontent.com/ndugal6/SchoolBook/master/SRSimgs/SB_TUTORAPP_DF.gif)

## Database ER Diagram
![alt tag](https://raw.githubusercontent.com/ndugal6/SchoolBook/master/Database/SchoolBookERv1.2.gif)

# Appendix B: To Be Determined List

| no. | Function | Last Review Date  | Able to Achieve? |
| --- |   ---    |     --------      |    -------       |
|1.   | Multi-Threaded real-time chat | 10/20/2016 | No   |
|2.   | IOS/Android Application      | 10/20/2016 | No   |

