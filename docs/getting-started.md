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
