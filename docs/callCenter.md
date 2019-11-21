# Call Center Guide

A guide for the lovely people at our totally not outsourced call center in India to help diagnose and solve problems that users face. 

## Problem: Unable unable to capture video and/or audio

user has app permissions improperly set up

ask user to refer to the provided [Technical Documentation](techinicalDocumentation.md) to set up the proper permissions

## Problem: Received an error code

User has told you they keep getting an error with a 3 digit code, use the following list for steps to take to try and solve their issue.

* ### `400 Bad Request, app made a misformatted or corrupt request`

    Restart app and if problem persists, report to Dev team with an issue code and stacktrace and log of user events

* ### `401 Unauthorized, app made an unauthorized request`

    User is not properly signed in or their 0Auth token has expired, tell user to reconnect their google/facebook/instagram account

* ### `403 Forbidden, User requested acess to forbidden content `

    - User requested fact checking on "Tiananmen Square", "Tank Man", and other variants, tell user to stop
    - User requested existential content to fact checker, refer user to local religious institution or Psychologist

* ### `404 Not Found`   

    app or user requested method or content was not found on the server, if problem persists, report to Dev team with an issue code and stacktrace and log of user events

* ### `500 Internal Server Error`

    Send message to Dev team to yell at Jason, he probably spilt kombacha on the server again 

* ### `503 Service Unavailable`

    Send message to Dev and Upkeep team to check the AWS bill, tell user their service will be back on soon, and any fact checking requests may be made to our actual call center at **1-800-IM-TOO-LAZY-TO-TYPE**

!!!info
    If any of the above does not work and/or the user is not being helpful, send them over to directly to Jason's mobile phone number.
    
    if you don't already have his mobile number, email the automatic response server with your **only** employee ID at `dev-team-head@widgets.inc`

*****

## Problem: Unable to capture video/audio
* check internet connection, attempt to connect to google and verify internet connection
* verify user has given proper permissions to the file system and camera
* verify status of internet service providers
* verify no error codes are being displayed

