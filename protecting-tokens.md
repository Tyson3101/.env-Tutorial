# Enviroment Variables

### This is similar to configuartion files, but hides it when sharing to github/hosting providers.

## Installation

#### To be able to use and read from .env files, You will need to install the `dotenv` node module:
##### To install it you wil need to open the console and run,

```npm install --save dotenv```

## Setup

##### First step is to create a file and name it `.env` and then require the dotenv node module
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

##### Now when you log into the bot copy this code into it:
```javascript 
  const Discord = require('discord.js') // Requires Discord.Js module
  const client = new Discord.Client() // Creates a new Client Instance
  require('dotenv') // Requires the dotenv module for reading .env files
  const youtubeAPI = process.env.YOUTUBEAPIKEY // Defines youtubeAPI with the value of YOUTUBEAPIKEY from the .env file
  const prefix = process.env.PREFIX // Defines prefix with the value of PREFIX from the .env file

  client.login(process.env.TOKEN) // Logs into the bot and accesses the .env file and gets the value of TOKEN
```

###### Note* When accesing a values from .env, Add `proces.env` in front of it with the name that contains the value.

## Using .gitignore to ignore the .env file when uploading to github, etc.
###### Note* If your hosting providers requires github, most hosting providers have .env file implementation

##### Create a gitignore file and call it .gitignore and add this code into it:
```.env```

###### Note* When ignoring files, put the name in the .ignore file

