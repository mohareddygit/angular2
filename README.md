# Angular 2 data entry

This application is an opportunity to learn more about Angular2.  This time the goal is to create an application that implements the following:
- Angular 2
- TypeScript
- Pug (formerly known as Jade) for html templating
- Sass for css
- Express for services
- Browser sync for a better dev experience
- Mongodb or RethinkDb as the database

## Premise
The premise of the application developed here is that of a health journal.  It should provide the following:
* Login
* Configure healthcare providers
* Configure Insurance
* Create physician visit 
   * Date
   * Notes
   * Follow up


## Installation
```
$ git clone https://gitlab.com/nashvegastech/angular2-dataentry.git
$ cd angular2-dataentry
$ npm install -g typescript typings gulp node-sass
$ npm install
$ npm start 
```
## Folder Structure
Currently everything (almost) is in ```./src```.  From there the application is broken down into the following:
* app - Angular 2 client application components.
    * main.ts - angular bootstrap file.
* sass - sass files for use both within the Angular app or any views served by express.
* server-views - any views that we need for express to serve
* templates - pug files used for angular components.
* in the root directory the following files are used:
    * server.js - the base expressjs server
    * systemjs.config.js - called by the client to setup systemjs
    * gulp files - explained below
    * tsconfig.json - used by TypeScript
    * tsconfig.app.json - special TypeScript config for the angular 2. application. Note - it excludes the ```./src/server``` directory.
    * tsconfig.server.json - special TypeScript config for the express server.  Note - it excludes the ```./src/app``` directory.

## Quick walkthrough
*angular application*
We are using angular components to compose the application
  

## todo
1. gulp file setup
    1. compilation
    2. browser sync
2. Express setup
    1. server.js + src/server/app.ts