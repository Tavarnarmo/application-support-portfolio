# Issue with logging in
## Problem
The user tried to log in to WolfERP, but only a loading spinner appeared. The user remained on the login screen and no error message was displayed.
## Additional information
Caps Lock was off.
The user entered the password manually and still couldn't log in.
There had been no recent application update.
The user successfully logged in at around 8:00 AM the same day, but couldn't log in at around 2:00 PM.
After restarting the application, the issue was still present.
The internet connection and email worked normally.
## Diagnostics
After checking the account:

The account was active and not locked.
The password had not expired.
The system showed no failed login attempts.
The user's permissions appeared normal.
No failed login attempts despite multiple login attempts by the user seemed suspicious, so I asked the user to try logging in on another computer. The login was successful.
After that, I assumed that the issue was related to the user's computer and checked the Knowledge Base for possible causes. I found that the issue could be caused by 
an incorrect date, time, or time zone setting. On the user's computer, the date was correct, but the clock showed 16:31 when the actual time was 18:31. 
The time zone was set to UTC+01 and automatic time zone settings were disabled.

I corrected the time on the user's computer and then asked the user to try logging in again. The login was successful.
## Root cause
The root cause was an incorrect system time on the user's computer.
## Result
After correcting the time on the user's computer I asked the user to try logging in again. The login was successful.
