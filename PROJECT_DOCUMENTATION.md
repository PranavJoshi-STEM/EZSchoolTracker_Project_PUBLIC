# EZSchoolTracker Project Documentation
## Description:
This document provides information on functions, the creation process, known issues, and upcoming planned features.

For more information on EZSchoolTracker, please check README.md.  If you would like to collaborate on this project with me in the future, feel free to contact me at Joshipn2018@gmail.com.

## How does the client code work?
More information about each component can be found below. In short, each page is a frame, and each frame is further divided into sub-frames which hold all the widgets and text.  Whenever you switch pages, all frames are deleted and the new page's frames are loaded in.  Whenever the client switches to another page and needs to back up to the server, it posts info to the "/commands/" route found at **127.0.0.1:5000**.  It also uses "/get_data/" and "/send_data/" during the login to send data to and from the server.

## How does the server code work?
More information about the server code can be found below.  In short, it has 3 routes ("/commands/", "/get_data/", and "/send_data/") which it uses to communicate with the client.  When the server code first loads in, it decrypts data from the server_data.txt file using the key and assigns the dictionary value to server_data.  When the server backs up, it encrypts the server_data and pastes it into server_data.txt and today's archive file.

## Known Issues (will be fixed in phase 2):
- Client appears distorted on Windows computers due to the different GUI rendering systems

## Planned Features (coming in phase 2):
- Fix EZSchoolTracker on Windows operating systems
- Add more functionality to the server i.e., create more users and districts
- Allow multiple clients to connect to the server at the same time

---

## All Versions Leading to Version 1.0 (client and server):
### Version 1.0:
- (Server) Converted code to a Unix Application File so it would stand alone.
- (Client) Converted code to a macOS application file so it would stand alone.
- (Both) Wrote the README.md file.

### Version 0.19:
- (Server) Fixed bugs in the code (encrypted data twice and made it unreadable).
- (Client) Fixed bugs in the code.  Some know bugs are related to...
	- Deleting a student and then creating one with the same student ID
	- Trying to find a student before an event was selected
	- Conflicts between found_frame() and students_frame() when trying to remove/add a student to district_data when their checkbox was ticked.

### Version 0.18:
- (Server) Introduced encryption and decryption through functions encrypt_data(data, key) and decrypt_data(data, key).  The functions use AES encryption/decryption and the key is a string that is transformed and converted to be in the right format to help encrypt/decrypt.  Server data files are now encrypted.
- (Server) Fixed bugs in the code.  Included the ability to ask if the user wants to see the server_data.
- (Client) Fixed bugs in the code.

### Version 0.17:
- (Server) Removed unnecessary/unused features.  Stylized code in PEP-8.  Improved readability.
- (Client) Removed unnecessary/unused features.  Stylized code in PEP-8.  Improved readability.
- (Client) Enabled server backing up (sends district_data to the server to get backed up).

### Version 0.16:
- (Client) Made lots of small touches to the code to fix bugs, improve readability and improve features.
- (Client) Improved spacing between widgets, added more error labels and improved font and font colour.
- (Client) Made the screen update better (the program didn't have to go to the blank page and back anymore).

### Version 0.15:
- (Client) Edited generate_report_frame() so it can also confirm the report.
- (Client) Edited generate_report_frame()'s report so it also shows the highest prize someone can get as well as the top highest school scorer.
- (Client ) Edited generate_report_frame()'s report so it also can reset everyone's point scores to 0.  Asks for confirmation before deleting.

### Version 0.14:
- (Client) Made generate_report_frame() which allows users to make and delete prizes and generate a report.

### Version 0.13:
- (Client) Made edit_student_frame() on the command page which allows the user to delete and edit a student.  Fully functional.

### Version 0.12:
- (Client) Started working on command_page().  Made add_student_frame() which creates a student and adds them to district_data.  Fully functional.

### Version 0.11:
- (Client) Wrote help_page() info in help_info.py.
- (Client) Created help_page() which allows the user to find potentially helpful information.
- (Client) Added find_info_frame_func() which is a frame that allows the user to search for search word matches and navigate to a page that has a match.  Has user error labels.
- (Client) Finished help_page() code.

### Version 0.10:
- (Client) Fixed main_page() bugs and errors.  Added more error messages to it
- (Client) Made the main page more user-friendly
- (Client) Finished writing code for the main page.  Starting to code the other pages soon.

### Version 0.9:
- (Client) Put all the main_page() frames on pages.py in Main() class for easier development.
- (Client) Fixed students_frame().  It now shows all students and is scrollable.

### Version 0.8:
- (Client) Made the found_frame() which shows the result from the find_student_frame().  Fixed both found_frame() and find_student_frame().

### Version 0.7:
- (Client) Made the find_student_frame() and students_frame() on the main page.  find_students_frame() is supposed to allow the user to find a student based on Student ID # or grade and name.  students_frame() is supposed to show all the students and has a scrollable area.  The frames don't work.

### Version 0.6:
- (Client) Made the text_frame() and create_event_frame() on the main page.  Currently, doesn't automatically update the screen.  text_frame() shows the events and some hints on how use the software.  create_event_frame() makes an event and adds it to district_data.

### Version 0.5:
- (Client) Made the header as top_frame() in pages.py.  Allows the user to switch pages, see when the last backup date is (currently set to "N/A") and see the current page title.  This is shown on every page with slight modifications.
- (Client) Made a blank page so I can update the screen by going in and out of the page.
- (Client) Added data backup feature to the client which happens every time the client changes the page.  Disabled the feature until the development of the pages are done.

### Version 0.4:
- (Client) Made help_info.py to hold all the help page info.
- (Client) Made library.py to hold all the extra functions.
- (Client) Made pages.py to hold all the pages since I predict main.py will get too long.

### Version 0.3:
- (Client) Outlined all the frames on the main page, help page and command page.
- (Client) main_page() is a collection of 6 frames, it will be able to create events, mark students' attendance, find students, switch pages and more.  Haven't implemented any features yet.
- (Client) help_page() will be a simple page with information and a search box to find search word matches.   Haven't implemented any features yet.
- (Client) command_page() is a frame that allows the user to create a student, edit/delete a student, generate a report, create/delete a prize, set everyone's points to zero and confirm the report.  Haven't implemented any features yet.

### Version 0.2:
- (Server) Made "/commands/" route and coded main logic of server.  
- (Server) It can now take commands from the client, send data, give data, save data and read data as well as other features.
- (Server) Made layout of how server_data would be.
- (Client) Added error messages to login_page().  
- (Client) Connected client to server.
- (Client) Once verified, it would send you to the main page where it would show the server data.
- (Client) Made wireframes for how the app would look.

### Version 0.1:
- (Client) Created login_page() frame with widgets and buttons.  
- (Client) Made clear_page() which destroys the page for the next page to be loaded.  
- (Client) Coded main logic to change pages (main()).
- (Server) Made "/get_data/" and "/send_data/" routes.  
- (Server) Introduced variables COLOUR and LINE taken from previous projects; variables used in printing things to the console.  
- (Server) Introduced backup(), read_save() and verify_user() functions; all were taken from previous projects.