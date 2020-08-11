# MFP Postman Authentication
Postman collection to authenticate with postman using actual credentials

In order for this to work you will first need to create a new web app in MFP for postman. If you already have a web app set up you can reuse that appid. The new app will need to have access to the LoggedIn scope or any scope you which to test.

There are 4 environment variables that the collection will need in order to work. 
1. HOST - The url from the mfp server ex. https://dev.ex-mfp.com
2. username - The username for the user you want to authenticate
3. password - The password for the user you want to authenticate
4. mfp_app_id - The MFP web app id that you initially set up in MFP.


The collection is broken down to 3 calls. 
1. Create Session - The create session endpoint is needed to set up a session between Postman and MFP.
2. Login User - Is where the actual authentication happens with MFP
3. Get Access Token - Will retrieve the access token to be used for future calls. This will create a new variable called 'manual_token'. You can use this token is any future calls with MFP to access authenticated endpoints.

