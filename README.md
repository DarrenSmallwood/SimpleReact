### Create an empty react app using create-react-app and publish to AWS s3 bucket

#### Create empty react page
* npm install -g create-react-app
* cd c:\repos
* npx create-react-app NameOfApp
* cd NameOfApp
* npm run build


#### Create s3 bucket - requires awscli
* aws s3 mb s3://nameofapp.com
* aws s3 website s3://nameofapp.com --index-document index.html
* aws s3 sync --acl public-read --sse --delete ./build/ s3://nameofapp.com

##### Test the site
http://nameofapp.com.s3-website-eu-west-1.amazonaws.com/
