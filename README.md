# EZSchoolTracker
## Please see:
This is a copy of EZSchoolTracker_Project made by Pranav Joshi (me).  Unlike EZSchoolTracker_Project, this repository does not contain the source code (in order to stop people from stealing the program and claiming ownership).  Instead, EZSchoolTracker_Project_PUBLIC only has the standalone applications, the data and the markdown files.  If you would like to see the code, please contact me at Joshipn2018@gmail.com.  NOTE: The standalone files only appear as 1 file when downloaded on macOS; otherwise, it looks like multiple macOS related folders.
## Description:
This project was built as a client-server application.  Version 1 was released on February 26th, 2023.

For more information on how EZSchoolTracker was made, please check PROJECT_DOCUMENTATION.md.  If you would like to collaborate on this project with me in the future, feel free to contact me at Joshipn2018@gmail.com.  **This project requires Python 3 and the following libraries to run the scripts and a recent version of macOS to run the Unix Executable File and application file.  Note that running the client scipt on an operating system other than macOS may look distorted.**

### Problem Statement: ###
In a role-play scenario created by FBLA (Future Business Leaders of America), attendance at school events is at an all time low.  To combat this, an application must be made which rewards students for coming to events by giving them prizes at the end of each quarter of the year.  The application must be easy to use, have several GUI functions, be intuitive to use and must solve the primary problem.

### The Goal of EZSchoolTracker: ###
EZST (EZSchoolTracker) is an application designed to encourage student attendance at events by allowing staff to create events, prizes, and mark students' attendance.  There are also several other features in this project such as the ability to edit/delete a student, make a student, delete a prize, generate a report, confirm a report, set everyone's points to 0, and delete an event among more features.

### Choosing Python and Tkinter: ###
Based on previous research, Python was the langauge chosen to be used for this project due to its simplicity and its wide array of libraries.  Following this, 2 graphical libraries could be chosen for this project, Pygame and Tkinter.  From the 2 options, Tkinter was found to be easier to code with.

### Challenges, lessons, and future goals: ###
Throughout the project, many challenges and lessons were overcome and learned.  Prior to EZSchoolTracker, I lacked knowledge of how backend servers work, encryption, and how to make a nice-looking client GUI.  After the release of version 1.0, I learned these topics among many more and can now efficiently make client and server applications.  In the future, I would like to dwell more into application development and make a stronger backend.

## How to Run the Project:
### Dependencies:
Both the client (macOS application file) and server (macOS Unix Executable file) stand alone files have all the dependencies needed to run.  **Nothing is required to run the stand alone client and server files other than a recent version of macOS.**

**Note:** 
- Some libraries come installed with Python (pip is needed for installation).  
- **A version of at least python 3 is required**.
- The client scripts on Windows look deformed compared to macOS due to the differences in the operating systems.

**Libraries used in making the server:**
- Flask
- Datetime
- Json
- Ast
- PyCryptodome
- Hashlib
- OS

**Libraries used in making the client:**
- Tkinter
- Requests
- Ast
- Json
- Datetime
- TkCalendar (not the same as Tkinter)
- Random

### Details to read before running the project:
 ⚠️  **Notes about running the project:**
- The server can only handle one client at a time
- You must start the server before the client is used
- The server must be in the same directory as the server data.  If the server data is encrypted with a different key, is corrupted, missing or is messed up in any other way, **the code will not work**.  Below is an example of how the directory should look with a Unix Executable File:
	- *EZST Server* - Unix Executable File
	- *server_data.txt* - Text file (should be encrypted with a key)
	- *data/* - Folder with data backups
- The IP address 127.0.0.1 at port 5000 should be allocated for the server
- **Please run the code on macOS**

## How to load each file:
### **The server file:**
Open a folder called "EZSchoolTracker Server - Standalone Mac OS Program" and click on "EZST Server (Version 1 - Mac OS)"; it is a Unix Executable File.  Please wait 30 seconds for it to load.

### **The server script:**
This is if you want to run the script instead of the standalone file (note, you need the libraries and at least Python 3 installed to run it).  Open a folder called "EZST Server Code" and run "main.py".  Please wait 30 seconds for it to load.

### **The client file:**
Open a folder called "EZSchoolTracker Client - Standalone Mac OS Program" and click on "EZSchoolTracker (Version 1 - Mac OS)"; it is a mac application.  Please wait 30 seconds for it to load.

### **The client script:**
This is if you want to run the script instead of the standalone file (note, you need the libraries and at least Python 3 installed to run it).  Open a folder called "EZSchoolTracker Code" and run "main.py".  Please wait 30 seconds for it to load.

**If your macbook refuses to load the standalone files because it can't scan it for errors, please refer to the "FAQ" section of this document and follow the steps mentioned under "Why does my macbook refuse to run the stand alone files?"**

---

### ⚠️ Steps to running the application:  
1. When you run the server first, please wait 30 seconds for the server to start.  It will ask if you want to see a decrypted version of the server_data; please put it in your input.  Please note that the server doesn't start until it gets a response from the user back.  After this, the server will start but immediately pause to ask you the question again (this is after flask is loaded); please enter your input again.  After this point, the server has started.  **If you don't see "Debugger PIN: 473-479-686", that means the server is not currently working.  Please continue responding and looking at the terminal until you see it.**  If you want to view the server_data, please use the encryption key "FBLA" to gain access to it.

2. Click on the client file and wait for 10 seconds.  At first, a window will pop up and then close.  Please wait for 10 more seconds and the client should load.

3. Use the client as you wish.  Just make sure that you close the client first before closing the server.

---

## How To Use The Program:
**Steps to run the program are listed above!**
If you want to use the client, here are some credentials you can use to log in and start trying out EZSchoolTracker:
- **Username**, **Password**, **District**
- 123456@development.com, abc123, development (Note, since the district is different, this won't have the same access to data as the accounts at the "demo" district)
- Viewer@demo.com, DEMO_1, demo
- Coder@demo.com, DEMO_2, demo

**If you want to view the server_data, use the encryption key "FBLA" to gain access to it.**

If you're curious on how the program works or how it was made, please check the project documentation.

## FAQ:
### **I accidently corrupted the server data**
Close the client and server.  Then, copy the data from the most recent file in the "data/" folder and paste it into the "server_data.txt" file.

### **How does this work?  How was it made?**
If you're curious about how the program works or how it was made, please check the project documentation.

### **Why does the client stand alone file look like a folder?**
If the client stand alone file appears like a folder on your operating system, this is most likely because you're running an operating system other than macOS.  Please run the scripts and standalone files on macOS only.

### **Why does my macbook refuse to run the stand alone files?**
When you try to run the client/server stand alone file, macOS will try to scan it for errors (which it can't).  First, run the application once and quit the mac message.  Then, right click on the file in Finder and click open.  On the message the mac gives you, click Open.  Voila, you should be able to run the stand alone files.

### **I have other questions**
Please check the "Contact Me" section below to find my email.

## Contact Me:
If you want to talk to me regarding any glitches, problems, questions or concerns, feel free to contact me below!

Email: Joshipn2018@gmail.com

## Information:
1. This project was made for the 2022/2023 FBLA CNLC competition.  
2. The prompt can be found here: [Coding_and_Programming_Event_Guide - Google Docs](https://docs.google.com/document/d/1atFHEy1No_Zya4elXRC3GFo_Iu7NPs6-hFDMJ8fIweg/edit).  
3. Version 1 (what was submitted to CNLC) was completed on February 26th, 2023.
4. This project was entirely made by me, Pranav Joshi.
5. If you want to use this project at all, you need to contact me for permission.
