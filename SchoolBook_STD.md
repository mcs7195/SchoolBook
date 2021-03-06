# Software Testing Document for SchoolBook

**Prepared by:** 

Clayton R Samson, Justin A Bougere, Nicholas A Dugal, Sean M Marino, Soh Guo Hao Steffano, Zachary J Robicheaux

**Date Prepared: 11/14/2016**


| Table of Contents         |
| --- |
| **1. Login/Registration** |
|      TC 1.1        Registration       |
|      TC 1.2        Login        |
|      TC 1.3        Password Reset        |
| **2. Profile Management** |
|      TC 2.1        Update Profile        |
|      TC 2.2        Add Course        |
|      TC 2.3        Register as Tutor        |
| **3. Study Group Management** |
|      TC 3.1        Create Study Group         |
|      TC 3.2        Search for study Group        |
|      TC 3.3        Join Study Group        |
|      TC 3.4        Leave Study Group        |
| **4. Notes Management** |
|      TC 4.1        Upload Notes        |
|      TC 4.2        Search for Notes        |

## Registration
### Registration with satisfied Validation
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.1.1 | **Test Case Name:** Registration with satisfied Validation  |
| **System:** SchoolBook         | **Sub-System:** Login/Registration      |
| **Designed By:** Steffano Soh    |  **Design Date:** 11/18/2016    |
| **Executed By:** *TBD*    |  **Execution Date:** *TBD* |

**Short Description:** <br/>
Test the registration system with satisfactory input
<br/>**Pre-Conditions:**
User Must not be already registered <br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.        | Click on the *Register* Button within the Login form section | System changes login form into Registration Form|||
|2.        | Key in __Test2@gmail.com__ in the *Email Address* Text field| -Nil- |||
|3.        | Key in __password1__ in the *Password* Text field| -Nil- |||
|4.        | Key in __Test2@gmail.com__ in the *Confirm Email Address* Text field| -Nil- |||
|5.        | Key in __password1__ in the *Confirm Password* Text field| -Nil- |||
|6.        | Key in __01/01/1990__ in the *Date of Birth* Text field| -Nil- |||
|7.        | Key in __Tom Riddle__ in the *Full Name* Text field| -Nil- |||
|8.        | Select __male__ radio button | -Nil- |||
|9.        | Select __Louisiana State University__ from the drop down list | -Nil- |||
|10.       | Click on the *Register* Button | System Displays Registration sucessful message. |||

**Post Condition:**<br/>
User is sucessfully registered <br/>
User account information now inserted into SchoolBook Database

### Registration with unsatisfactory Validation

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.1.2 | **Test Case Name:** Registration with unsatisfactory Validation  |
| **System:** SchoolBook         | **Sub-System:** Login/Registration      |
| **Designed By:** Steffano Soh    |  **Design Date:** 11/18/2016    |
| **Executed By:** *TBD*    |  **Execution Date:** *TBD* |

**Short Description:** <br/>
Test the registration system with unsatisfactory input
<br/>**Pre-Conditions:**
User Must not be already registered <br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.        | Click on the *Register* Button within the Login form section | System changes login form into Registration Form|||
|2.        | Key in __Test2__ in the *Email Address* Text field| -Nil- |||
|3.        | Key in __password__ in the *Password* Text field| -Nil- |||
|4.        | Key in __Test3__ in the *Confirm Email Address* Text field| -Nil- |||
|5.        | Key in __password1__ in the *Confirm Password* Text field| -Nil- |||
|6.        | Key in __01/01/1990__ in the *Date of Birth* Text field| -Nil- |||
|7.        | Key in __Tom Riddle__ in the *Full Name* Text field| -Nil- |||
|8.        | do not select any radio button | -Nil- |||
|9.        | do not select any drop down list value | -Nil- |||
|10.       | Click on the *Register* Button | System Displays error message shown in the block below |||

> Please enter a valid email address <br/>
> Please enter a valid password that consist of a mixture of alphaberts and numbers <br/>
> confirm email did not match <br/>
> confirm password did not match <br/>
> Please select your gender <br/>
> Please select a university 

**Post Condition:**<br/>
User account not registered <br/>
User remains in Introductory page

### Registration with Email Address already registered 
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.1.3 | **Test Case Name:** Registration with Email Address already registered   |
| **System:** SchoolBook         | **Sub-System:** Login/Registration      |
| **Designed By:** Steffano Soh    |  **Design Date:** 11/18/2016    |
| **Executed By:** *TBD*    |  **Execution Date:** *TBD* |

**Short Description:** <br/>
Test the registration system with satisfactory Email Address already registered
<br/>**Pre-Conditions:**
-Nil- <br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.        | Click on the *Register* Button within the Login form section | System changes login form into Registration Form|||
|2.        | Key in __Test@gmail.com__ in the *Email Address* Text field| -Nil- |||
|3.        | Key in __password1__ in the *Password* Text field| -Nil- |||
|4.        | Key in __Test@gmail.com__ in the *Confirm Email Address* Text field| -Nil- |||
|5.        | Key in __password1__ in the *Confirm Password* Text field| -Nil- |||
|6.        | Key in __01/01/1990__ in the *Date of Birth* Text field| -Nil- |||
|7.        | Key in __Tom Riddle__ in the *Full Name* Text field| -Nil- |||
|8.        | Select __male__ radio button | -Nil- |||
|9.        | Select __Louisiana State University__ from the drop down list | -Nil- |||
|10.       | Click on the *Register* Button | System Displays "Email Address already Registered" Message |||

**Post Condition:**<br/>
User is sucessfully registered <br/>
User account information now inserted into SchoolBook Database

## Login

### Login with Registered Email & Password

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.2.1 | **Test Case Name:** Login With Registered Email & Password  |
| **System:** SchoolBook         | **Sub-System:** Login/Registration      |
| **Designed By:** Steffano Soh    |  **Design Date:** 11/18/2016     |
| **Executed By:** *TBD*    |  **Execution Date:** *TBD* |

**Short Description:** <br/>
Test The Login Sub System with a Registered Email & Password<br/>
<br/>**Pre-Conditions:**
User Must have a Registered Account with SchoolBook<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.        | Key in __Test@gmail.com__ in the *Email Address* Text box within the Login Form | -Nil-|||
|2.        | Key in __password__ in the *Password* Text box within the Login Form | -Nil-|||
|3.        | Click on the *Login* Button within the Login Form | System Redirects user to his Profile Homepage | |

**Post Condition:**<br/>
1. User is logged into the SchoolBook System<br/>
2. User sees his information in the redirected page.

### Login with invalid Email & Password

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.2.2 | **Test Case Name:** Login With invalid Email & Password  |
| **System:** SchoolBook         | **Sub-System:** Login/Registration      |
| **Designed By:** Steffano Soh    |  **Design Date:** 11/18/2016     |
| **Executed By:** *TBD*    |  **Execution Date:** *TBD* |

**Short Description:** <br/>
Test The Login Sub System with a invalid Email & Password <br/>
<br/>**Pre-Conditions:**
-Nil-<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.        | Key in __invalid@gmail.com__ in the *Email Address* Text box within the Login Form | -Nil-|||
|2.        | Key in __invalidpassword__ in the *Password* Text box within the Login Form | -Nil-|||
|3.        | Click on the *Login* Button within the Login Form | System displays "incorrect Userid/Password" Message | |

**Post Condition:**<br/>
1. User denied access to SchoolBook<br/>
2. User stays in introductory page.


### Login with valid Email & invalid Password

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.2.3 | **Test Case Name:** Login with valid Email & invalid Password  |
| **System:** SchoolBook         | **Sub-System:** Login/Registration      |
| **Designed By:** Steffano Soh    |  **Design Date:** 11/18/2016     |
| **Executed By:** *TBD*    |  **Execution Date:** *TBD* |

**Short Description:** <br/>
Test The Login Sub System with valid Email & invalid Password<br/>
<br/>**Pre-Conditions:**
-Nil-<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.        | Key in __Test@gmail.com__ in the *Email Address* Text box within the Login Form | -Nil-|||
|2.        | Key in __invalidpassword__ in the *Password* Text box within the Login Form | -Nil-|||
|3.        | Click on the *Login* Button within the Login Form | System displays "incorrect Userid/Password" Message | |

**Post Condition:**<br/>
1. User denied access to SchoolBook<br/>
2. User stays in introductory page.


### Login with invalid Email & valid Password

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.2.4 | **Test Case Name:** Login with invalid Email & valid Password  |
| **System:** SchoolBook         | **Sub-System:** Login/Registration      |
| **Designed By:** Steffano Soh    |  **Design Date:** 11/18/2016     |
| **Executed By:** *TBD*    |  **Execution Date:** *TBD* |

**Short Description:** <br/>
Test The Login Sub System with invalid Email & valid Password <br/>
<br/>**Pre-Conditions:**
-Nil-<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.        | Key in __invalid@gmail.com__ in the *Email Address* Text box within the Login Form | -Nil-|||
|2.        | Key in __password__  in the *Password* Text box within the Login Form | -Nil-|||
|3.        | Click on the *Login* Button within the Login Form | System displays "incorrect Userid/Password" Message | |

**Post Condition:**<br/>
1. User denied access to SchoolBook<br/>
2. User stays in introductory page.

## Password Reset

### Password Reset with valid email
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.3.1  | **Test Case Name:** Password Reset with valid email  |
| **System:** SchoolBook         | **Sub-System:** Login/Registration      |
| **Designed By:** Steffano Soh    |  **Design Date:** 21/11/2016    |
| **Executed By:** TBD    |  **Execution Date:** TBD |

**Short Description:** <br/>
Test the password Reset Function
<br/>**Pre-Conditions:**
user must have a once registered with schoolbook before<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.| User Clicks on *Forget Password* link within the login form | System redirects user to password reset page|||
|2.| Key in __Test@gmail.com__ in the *Email Address* Text box | System Sends Reset URL to specified Email Address|||
|3.| User Visits link sent via email | -Nil- | | |
|4.| User Keys in new password | | |
|5.| User Clicks on *Submit* Button| System displays sucess message, Password Updated in SchoolBook Database | | |

**Post Condition:**<br/>
1. User's Password is updated in the database

### Password Reset with invalid email
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.3.2  | **Test Case Name:** Password Reset with invalid email  |
| **System:** SchoolBook         | **Sub-System:** Login/Registration      |
| **Designed By:** Steffano Soh    |  **Design Date:** 21/11/2016    |
| **Executed By:** TBD    |  **Execution Date:** TBD |

**Short Description:** <br/>
Test the password Reset Function
<br/>**Pre-Conditions:**
-Nil-<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.| User Clicks on *Forget Password* link within the login form | System redirects user to password reset page|||
|2.| Key in __invalid@gmail.com__ in the *Email Address* Text box | System Displays error message "Email not registered"|||

**Post Condition:**<br/>
1. User remains in Forget Password page

## Update Profile

## Update Profile with Vaild Parameters
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.4.1 | **Test Case Name:** Update Profile with Vaild Parameters |
| **System:** SchoolBook        | **Sub-System:** Update Profile     |
| **Designed By:** Zachary Robicheaux    |  **Design Date:** TBD   |
| **Executed By:** Zachary Robicheaux    |  **Execution Date:** TBD |

**Short Description:** <br/>
Tests the Update Profile system with all valid parameters.
<br/>**Pre-Conditions:**
1. User has a valid account.<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.        |Click __Update Profile__ on the Homepage.|User is taken to the Update Profile page|||
|2.        |Key in __Test2@gmail.com__ in the *Email Address* Text field| -Nil- |||
|3.        | Key in __password1__ in the *Password* Text field| -Nil- |||
|4.        | Key in __Test2@gmail.com__ in the *Confirm Email Address* Text field| -Nil- |||
|5.        | Key in __password1__ in the *Confirm Password* Text field| -Nil- |||
|6.        | Key in __01/01/1990__ in the *Date of Birth* Text field| -Nil- |||
|7.        | Key in __(504)-247-6216__ in the *Phone Number* Text field| -Nil- |||
|8.        | Key in __Tom Riddle__ in the *Full Name* Text field| -Nil- |||
|9.        | Select __male__ radio button | -Nil- |||
|10.        | Select __Louisiana State University__ from the drop down list | -Nil- |||
|11.|Click __Choose__ button for the Profile Picture|User is taken to file system on the computer|||
|12.|Select __test.jpg__|__test.jpg__ is uploaded to SchoolBook|||
|13.|Click __Update Profile__|System displays "updated profile" Message|||

**Post Condition:**<br/>
1. User's account information is updated
2. Page is refreshed

## Update Profile with Invaild Parameters
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.4.2 | **Test Case Name:** Update Profile with Invaild Parameters  |
| **System:** SchoolBook        | **Sub-System:** Update Profile     |
| **Designed By:** Zachary Robicheaux    |  **Design Date:** TBD   |
| **Executed By:** Zachary Robicheaux    |  **Execution Date:** TBD |

**Short Description:** <br/>
Test the Update Profile system using an invalid phone number and birth date.
<br/>**Pre-Conditions:**
1. User has a valid account.<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.        |Click __Update Profile__ on the Homepage.|User is taken to the Update Profile page|||
|2.        | Key in __(504)-247-62166__ in the *Phone Number* Text field| -Nil- |Text Field higlights red||
|3.        | Key in __99/01/1990__ in the *Date of Birth* Text field| -Nil- |Text Field highlights red||
|4.|Click __Update Profile__|System displays "invalid parameters" Message|||

**Post Condition:**<br/>
1. User's account information remains the same


## Add Course

## Add Course with Valid Class
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.5.1 | **Test Case Name:**   |
| **System:** SchoolBook        | **Sub-System:**   Add Course with Valid Class  |
| **Designed By:** Zachary Robicheaux    |  **Design Date:** TBD    |
| **Executed By:** Zachary Robicheaux    |  **Execution Date:** TBD |

**Short Description:** <br/>
Test the add course subsystem using valid class selection.
<br/>**Pre-Conditions:**
1. User has a valid account.
<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.|Click "Add Course" on the Homepage.|User is taken to the Add Course page; page displays all classes from the user's university|||
|2.|Select the course labeled "test"|-Nil-|||
|3.|Click the "Add Course" button|System displays "course added" Message|||

**Post Condition:**<br/>
1. "test" is added to the user's list of classes
2. The page is refreshed.

## Add Course that User is Enrolled in
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 1.5.2 | **Test Case Name:**   |
| **System:** SchoolBook        | **Sub-System:**   Add Course that User is Enrolled in  |
| **Designed By:** Zachary Robicheaux    |  **Design Date:** TBD    |
| **Executed By:** Zachary Robicheaux    |  **Execution Date:** TBD |

**Short Description:** <br/>
Test the add course subsystem using a class the user is already enrolled in.
<br/>**Pre-Conditions:**
1. User has a valid account.
2. User is enrolled in class "test" 
<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.|Click "Add Course" on the Homepage.|User is taken to the Add Course page; page displays all classes from the user's university|||
|2.|Select the course labeled "test"|-Nil-|||
|3.|Click the "Add Course" button|System displays "already enrolled in class" Message|||

**Post Condition:**<br/>
1. The class "test" won't be re-added to the user's list of classes.


## Register as Tutor

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 2.3.1 | **Test Case Name:** Register as tutor  |
| **System:** SchoolBook         | **Sub-System:** Profile Management      |
| **Designed By:** Steffano Soh    |  **Design Date:** 21/11/2016    |
| **Executed By:** *TBD*    |  **Execution Date:** *TBD* |

**Short Description:** <br/>
Test the register as tutor system
<br/>**Pre-Conditions:**
User must be registered with SchoolBook
User must be logged in
<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.| Click on the *Profile* link in the submenu| System displays submenu item |||
|2.| Click on the *Register as Tutor* Link | System redirects user to Register as tutor page|||
|3.| Select __Louisiana State University__ from the *university* drop down list| -Nil-|||
|4.| Select __csc4103 - Operating Systems__ from the course codes drop down list| -Nil-|||
|5.| click on *upload pdf* Link and select a pdf file to upload| -Nil- ||
|6.| click on *Register as tutor* Button | System Displays Message "Registration request sucessfully made" | ||

**Post Condition:**<br/>
1. Request to be registered as tutor made and pending for approval<br/>
2. pdf, University and course ID selected stored in database<br/>
3. upon approval user recieves confirmation Email.

## Create Study Group
### Create Valid Study Group
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** *3.1.1* | **Test Case Name:** *Create Valid Study Group*  |
| **System:** *SchoolBook*         | **Sub-System:** *Study Group*      |
| **Designed By:** *Nicholas Dugal*    |  **Design Date:** *11/19/2016*    |
| **Executed By:** *CONTENT HERE*    |  **Execution Date:** *CONTENT HERE* |

**Short Description:** <br/>
*Test the study group creation with valid input*
<br/>**Pre-Conditions:**
*User must be logged in*<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.|User selects setup study group function|System presents user with setup study group page|||
|2.|User selects course|Nil|||
|3.|User provides valid location|Checked with Location Regular Expression|||
|4.|User provides date|Check with Date RegExpression|||
|5.|User provides time|Checked with Time RegExpression|||
|6.|User selects whether or not to request tutor|Nil|||
|7.|User clicks Finalize Study Group|System display success message and returns to home screen|||
**Post Condition:**   User in now member of created study group<br/>

### Create Study Group Using Irregular Input
|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** *3.1.2* | **Test Case Name:** *Create Study Group Using Irregular Input*  |
| **System:** *SchoolBook*         | **Sub-System:** *Study Group*      |
| **Designed By:** *Nicholas Dugal*    |  **Design Date:** *11/19/2016*    |
| **Executed By:** *CONTENT HERE*    |  **Execution Date:** *CONTENT HERE* |

**Short Description:** <br/>
*Test the study group creation form regular expression checkers*
<br/>**Pre-Conditions:**
*User must be logged in*<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.|User selects setup study group function|System presents user with setup study group page|||
|2.|User selects course|Nil|||
|3.|User provides invalid or incorrectly formatted location|Box is highlighted red|||
|4.|User provides past date or incorrectly formatted date|Box is highlighted red|||
|5.|User provides past time or incorrectly formatted time|Box is highlighted red|||
|6.|User selects whether or not to request tutor|Nil|||
|7.|User clicks Finalize Study Group|System display failure message, requesting to fix highlighted boxes|||
**Post Condition:**   User remains at creation screen<br/>


## Search for study Group 
### Valid Study Group Search

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** *3.2.1* | **Test Case Name:** *Valid Study Group Search*  |
| **System:** *SchoolBook*         | **Sub-System:** *Study Group*      |
| **Designed By:** *Nicholas Dugal*    |  **Design Date:** *11/19/2016*    |
| **Executed By:** *CONTENT HERE*    |  **Execution Date:** *CONTENT HERE* |

**Short Description:** <br/>
*Test the search for study group function*
<br/>**Pre-Conditions:**
*User Must Be Logged in*<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.|From either the home page menu or a specific course page menu the user selects the find study group function|The system presents the user with a find study group screen.|||
|2.|User selects course department|Courses for next step are loaded|||
|3.|User selects course|The system displays a list of upcoming scheduled study groups for the specified course and its details|||
|4.|User a study group from the list|System displays a screen showing the details of the study group and a join study group option|||
|5.|User selects option to join study group|System display success message and returns to homescreen|||

**Post Condition:**User is now a member of the study group selected<br/>


## Join Study Group

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 3.3.1 | **Test Case Name:** Join Study Group  |
| **System:** SchoolBook         | **Sub-System:** Join Study Group      |
| **Designed By:** *Sean Marino*    |  **Design Date:** *11/20/2016*    |
| **Executed By:** *CONTENT HERE*    |  **Execution Date:** *CONTENT HERE* |

**Short Description:** <br/>
*Select a listed study group by searching and join the specific study group*
<br/>**Pre-Conditions:**
*User must access the list of study groups*<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.|Scroll through the list of available study groups|-Nil-|||
|2.|User selects the specified study group|System displays a screen showing the details of the study group and a join study group option|||
|3.|User selects the join study group option|System displays a success/failure message and returns the user to the study group's detail page|||

**Post Condition:**User has successfully joined a study group<br/>



## Leave Study Group

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. :** TC 3.4.1 | **Test Case Name:** Leave Study Group  |
| **System:** SchoolBook         | **Sub-System:** Leave Study Group      |
| **Designed By:** *Sean Marino*    |  **Design Date:** *11/20/2016*    |
| **Executed By:** *CONTENT HERE*    |  **Execution Date:** *CONTENT HERE* |

**Short Description:** <br/>
*Allows users successfully leave the study group that they have joined
<br/>**Pre-Conditions:**
*User must be enrolled in a study group*<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.|User accesses the list of currently joined study groups|-Nil-|||
|2.|User selects the study group that they intend to leave from the list|The system displays a confirmation message asking if the user intends to leave the selected course displaying the study group's details|||
|3.|User confirms the confirmation message to leave the study group|System displays a success/failure message and returns the user to the home page or returns the user back to the list of study groups if the user denies the confirmation message|||
**Post Condition:**User successfully leaves the study group<br/>


## Upload Notes With Satisfactory Input

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. : 4.1.1 | **Test Case Name: Upload Notes  |
| **System: SchoolBook         | **Sub-System: Notes Management      |
| **Designed By: Clayton Samson    |  **Design Date: 11/21/2016    |
| **Executed By: TBD    |  **Execution Date: TBD |

**Short Description:** <br/>
Test upload notes function with satisfactory input.
<br/>**Pre-Conditions:** 1. User has a verified account and is successfully logged into the system.<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.| User selects upload notes button from the main menu. | System displays the upload notes page.  |||
|2.| User specifies the course the notes are for from a list of their enrolled courses. | System updates the specified course field with the users specified element. |||
|3.| User elects the choose file button at the bottom of the page. | System displays a file browser for the user to specify their document. |||
|4.| User specifies a PDF file they want to upload. | System uploads file to database and displays a confirmation message.|||

**Post Condition:** 1. The PDF file is uploaded to the database.<br/>


## Upload Notes With Unsatisfactory Input

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. : 4.1.2 | **Test Case Name: Upload Notes  |
| **System: SchoolBook         | **Sub-System: Notes Management      |
| **Designed By: Clayton Samson    |  **Design Date: 11/21/2016    |
| **Executed By: TBD    |  **Execution Date: TBD |

**Short Description:** <br/>
Test upload notes function with unsatisfactory input.
<br/>**Pre-Conditions:** 1. User has a verified account and is successfully logged into the system.<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.| User selects upload notes button from the main menu. | System displays the upload notes page.  |||
|2.| User specifies the course the notes are for from a list of their enrolled courses. | System updates the specified course field with the users specified element. |||
|3.| User selects the choose file button at the bottom of the page. | System displays a file browser for the user to specify their document. |||
|4.| User specifies a non PDF file they want to upload. | System determines the file the user has chosen is not a PDF, stops the upload process and displays an appropriate error message. |||

**Post Condition:**<br/>


## Successful Search for Notes


|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. : 4.2.1 | **Test Case Name: Search for Notes  |
| **System: SchoolBook         | **Sub-System: Notes Management      |
| **Designed By: Clayton Samson    |  **Design Date: 11/21/2016    |
| **Executed By: TBD    |  **Execution Date: TBD |

**Short Description:** <br/>
A user is logged into a verified account, and there are notes in the database for the desired course.
<br/>**Pre-Conditions:**
*CONTENT HERE*<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.| User selects the search bar at the top of the main page.| System takes in string input for course department and ID.|||
|2.| User presses enter or clicks on magnifying glass to confirm they are finished with their input.| System searches for any notes with that course department ID, and displays the results as a list.|||

**Post Condition:**<br/>

## Unsuccessful Search for Notes

|  | |
|----------------------------------- | --------------------------------    |
| **Test Case No. : 4.2.2 | **Test Case Name: Search for Notes  |
| **System: SchoolBook         | **Sub-System: Notes Management      |
| **Designed By: Clayton Samson    |  **Design Date: 11/21/2016    |
| **Executed By: TBD    |  **Execution Date: TBD |

**Short Description:** <br/>
A user is logged into a verified account, and there no notes in the database for the desired course.
<br/>**Pre-Conditions:**
*CONTENT HERE*<br/>

| **Step** | **Actions** | **Expected System Response** | **Pass/Fail** | **Comments**|
| ---------| ------------| -----------------------------| --------------| ------------|
|1.| User selects the search bar at the top of the main page.| System takes in string input for course department and ID.|||
|2.| User presses enter or clicks on magnifying glass to confirm they are finished with their input.| System finds no acceptable notes in the database, and displays a message stating that there are not yet any notes uploaded for the desired course.|||
