# watch2gather
Watch movies to gather online together [Movie Planner]

Build / Deployment Instructions

Build Instructions:

This application was built using MERN Stack. We have used Node Package Manager (NPM) for the entirety of the application
and anyone with the source code can easily reproduce the steps to build the application.

The steps to build the application are:

1) Download the entire project from GitLab via git clone <git url>.

2) Once cloned, open the project in your IDE of choice or open the folder in Command Prompt (CMD).

3) First, go to the ‘client’ folder using “cd client”.

![image](https://user-images.githubusercontent.com/48622120/186283317-f2654565-1e5e-4573-bcc6-24a97f8fc873.png)

4) Run “npm install” to install all the dependencies and libraries the application requires on your local machine.

![image](https://user-images.githubusercontent.com/48622120/186283348-0235a9cb-2c05-41bb-ab5b-2d69195329ae.png)

5) This will take a little while to install all the dependencies based on your Internet connection.

6) Once the installation is complete, you can run the program using “npm start”.

![image](https://user-images.githubusercontent.com/48622120/186283370-41cc1434-134d-4273-aee0-893cac303154.png)

7) This will open a “localhost:3000” instance on your default browser and start running the   application’s frontend.

8) Now, open another terminal in the root project directory and go to the ‘server’ folder using “cd server”.

![image](https://user-images.githubusercontent.com/48622120/186283398-b3c3aa7f-3a65-4d57-9961-51806ccb68e2.png)

9) Run “npm install” to install all the back-end dependencies and libraries this application requires.

![image](https://user-images.githubusercontent.com/48622120/186283433-a4c34b10-1cc6-403f-9493-ef501b2be915.png)

10) Once the installation is complete, run “npm start” to start the back-end.

![image](https://user-images.githubusercontent.com/48622120/186283471-ac251ae5-9ddd-470f-836f-21d4d25f1dd8.png)

11) Now, you have successfully built and started running the application on your local machine.

Deployment Instructions:

We have deployed this application on Heroku through CI/CD Pipeline and these steps will help in a successful deployment of this application on Heroku.

The steps to deploy the application are:

1) Create an Heroku account if you don’t already have one on https://id.heroku.com/login.

2) Once you have created an account, log in to your account and you will be redirected to the Dashboard.

3) There will be a “New” button from which you will need to click “Create new app”.

![image](https://user-images.githubusercontent.com/48622120/186283524-0cdf24ad-3237-455f-9abc-2a1d1a840160.png)

4) When you click on “Create new app”, it will ask you to provide a project name and select a region. Choose whatever name you like and it will let you know if that project name is available or not. You can choose whichever region you want. For this project, we have used “United States” as our region for our application.
5) After successful creation, you will be sent to the Project page.

![image](https://user-images.githubusercontent.com/48622120/186283556-7f55ea30-654a-465b-b908-b2d12e96e9cd.png)

6) We have created 2 projects for Develop branch - “watch2gether-front-end-dev” and “watch2gether-back-end-dev”, 2 projects for Staging branch - “watch2gether-front-end-staging” and “watch2gether-back-end-staging” and 2 projects for Main branch - “watch2gether-front-end-main” and “watch2gether-back-end-main”

7) To successfully deploy, we need to set some Configuration variables and add Buildpacks to our Heroku application.

8) Go to the “Settings” tab on your dashboard.

![image](https://user-images.githubusercontent.com/48622120/186283588-c8a14933-6314-4c2f-8dec-218590fba1f9.png)

9) Scroll down and find the “Buildpacks” section. There is an “Add buildpack” button over there, click on that. It will let you select a project or add a URL.

10) For front-end applications that use ReactJS, we are using the following Buildpack - https://github.com/mars/create-react-app-buildpack.

11) Add the above url and “Save changes” to add the buildpack to your application.

12) Finally, you have completed all the necessary changes to be made to your front-end application on Heroku. Now, let's move to the back-end application on Heroku.

13) Redirect the same above steps from Step “c” to Step “i” to create an app on Heroku.

14) After going to the Settings tab, for the NodeJS back-end application, you need to add the following Buildpack - https://github.com/heroku/heroku-buildpack-nodejs.

15) Add the above url and “Save changes” to add the buildpack to your application.

16) Now, just above the Buildpack section, there is a “Config Vars” section.

![image](https://user-images.githubusercontent.com/48622120/186283657-dc9d5ef7-45df-4f3e-9100-627e55cdea07.png)

17) We have to add the “JWT_SECRET” and “MDB_CONNECT” variables which are the “JWT Token Secret” and “MongoDB Connect” variables which will establish connections between our application and jwt and mongodb.

18) To generate a “JWT_SECRET”, go to https://jwt.io/ and generate a new Encoded token. Copy the token and add “JWT_SECRET” in Key and the token generated in the Value column of the Config Vars.

19) Similarly, create a new project in MongoDB. If you do not have an account, create an account.

20) Once you have created a new project, go to the “Atlas” tab -> “Database Deployments” and click on the “Connect” button beside your project’s name.

![image](https://user-images.githubusercontent.com/48622120/186283683-ca76e79a-6887-480d-814f-05565c4dcf77.png)

21) Choose “Connect your application” and select “NodeJS”.

![image](https://user-images.githubusercontent.com/48622120/186283717-0669db03-6af4-4bf6-b111-a669b25cca35.png)

22) Copy the connection string, add your password for the Project in the space provided in the connection string and paste the complete string to your Config Var for Key - “MDB_CONNECT” and value being the connection string.

23) Finally, after adding the config vars, you are all set for the complete front-end and back-end application deployment on Heroku.

