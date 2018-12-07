
Approach:

To implement logs, I first read the documentation to understand the basics of creating a log and viewing logs. I decided that I wanted to log when a note was created and by whom. My initial idea was to place it in the class initializer in models.py but I couldn't find a way to get the name of the user who added the PersonalNote. Then, I moved the line to create() function in api.py where there is a user variable that I can utilize. Initially this didn't seem to work because I was creating new PersonalNotes via the Django admin. Once I realized my mistake and tried adding PersonalNotes via the API, I was able to get a log entry when a PersonalNote is created. To create logs when PersonalNotes are added via the admin page, I think we will need to write a create() function in views.py. This will be a task for another time. Limiting the logging portion to just API posts would work fine, however, because users who are not superusers currently have no way of adding PersonalNotes via the admin page.
