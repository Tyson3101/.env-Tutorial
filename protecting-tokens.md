# Enviroment Varibles

### This is similar to configuartion files, but hides it when sharing to github/hosting providers.

## Installation

#### To be able to use and read from .env (Enviroment Valibles File), You will need to install the `dotenv` node module:
##### To install it you wil need to open the console and run,

```npm install --save dotenv```

## Setup

##### First step is to create a file and name it `.env` and then require the dotenv node module
```javascript
  requrie('dotenv').config()
```

##### Now in the `.env` file and add this code below;
```DISCORD_TOKEN=PUT-TOKEN-HERE```
####### Note* The values of .env files aren't strings

## Reading from it

##### Now when you log into the bot copy this code into it;
```javascript 
  client.login(process.env.DISCORD_TOKEN)
```

####### Note* When accesing a value from .env, Add `proces.env` in front of it.


