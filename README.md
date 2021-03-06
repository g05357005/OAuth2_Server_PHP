# OAuth2_Server_PHP
- Creating an OAuth2 in PHP
- Creating An API for implementing OAuth2
- index.php redirects you to login page of your website


## How to implement
- Clone/Download the repo in your PC.
- Unzip the folder in htdocs (if using xampp) or www/html/ (i.e. root folder of the web server).
- Start the server in your PC.
- Open your web-browser and go to [http://localhost/OAuth2_Server_PHP/](http://localhost/OAuth2_Server_PHP/)
- Click on button "LogIn By OAuth2". Cheers :) your OAuth2 server is running.
- For more details about functionality please read the following description.


## api_server

**index.php authenticates the user ( We call it AUTHENTICATION SERVER )**
    - If the user click on "Allow", the service redirects the user-agent to the application's redirect URI, and returns a URI fragment containing the access token.
    - If the user clicks "Deny", the service redirects back to login page.

**resource.php provides data to client ( We call it RESOURCE SERVER )**
    - The application extracts the access token from the full URI that the user-agent has retained and returns
    user data in JSON format.


## client+oauth_server

**index.php contains the login page of your website ( We call it CLIENT SERVER)**
    - If user clicks on "Login By OAuth2" then it redirect to /api_server/index.php where it will be prompted by the service to allow or deny the application access to their account.

**profile.php**
    - The user-agent executes the provided script and passes the extracted access token to the application.

**oauth2.php ( We call it OAuth SERVER )**
    - It is the simple implementation of OAuth2.0 library.

**config.inc.php contains private configuration values**

    It defines:
    > $apiKey (consumer_key)
    > $consumerSecret (consumer_secret)
    
## Currently Working on

**Nonce and Timestamp implemenation in API Server**


