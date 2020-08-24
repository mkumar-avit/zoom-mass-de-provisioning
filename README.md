# zoom-enterprise-user-deprovisioning

Standalone Python program that manages deprovisoning or relicensing users in Zoom to basic base on either an email list of users, or their last sign-in date.  It uses the TKinter module to provide a very basic GUI interface.

Users need an API Key and API Secret with admin-level access from a JWT Token App in Zoom's marketplace.  The code will generate the JWT Token. 

The program will retrieve all users in account, check against the specified inactive data, and relicense users to Basic if they still have cloud recordings (if checked in the program) or else delete them if they also haven't been active for the specified number of months.  The program will save the user data to file, so it can be opened by the program again later.

As an option, the email list is just a list of email addresses of users with a header at the top of the csv file (i.e. Emails) that will be used to delete users from Zoom  en masse

Bugs:
This is a functional alpha release and will license and delete users from your Zoom account.  There are bugs with re-opening the saved user file generated by the program, but that will be addressed soon.



