# Application-to-P.I.-Works
question 5
[Markdown Guide](https://www.markdownguide.org/cheat-sheet/)

# User Interface Specification

## Introduction
This document outlines the specifications for the user management screen of our application. It is intended for software developers who will be implementing the user interface. The screen can list users, add new users, and toggle the visibility of disabled users.

## UI Components
The user management interface consists of the following components:

### User List
A table listing all users with the following columns at the left of the page:
- `ID`: Unique number sequence for each user increments by one and starts with 1
- `User Name`: The username for each user
- `Email`: Email address of the user
- `Enabled`: Indicates whether the user account is active or not

###User List Example
| ID ![filter photo](filter.png)| User Name ![filter photo](filter.png)| Email ![filter photo](filter.png)| Enabled ![filter photo](filter.png) |
| ----------- | ----------- | ----------- | ----------- |
| 1  | AdminUser | admin@piworks.net | true |
| 2  | Test User  | testuser@piworks.net | true |

### User Actions
- **New User Button**: Triggers a form for creating a new user account at the left of upper grey panel
- **Hide Disabled User Checkbox**: Toggles the display of disabled user accounts in the user list at right next to new user button
- **Save User Button**: Saves the new user details and updates the user list at the right of the upper grey panel
- **Enabled Checkbox**: A checkbox to set the new user account as active or not 
- **User Roles Dropdown Combobox**: A dropdown combobox to assign roles of Guest, Admin, SuperAdmin to the new user 


### New User Form
A form displayed to the right of the user list with the following fields:
- `Username`: Field to enter the new user's username
- `Display Name`: Field to enter the new user's name
- `Phone`: Field to enter the new user's phone number
- `Email`: Field to enter the new user's email address
- `User Roles`: A dropdown combobox to assign roles to the new user
- `Enabled`: A checkbox to set the new user account as active or not

## Behavior and Interaction
- Clicking on the **New User Button** will clear the new user site’s form fields 
- The **Hide Disabled User Checkbox**, when checked, will filter out disabled users from the user list table
- Clicking the **Save User Button**, the inputs will be checked for validation of proper email and phone format, non-empty username, and at least one role selection
- Clicking the **Save User Button** will check the input fields and either show an error message or add the user in the list
- Error messages will be shown next to the form field with invalid input

## Error Handling
The system should handle the following errors and provide feedback accordingly:
- Duplicate username or email
- Invalid email or phone format
- Submitting empty required fields

## Order of Tasks for User Enrolling

1. Fill out the New User form with the required details
2. Click the "Save User" button to submit the form
3. Verify that the new user's name appears in the “User List”
