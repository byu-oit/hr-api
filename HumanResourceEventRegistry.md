# Registry of Human Resource Events

For the Address, Email, and Phone event types there is just one corresponding event type for data synchronization. Whether data for these events is added, changed, or deleted it will always fall under the changed type event.

|Category of Event Type    |Description   |Event Types for Data Synchronization    |
|--------------------------|--------------|----------------------------------------|
|Address                   |Physical addresses used to contact members of the BYU community.<br>This includes addresses of types Mailing (MAL), Residence (RES), Work (WRK), and Tracing (PRM) as well as some other specialized address types.|Address Changed|
|Personal Data             |This includes much of a person's biographical information, such as date_of_birth, age, gender, name, citizenship, etc.|Name Changed<br>SSN Changed<br>Ethnicity Changed<br>Birthdate Changed<br>Deathdate Changed<br>Visa Changed<br>Religion Changed<br>Citizenship Changed<br>Gender Changed<br>Marital Status Changed|
|E-mail Address            |This is electronic address used for e-mail communication.|Email Changed|
|Phone                     |This is phone numbers, capabilities, and restrictions imposed by the person.|Phone Changed|
|Job Data                  |This includes much of the employee's job history such as hire, job transfer, leave of absence, and termination information.|Hired<br>Job Changed<br>Leave of Absence Changed<br>Terminated|
|Time Punches              |Includes hourly employee's time clock punches and corrections.|Punch Occured<br>Punch Changed<br>Punch Deleted|
|eForms|This includes any eForm related events.|eForm Approved by the Front Desk<br>eFrom changed|
