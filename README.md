# Google-Authentication-nodejs

## Google credentials
First we have to get Google credentials .
To get credentials 'if don’t already have them '  go to [Google developer Console](https://console.developers.google.com/)

>_1)create a new project
>
>2)Select the project and click credentials and the select OAuth client ID
>
>3)Now Select Web Application in application type.
>
>4)Input your app name or whatever else you like , in Authorized JavaScript origins add this line`http://localhost:3000 ` and in Authorized redirect URIs field add this line ` http://localhost:5000/auth/google/callback `  and the click to create .
>
>5)Now copy your *Google client ID* and *Google client secret*_
[Help](https://developers.google.com/adwords/api/docs/guides/authentication)

## Lets Initialize the New Project

To initialize the new project you just need to create a new folder "App name" and open folder in visual studio (or any other IDE ) code or any other IDE and run the below code in command line
```javascript
 npm init
```
Just fill the project name and any other detail or just skip. After the `package.json` file is generated .

## Structure of the project

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/k2tfjrkggumaoj2fwr2z.jpg)
As with the reference of the above image create folders and files leave node_modules package-lock and package-json as they generate automatically .

## Install Dependencies

These are the Dependencies we need to install for our project.
```
express
ejs
connect-mongo
dotenv
express-session
mongoose
passport
passport-google-oauth20
```
Install Dependencies by write the below code in your terminal
```javascript
npm i ejs connect-mongo dotenv express-session mongoose passport passport-google-oauth20
```
## Setup App for run
To start the server automatically we just need to install Nodemon which restart server automatically when any change is detected
```javascript
npm i -D nodemon
```
Setup application for developer run and normal run. Just change the Script section with the below code in package.json.
```
"scripts": {
    "start": "node app.js",
    "dev": "nodemon app.js"
  },
```
## Start local server

To start our app for testing/developer just simply type the following command in the command line:

```javascript
npm run dev
```

#### The main work is start from there

You need to just put your google client id and secret in this file. And also the mongodb uri like(`mongodb://localhost:27017/`) if you are hosting mongodb from your system . if you are using [Mongodb Atlas](https://www.mongodb.com/cloud/atlas/) it like(`mongodb+srv://XXXX:XXXX@cluster0.obaan.mongodb.net/{DBNAME}?retryWrites=true&w=majority`)

file:`config/config.env`

```
PORT = 3000
MONGO_URI=mongodb+srv://XXXX:XXXX@cluster0.obaan.mongodb.net/{DBNAME}?retryWrites=true&w=majority
GOOGLE_CLIENT_ID = XXXXXXXXXX
GOOGLE_CLIENT_SECRET = XXXXXXXXXXXXXXXX
```
