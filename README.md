# ApiRTC over Angular Steps by Steps Tutorial

This project is a very simple **WebRTC** application developped in **angular** and using **ApiRTC**. 

It is running **live** hosted on github.io : https://apirtc.github.io/ApiRTC-angular/.

This is also a **tutorial** as this README lists the steps that created the project from scratch :

## Install angular command line interface

`sudo npm install -g @angular/cli`

(This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.2.12.)

## Create the new angular app

`ng new ApiRTC-angular`

`cd ApiRTC-angular`

## Import angular-material 

This will be used to produce nice form ;)

`ng add @angular/material`

## Import **ApiRTC**

`npm install @apizee/apirtc@latest --save`

## Code the application

Please check the code in this repo.

Following is the exhaustive list of modified files and how :

* In `src/app/app.module.ts` add imports of modules for angular reactive forms and @angular/material. 

* Replaced default content of `src/app/app.component.html` with a simple form to enter conversation name and tags for remote and local videos.

* Copied code from first Conversation tutorial (https://github.com/apizee/ApiRTC-examples/blob/master/conferencing/js/conference.js) in `src/app/app.component.ts` (https://github.com/ApiRTC/ApiRTC-angular/blob/main/src/app/app.component.ts) and adapt to typescript and angular.

## Run in Development mode

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

The application can be opened in multiple tabs to test **ApiRTC** conversation with **multiple peers**.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Deploy to 'docs' (for github pages deployment)

```
ng build --configuration production --output-path docs --base-href /ApiRTC-angular/`
cp docs/index.html docs/404.html
git add docs/*
git status
git commit -a -m "deploy"
git push origin main
```
