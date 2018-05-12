# PacePrintWebPortal- Web Scripting Final Project
A web portal for students to print to the Pace Print management system.

This webpage was made to be a lightweight html/css/javascript application that could be run on a server with limited accessibility. It was meant to compliment/ further add to an existent system that I built this spring which allows for mobile printing.

This project is targeted at students who:
1. don't have the Pharos Print client installed on their computers
2. don't have the PacePrint app on their IOS device
3. have an Android device (not supported)

The webpage has been added to my "pace website": tinyurl.com/paceprint aka webpage.pace.edu/wb63126p/inputform.html

The hardest part/ spent a huge amount of time on was with authentication. There was no good way (just like you said) to get the Pace banner system to work. I did implement google sign in authentication but I removed it as it would be another unneccesary step. Thus, I removed any authentication and tweaked the Firebase storage rules that allow only write requests (so random people can't just access the storage bucket)- I also added server-side code that checked that the username was correct (ex: is the 8th character of a students username either a n or p? if not, then don't attempt to print the file).

I added two demo videos on Youtube:
1. **WebPortal working with the Pace Print System** This video is a "behind the scenes" Demo of what interactions the webpage has with Firebase storage, a MacOS server running a Java program and AppleScript, and Pace's Pharos printing management system. 
LINK: https://youtu.be/1DLHm4vKw34

2. **WebPortal Student Use Case: Need to print Google Doc.** This screen recording shows the WebPortal's flexibility in that students without the PacePrint app on IOS, or students who own Android/ just simply want to print from their computers can print to Pace's printing system. This video is basically what the student experiences.
LINK: https://youtu.be/HijSgufUxt4



Things I may have added/ should have added:
-Using the things I learned about databasing, I should have played around with Firebase databasing. A mock implementation of databasing using MAMP may have further proved my understanding, however, I would not be able to run this on the webpage server. I also, have logging server side of what users print and how many.
-I think using client side javascript is considered dangerous since an attacker could meddle with the scripts. Do you think this approach is 'safe' since all that is going on is just uploading a file?

