# Azure-NodeExpress
How to create and deploy your Node.js Express App into Azure using GitHub.

## Setup GitHub Repository
1. Create a new GitHub repository.
2. Add **.gitignore: Node**.

## Setup Azure Web App
1. Log into your Azure portal and click on the **New** button on the Services blade.
2. Select **Web App** in the Popular column.
3. Provide **App name**, **Resource Group** and **App Service Plan**.
4. **Create**.
5. Go into your new **Web App**.
6. Under the *Deploymnet* section in the blade. Click **Deployment option** > **Choose Source** > *GitHub* > *Enter your GitHub details* > **Choose project** > *select your repository* > **Choose Branch** > *Choose your branch*.
7. **OK**

## Install Node.js
1. Download and install Node.js 
[here.](https://nodejs.org/en/ "Node.js home page")

## Using Express Generator
1. Navigate into the working folder and open your command-line tool.
2. Install Express Generator globally by using the following command.

    > npm install express-generator -g

3. Create the application skeleton using the following command using Pug as the view engine.

    > express --view=pug **[appName]**

    *Replace [appName] with your name.

4. Install the dependencies.

    >cd **[appName]**
    >
    >npm install

5. Start your App.

    >npm start

6. Test your Node Express App: load http://localhost:3000/ in your browser.
7. Add the following key into your **package.json** file
    > **"engines": { "node": "8.9.0" }** -- this is REQUIRED for Azure.

8. Commit changes into *GitHub*.

## Conclusion
Back into your Azure portal in the Deployment option of your Web App, you should be able to see the new version deploy.