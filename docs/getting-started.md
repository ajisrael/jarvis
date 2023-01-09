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

## Create and Setup Server

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

Copy the `.gitignore` file from your client to your sever directory

Then create a `server.js` file in the server directory and get ready to start coding your backend server.

## Get OpenAI API Key

Navigate to [Open AI's website](https://openai.com/api/). If you don't have an account, click on the 'Get Started' prompt until you land on the overview page.

From there, click on your profile and then view api keys.

Then click `Create new secret key` and copy the key to your clipboard.

Now head back to the project and create a `.env` file in the project's root directory. Here you will save the API key to an environement variable like in the following example:

```bash
OPEN_API_KEY="insert api key here"
```

At this point I would also recommend creating a `.gitignore` file in the root directory that includes `.env` to make sure this key is not saved in your git history.

Now that you have your key, you can begin coding the backend of the application.

Note: for the `openai.createCompletion()` command, here are what the following fields correspond to:

```
{
  model: 'text-davinchi-003', // which model to use
  prompt: `${prompt}`,
  temperature: 0.7, // how much risk it is willing to take when formulating an answer 0 = none
  max_tokens: 64, // controls length of response
  top_p: 1,
  frequency_penalty: 0, // controls repeating of answers, 0 = no restrictions on repetition
  presence_penalty: 0,
}
```

## Running the Backend Server

Run the following command for running the server (after adding the script to `package.json`):

```bash
npm run server
```

For during development:

```bash
npm run dev
```
