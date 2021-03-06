---
title: Quickstart for DHIS2 App Development
category: guide
layout: page
---

# Quickstart for DHIS2 App Development

## Create a new app and connect it to a local DHIS2 instance in 10 minutes or less.

### Introduction
You can start developing a DHIS2 app on OSX, Windows or Linux using Docker and the DHIS command line interface (CLI). In this guide, you will install the prerequisites, start up a local DHIS2 instance and create a new app. Your app will connect to the local DHIS2 instance.

### Installing prerequisites
If you are using Debian Linux, 
1. Follow the [DHIS2 Docker guide](https://developers.dhis2.org/guides/dhis2-docker) to install the prerequisites

If you are using OSX or Windows,
1. Install [Docker](https://docs.docker.com/get-docker/)
3. Install [yarn](https://classic.yarnpkg.com/en/docs/install)
4. From the command line or terminal, install DHIS CLI
```
yarn global add @dhis/cli
```
Now that you have installed Docker and the DHIS CLI you are ready to start up DHIS2

### Starting a local DHIS2 instance

1. From the terminal, start up DHIS2 and seed the database
```
d2 cluster up 2.35.0 --db-version 2.35 --seed
```
2. From the browser, navigate to http://localhost:8080. If DHIS2 is running, you should see the following page,
![](../assets/quickstart_guides/image-of-login.png)

If you can load DHIS in the browser, you are ready to create a new app

### Creating a new app
1. From the terminal, create a new DHIS2 app called "my-app"
```
d2 app scripts init my-app
```
2. Change directories to `/my-app` and start the app
```
cd my-app && yarn start
```

### Connecting your app to DHIS2
1. From the browser, navigate to http://localhost:3000. You will see the following page
![](../assets/quickstart_guides/new-app-login-page.png)
2. Enter your DHIS2 server url and the username and password of the default admin user
```
server: http://localhost:8080
username: admin
password: district
```
3. You will see the default admin user name and a welcome message
![](../assets/quickstart_guides/new-app-login-success.png)

Congratulations! You are ready to start developing a DHIS2 app 🎊 

### Next steps
Now that you have created a DHIS2 app and connected it to a local DHIS2 instance you can learn more about developing apps on DHIS2. 
- Learn more about DHIS2 apps from the [developer documentation](https://docs.dhis2.org/dhis2_developer_manual/apps.html)
- Watch training videos from the [developer academy](https://www.youtube.com/playlist?list=PLo6Seh-066RynhjhnJNUITOZykA7397We)