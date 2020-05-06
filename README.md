# PWA Budget Tracker

Progressive Web Application for Budget Tracking Online/Offline

![GitHub top language](https://img.shields.io/github/languages/top/ac0712148/pwa-budget-tracker)
![github-repo-size](https://img.shields.io/github/repo-size/ac0712148/pwa-budget-tracker)
![github-last-commit](https://img.shields.io/github/last-commit/ac0712148/pwa-budget-tracker)


## Links
App: https://hidden-garden-43512.herokuapp.com/
Repo: https://github.com/ac0712148/pwa-budget-tracker


## Table of Contents
  * [Description](#description)
  * [Technology Specs](#technology-specs)
  * [Installation and Dependencies](#installation-and-dependencies)
  * [Purpose](#purpose)

  ## Description

  For this project we design and build a budget tracker that lets the user log additions to funds as well as expenses. The application also lets the user visually track their budget with the use of a chart that dynamically adjust with the transaction the user inputs. Another feature this application provides is offline functionality. This allows the use of the applications' budget tracking capabilities while being offline. These transactions are synced with the database when the application goes back online.

  ## Technology Specs

  This application runs on `Node` for the server configuration. We also use `mongoose` to structure our data and configure our transaction model. For the database we use when we go offline, `indexedDB` is used to store all pending transactions and synced to `mongoDB` when a connection is restored. To have running functionality when the site goes offline, we use `service-workers` to cache important files. The service worker is programmed to install and pre-cache, activate and remove old cached files, and fetch and intercept request call to save. For the client side, we use the `Web API` to do perform POST and GET call to the database.

  ## File Structure
```
.
├── models
│   └── transaction.js
│ 
├── package.json
│
├── public
│   ├── db.js
│   ├── index.html
│   ├── index.js
│   ├── manifest.json
│   ├── service-worker.js
|   ├── styles.css
│   └── icons
|       ├── icon-192x192.png
│       └── icon-512x512.png
│
├── server.js
│
└── routes
    └── api.js
```

## Installation and Dependencies

To install and this project in you local host, make sure this you have this projects' `package.json` in your directory. You also must have mongoDB installed to run a local database. If these requirements are met, then simply run the following command to install dependencies:
```
npm install
```
Then, once the dependencies are installed, run the following command to run the localhost application on port 3000:
```
npm start
```

## Purpose

The purpose of this project is to demonstrate the use of service-workers in progressive web applications. We use these technologies to demonstrate offline functionality with the use of indexedDB. This project is also used to show the use of the Web API to communicate with the server and store transactions.