---
title: "Project Setup & "Hello, World!" app - Angular"
seoTitle: "Angular project setup, Hello world in angular"
datePublished: Sat Mar 04 2023 09:40:42 GMT+0000 (Coordinated Universal Time)
cuid: cletrxros000708l06epo8i2a
slug: project-setup-hello-world-app-angular
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1677922238764/a9a1b436-90c8-49e2-b303-51e16e87ab14.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1677922783044/06b33f0c-f398-4a04-87b8-3e049d8dd1bf.jpeg
tags: angularjs, nodejs, setup, hello-world

---

Welcome to the second article in the series - **"A beginner's guide to understanding Angular"**. You can read the previous articles on this series from this [*link*](https://rakshaa.hashnode.dev/series/beginner-angular)*.*

Having understood what Angular is from our previous article, we will proceed with the project setup and see how we can write our first "Hello, World!" app in Angular.

## Project Setup -

### #1 Installing NodeJS

To get started with using the Angular framework, we need NodeJS. Node.js is a platform built on Chrome's JavaScript runtime for easily building fast and scalable network applications. Also, NodeJS takes part in loading the AngularJS application with all its dependencies, such as CSS files and JavaScript files in the browser. So, if you don't have NodeJS installed on your PC, go to the [NodeJS website](https://nodejs.org/en/) and download the LTS version (Recommended for most users) for your operating system. Run and install the setup file downloaded.

> **To check if NodeJS is properly installed on your PC, open your command prompt and type node in the command line. If a JavaScript console opens up with "&gt;", then NodeJS is installed properly.**

### #2 Installing Angular

Now exit from the JS Console by typing .exit and in the command line type the below command to install Angular (as given in [Angular Docs](https://angular.io/guide/setup-local))

```powershell
npm install -g @angular/cli
```

`(g here refers to global install, which can be accessed from anywhere on your computer)`

Accept the defaults by pressing the Enter or Return key. After the processing bar is complete, the project setup is done. Create a new folder and create the first angular app (*named first-app*) as shown below. The `ng new first-app` command will create the first-app folder which has everything you need to create the first app.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677906322786/eb4134c5-8999-40d7-b785-74de75e599cb.jpeg align="center")

---

## Writing our first app -

### #1 Default Angular app

You can install any IDE to proceed to the next step, eg: [VS Code](https://code.visualstudio.com/download). Open the first-app folder we created in the IDE. The files and folders look similar to the one shown here.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677906377633/449773d7-2b3e-450f-becd-68f15603826f.jpeg align="center")

*All of these different files and folders don't make sense to a beginner, but proceeding with the upcoming articles published in this series will help you understand them!*

Let us now see what the app that Angular ships with looks like. Open up a new terminal in the IDE and type,

```powershell
ng serve --open
```

This command will serve the app on [localhost](https://en.wikipedia.org/wiki/Localhost#:~:text=In%20computer%20networking%2C%20localhost%20is,via%20the%20loopback%20network%20interface.) in your default browser at port number 4200. The app will look as shown below.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677909452820/150fdf85-909d-4794-a962-2e60a52d1332.jpeg align="center")

### #2 Understanding the default Angular app

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677911740740/67d2aa87-b825-43bd-abb5-f13102dee848.png align="center")

If we open `app.component.ts` and `app.component.html` files from **src -&gt; app**, we can see that these lines together result in the line "first-app is running!" as shown below.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677911859672/174555d7-b547-4070-9eaf-39f3523158a3.png align="center")

Here, 'first-app' word is replaced in place of {{ title }} in `app.component.html` as `title = 'first-app'` is assigned in `app.component.ts`

### #3 Displaying "Hello, World!"

So to display "Hello, World!", we are going to delete all the contents in the `app.component.html` file and replace them with the one shown below.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <h1>
    {{ title }}
  </h1>
</body>
</html>
```

As for the `app.component.ts` file, we will just change the title = 'first-app' to <mark>title = "Hello, World!"</mark> and save the changes in both the files.

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'Hello, World!';
}
```

Now, if we open the browser, it would display as,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677912869327/cace6c61-d426-4ad2-a06c-e279913db1dc.png align="center")

*Hurrah! We have created our first Angular app!*

*Let's understand how Angular actually works and other interesting stuff in the upcoming articles. Stay tuned!*

---