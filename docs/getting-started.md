# Getting Started

## Check for Node JS

Check for Node JS with the following command. If you don't have it, be sure to install it through [node version manager (NVM)](https://www.freecodecamp.org/news/node-version-manager-nvm-install-guide/).

```bash
node -v
```

## Create project

Run the following command to create the project

```bash
npm create vite@latest client --template vanilla
```

Be sure to select Vanilla for the framework and JavaScript for the variant (for this project)

## Install dependencies

Move into the newly created client directory

```bash
cd client
```

Then install dependencies with

```bash
npm install
```

## Download Assets

Download and unzip the provided assets for the project from [here](https://drive.google.com/file/d/1RhtfgrDaO7zoHIJgTUOZKYGdzTFJpe7V/view).
Then put them inside the client directory.

## Cleanup Project

Move the `favicon.ico` file from assets to public, delete the `vite.svg` file in the public directory, and delete `counter.js` from the client directory

## Run Project

Start the project witht the following command:

```bash
npm run dev
```

## Create Server

To begin work on the backend of the application navigate back to the root of the project, create the server directory, and enter the server directory with the following command:

```bash
cd .. && mkdir server && cd ./server
```

Then run the following command to initialize your backend application:

```bash
npm init -y
```

Run the following commands to install your dependencies

```bash
npm install cors dotenv express openai
npm install nodemon --save-dev
```

Then create a `server.js` file in the server directory and start coding your backend server
