# ApiRTC-Angular

This project is a very simple **angular** application using **ApiRTC**. 

It is running **live** hosted on github.io : https://apizee.github.io/ApiRTC-angular/.

This is also a **tutorial** as this README lists the steps that created the project.

## ApiRTC over Angular Steps by Steps Tutorial

Starting from scratch, first install angular cli (command line interface) :

`sudo npm install -g @angular/cli`

(This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.2.12.)

Create the new angular app :

`ng new ApiRTC-angular`

`cd ApiRTC-angular`

Import angular-material that will be used to produce nice form :

`ng add @angular/material`

Import **ApiRTC** :

`npm install @apizee/apirtc@latest --save`

In `src/app/app.module.ts` add imports of modules for angular reactive forms and @angular/material.

Replaced default content of `src/app/app.component.html` with a simple form to enter conversation name and tags for remote and local videos.

Copy code from first Conversation tutorial (https://github.com/apizee/ApiRTC-examples/blob/master/conferencing/js/conference.js) in `src/app/app.component.ts` and adapt to typescript and angular.

Run `ng serve`

The application can be opened in multiple tabs to test **ApiRTC** conversation with **multiple peers**.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Deploy to 'docs' (for github pages deployment)

`ng build --prod --output-path docs --base-href /ApiRTC-angular/`

`cp docs/index.html docs/404.html`

`git add docs/*`

`git status`

`git commit -a -m "deploy"`

`git push origin main`
