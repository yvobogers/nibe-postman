# nibe-postman
Before using, make sure you have created a NIBE Uplink account and you have registered a new application. For more information see: https://api.nibeuplink.com/Home/About

### How to use
* Import the collection and update the Variables to correctly reflect the `client_id` and `client_secret` that NIBE assigned to you. Fill in `redirect_uri` and `state` (can be anything). 

* Open the `1. Authorize endpoint` in a browser and approve the access. The browser returns your application code in a `200 OK` with a JSON response. Fill in this code in Postman in the `code` collection variable. 

* Now Send the `2. Token endpoint - Authorization Token` request. This returns an `access_token`. Fill this in as the Bearer Token in the `Authorization` tab of the `Functions` folder in the Postman collection.

* Now you can explore the `Functions` endpoints. When your access token expires, repeat the procedure or use the `refresh_token` which is returned under (2.) to regularly obtain a new access token using the request `3. Token endpoint - Refresh Token`.
