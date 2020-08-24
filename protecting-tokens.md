# Enviroment Varibles

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

##### Now in the `.env` file and add this code below;
```
TOKEN=Put-token-here
PREFIX=!
YOUTUBEAPIKEY=put-api-key-here
```
###### Note* The values of .env files aren't strings

## Accesing Values from .env files

##### Now when you log into the bot copy this code into it;
```javascript 
  const Discord = require('discord.js') // Requires Discord.Js module
  const client = new Discord.Client() // Creates a new Client Instance
  require('dotenv') // Requires the dotenv module for reading .env files
  const youtubeAPI = process.env.YOUTUBEAPIKEY // Access the .env file and gets the value of YOUTUBEAPIKEY
  const prefix = process.env.PREFIX // Access the .env file and gets the value of PREFIX 

  client.login(process.env.TOKEN) // Logs into the bot and accesses the .env file and gets the value of TOKEN
```

###### Note* When accesing a values from .env, Add `proces.env` in front of it.


