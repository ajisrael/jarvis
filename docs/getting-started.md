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

Now head back to the project and create a `.env` file in the server directory. Here you will save the API key to an environement variable like in the following example:

```bash
OPENAI_API_KEY="insert api key here"
```

Now that you have your key, you can begin coding the backend of the application.

Note: for the `openai.createCompletion()` command, here are what the following fields correspond to:

```
{
  model: 'text-davinci-003',
  prompt: `${prompt}`,
  temperature: 0, // Higher values means the model will take more risks.
  max_tokens: 3000, // The maximum number of tokens to generate in the completion. Most models have a context length of 2048 tokens (except for the newest models, which support 4096).
  top_p: 1, // alternative to sampling with temperature, called nucleus sampling
  frequency_penalty: 0.5, // Number between -2.0 and 2.0. Positive values penalize new tokens based on their existing frequency in the text so far, decreasing the model's likelihood to repeat the same line verbatim.
  presence_penalty: 0, // Number between -2.0 and 2.0. Positive values penalize new tokens based on whether they appear in the text so far, increasing the model's likelihood to talk about new topics.
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
