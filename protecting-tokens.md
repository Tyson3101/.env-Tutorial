# Enviroment Variables

### This is similar to configuartion files, but hides it when sharing to github/hosting providers.

## Installation

#### To be able to use and read from .env files, You will need to install the `dotenv` node module.
##### To install it you wil need to open the console and run:

```npm install --save dotenv```

## Setup

##### First step is to create a file and name it `.env` and then require the dotenv node module in your main file:
```javascript
  requrie('dotenv')
```

##### Now in the `.env` file and add this code below:
```
TOKEN=Put-token-here
PREFIX=!
YOUTUBEAPIKEY=put-api-key-here
```
###### Note* The values of .env files aren't strings

## Accesing Values from .env files

##### Now in the main file of your bot add this code into it:
```javascript 
  const Discord = require('discord.js') // Requires Discord.Js module
  
  const client = new Discord.Client() // Creates a new Client Instance
  
  require('dotenv') // Requires the dotenv module for reading .env files
  
  const youtubeAPI = process.env.YOUTUBEAPIKEY // Defines youtubeAPI with the value of YOUTUBEAPIKEY from the .env file
  
  const prefix = process.env.PREFIX // Defines prefix with the value of PREFIX from the .env file

  client.login(process.env.TOKEN) // Logs into the bot and accesses the .env file and gets the value of TOKEN
```

###### Note* When accesing a values from .env, Add `process.env` in front of it with the name that contains the value.

## Using .gitignore to ignore the .env file when uploading to github, etc.
###### Note* If your hosting providers requires github, most hosting providers have .env file implementation
###### Note* A .gitignore file is for use of github only

##### Create a file and call it `.gitignore` and add this code into it:
#### `.env` This ignores the .env file when commiting to github
#### `node_modules`  This is optinal and this ignores the node_module folder when commiting to github

###### Note* When ignoring files/folders, put the name in the .gitignore file

