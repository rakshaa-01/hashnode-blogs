---
title: "Integrating External CSS - Bootstrap"
seoTitle: "Integrating External CSS - Bootstrap"
datePublished: Tue Mar 07 2023 13:56:32 GMT+0000 (Coordinated Universal Time)
cuid: cleybebbn000h0al5dr1chwo5
slug: integrating-external-css-bootstrap
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678173220211/bf6c9cef-afbf-4f41-9103-7c8b1c62dcac.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1678197337713/920f1a70-c24d-4393-817a-088ae584a4ac.jpeg
tags: css, bootstrap, angularjs, 2articles1week, devsintechblogs

---

Welcome to the fifth article in the series - **"A beginner's guide to understanding Angular"**. You can read the previous articles on this series from this [*link*](https://rakshaa.hashnode.dev/series/beginner-angular)*.*

So we know that Angular is a front-end framework, right? And for doing front-end development, the most important part is CSS. So for integrating CSS into our Angular app, we need to make use of a CSS framework. **Bootstrap** is a well-known CSS framework.

So, for integrating bootstrap into our project,

**(a)** Open a new terminal in your IDE and type the command shown below - `npm i bootstrap@5.3.0-alpha1`. Currently, the latest version of bootstrap is version 5.3.0-alpha1 and so we use that in the command.

```powershell
npm i bootstrap@5.3.0-alpha1
```

What this command does is, it will download all the files of bootstrap and store them in the `node_modules` folder as shown below:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678119979459/bd0684ca-e541-4f7f-86dd-71794ab44c1b.png align="center")

> node\_modules folder contains the external packages that are downloaded using npm (Node Package Manager).

**(b)** Next, for adding bootstrap to the project, navigate to bootstrap -&gt; dist -&gt; css and right-click and copy the relative path.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678161198644/9b3fac84-77d1-421e-88bb-5aaa3bba2c10.png align="center")

**(c)** Now go to the file, angular.json and paste the copied path under the styles array as shown below. While pasting kindly ensure that you change all the backslash (\\) to forward slash (/) and save the **angular.json** file.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678161597940/276a1982-070e-4a7e-86bd-31553cbfb5df.png align="center")

**(d)** You should now go to your terminal and stop the currently serving application and save all the files and start a fresh serving process.

(Do `ng serve --open`)

To check if bootstrap is working, let us go to the `app.component.html` file and type:

```xml
  <h1>
    <div class="jumbotron">
    {{ title }}   
<!--Here, title = "Hello, World" declared in app.component.ts-->
  </div>
  </h1>
```

Here, the `class = "jumbotron"` is a Bootstrap class that implements a **big box for calling extra attention to some special content or information.**

Upon saving this, in the browser window, we get,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678166257270/28d9bb1e-c8f4-4b38-ac1d-4999974b7e26.png align="center")

We remember from our [second article](https://rakshaa.hashnode.dev/project-setup-hello-world-app-angular) that we were getting just getting plain "Hello, World!" without any jumbotron effects like this,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678166567374/ccaf8c23-05b7-4033-98e4-013340ea2f71.png align="left")

***Thus, Bootstrap is working fine!***

And that's a wrap-up. I hope you have learned something from this blog. If it's helpful to you and your front-end development journey then do like, follow me on [Hashnode](https://hashnode.com/@rakshaa) and [Twitter](https://twitter.com/TheRakshaa) and do subscribe to my [Hashnode newsletter](https://rakshaa.hashnode.dev/newsletter) so that you don't miss any future posts. Thanks for reading and have a great day!

*Stay tuned for the upcoming articles in this series!*