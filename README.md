# Okta_NodeJS

This is an SSO example using NodeJS/Express. Please follow the steps shown below to get this example working.

Step 1: Create a new project with express-generator and pug for the view.
  mkdir express-app
  cd express-app
  npx express-generator --view=pug
  
 Step 2: Before you begin, you’ll need a free Okta developer account. 
  Install the Okta CLI and run okta register to sign up for a new account. 
  If you already have an account, run okta login. 
  Then, run okta apps create. 
  Select the default app name, or change it as you see fit. 
  Choose Web and press Enter.
  Select Other. Then, change the Redirect URI to http://localhost:3000/callback and use http://localhost:3000 for the Logout Redirect URI. 
 Express uses port 3000 by default.
  
Step 3: Install Schematics CLI: Read here for more info on Schematics - https://www.npmjs.com/package/@oktadev/schematics/v/3.3.0
  npm install -g @angular-devkit/schematics-cli
  
Step 4: Install and run OktaDev Schematics with your Okta values for $issuer, $clientId, and $clientSecret:
  npm i -D @oktadev/schematics
  schematics @oktadev/schematics:add-auth --issuer=$issuer --client-id=$clientId --client-secret=$clientSecret
  
 Please note: An .env file will be generated with your client secret in it. Make sure to add *.env to .gitignore and don’t check it into source control!
 
Step 5: Start your app and authenticate with Okta! 🚀
  npm start
 
