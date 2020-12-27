# aws-amplify-demosite

Demo website for use with AWS tutorial https://aws.amazon.com/getting-started/hands-on/build-serverless-web-app-lambda-apigateway-s3-dynamodb-cognito/

## Step 1 setup

Clone the demo website from s3 to this repo

## Deploy with amplify

You can manually deploy a static site to an s3 bucket and manage updates yourself, or Amplify can do it with one touch.  Connect amplify to your git repo, and the branch you want to use for deployment.  Each time you push to that branch your site will be automatically redeployed.

## Cognito

Using cognito you can define user login flows by selecting a few configuration options. This creates a user pool which you link to your app by updating the valuse in `js/config.js` (for a web app).

Note that AWS reckon its safe enough to use the cognito pool id https://aws.amazon.com/blogs/mobile/how-amazon-cognito-keeps-mobile-app-users-data-safe/  but if people clone and run your open source app they will also be accessing your congnito setup (and you will bear the costs).

So I think best practice is to use these keys only in a private repo or use code logic somehow to retrieve the values from somewhere.  I don't know how this would work with the continual deployment but there would be a way.