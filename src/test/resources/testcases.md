**Test cases**

*ID:* tc_l1
*Pre-conditions:*
*Title:*
*Steps:*
*Expected result:*

**Login Page**

*ID:* tc_l1
*Pre-conditions:* existing user, known username and password:  test@gmail.com, logged out
*Title:* Auth with valid email and password, already existing user
*Steps:* 
1. Enter valid email, password
2. Press enter 'login' button
3. Chose english as language
*Expected result:* 
Contacts page is opened, "Contact list" block is shown

*ID:* tc_l2
*Pre-conditions:* logged out
*Title:*verify a warning message when email and password field are left empty after editing
*Steps:* 
1. left click on email field,
2. left click on free space beyond fields, 
3. verify if warning message is displayed (email required),
4. left click on password field,
5. left click on free space beyond fields,
6. verify if warning message is displayed (password required)
*Expected result:* warning messages "Email/password is required" are displayed

*ID:* tc_l3
*Pre-conditions:* logged out, login page opened
*Title:* check login button is enabled when required fields are filled with correct email and password >= 8 characters
*Steps:* 1.enter test@gmail.com into email field, 2. enter test@gmail.com into password field
*Expected result:* login button is enabled

*ID:* tc_l4
*Pre-conditions:* logged out, login page opened, email field is empty, password field is empty
*Title:* check login button is not enabled when email and password fields are empty
*Steps:* 
1. enter test@gmail.com into email field, 
2. enter test@gmail.com into password field,
3. check if login button is active
*Expected result:* login button is disabled

More TCs
check login button is not enabled when email is filled with qwe@gmail.com and password field empty
check login button is not enabled when email empty and password: 12345678
check login button is not enabled when email empty and password: 123456
check login button is not enabled when email: !!!@!!!.!! and password: 12345678
verify if the password field is of the password type



**Contacts Page**

*ID:* tc_c1
*Pre-conditions:* logged in as test@gmail.com, contacts page is opened
*Title:* new added contact is at the bottom of the Contact list
*Steps:*
1. click on 'add new contact' link
2. enter First name: 'Name' + current date/time, Last name: 'Second Name'+ current date/time, About: 'Third name' + + current date/time
3. press save button
4. press on contacts link
5. find line with entered data

*Expected result:*
1. 'add contact' form appeared, save button is disabled
2. save button is active
3. new page is opened -- Contact info, first name and last name fields contain data from field 2
4. contacts page is opened
5. new contact is at the bottom of the list

ID:* tc_c2
*Pre-conditions:* logged in as test@gmail.com, contacts page is opened, there are contacts in the list
*Title:* when contact is clicked in the contact list the contact info page of this contact is opened
*Steps:*
1. chose random contact from contact list, remember its name and click on it
2. check that contact info is the same as in contact list
*Expected result:
new page is opened -- Contact info, first name and last name fields contain data from field 2

*ID:* tc_c3
*Pre-conditions:* logged in as test@gmail.com, contacts page is opened
*Title:* adding 2 users with the same Name and Surname is possible both available at contact list
*Steps:* 
1. click on the add new contact link
2. generate random String (e.g. from datetime)
3. Enter "Tin"+random string from s2
4. click save button, write down url
5. click on the add new contact link
6. repeate step 3 with the same data
7. click save button
8. press on contact link
9. find lines with those contacts
*Expected result:*
1. Add contact dialog is opened
3. Save button is active
4. Contact info page is opened with Name and Surname entered in step 3
5. Add contact dialog is opened
6. Save button is active
7. Contact info page is opened with Name and Surname entered in step 3
8. Contact list is opened
9. two users with Name, Surname from step 3 at the bottom of the list

*ID:* tc_c4
*Pre-conditions:* logged in as test@gmail.com, contacts page is opened
*Title:* deleted contact is not visible in the contact list
*Steps:*
1. click on add new contact link
2. enter 'Name'+ current date time as name , "Surname"+ current datetime as last name
3. press save button
4. press on contacts link
5. find line with contact data
6. click on 'bin' button to delete our created contact on the line of the contact
7. confirm deletion and press remove contact
8. find line with contact data
*Expected result:*
1. Add contact dialog is opened
2. Save button is active
3. Contact info page is opened with with data from step 2
4. Contact page is opened
5. New contact is in the list
6. Remove contact dialog is opened
7. Contact list is reloaded, Remove contact message is shown for several seconds
8. Contact is not in the list