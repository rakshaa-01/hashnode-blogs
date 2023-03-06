---
title: "How Angular loads?"
seoTitle: "How Angular loads?"
datePublished: Mon Mar 06 2023 18:00:14 GMT+0000 (Coordinated Universal Time)
cuid: clex4nv6w000109l7ch479wzd
slug: how-angular-loads
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678125472578/1671a1a1-956f-44d6-a7fa-d7d41872a724.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1678125569611/57ce243c-0597-4320-8b40-fcbc1444ed49.jpeg
tags: angularjs, 2articles1week, devsintechblogs

---

Welcome to the fourth article in the series - **"A beginner's guide to understanding Angular"**. You can read the previous articles on this series from this [*link*](https://rakshaa.hashnode.dev/series/beginner-angular)*.*

We saw what components and modules are from our [third article](https://rakshaa.hashnode.dev/angular-and-typescript-whats-the-relation) in this series. But how do these different components get served when we saw "Hello, World!" on our screen from the [second article](https://rakshaa.hashnode.dev/project-setup-hello-world-app-angular)?

To understand that, let's go to our browser window of the hello world screen and do Right-click -&gt; View Page Source, then the screen on the right side appears:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678124622725/85617e0d-f0c9-41a3-b090-cd8918f0ba9b.png align="center")

*(Note: If your output browser screen is not visible or you have accidentally closed, go to your IDE, open up your project folder, open up a new terminal and type* `ng serve --open`*)*

We see that there is an &lt;app-root&gt; element as highlighted above. From our basics of HTML, we know that HTML does not have any &lt;app-root&gt; element by default. This new element that appears in the 'Page Source' is custom-built by Angular. So how did this element appear?

So, in our [second article](https://rakshaa.hashnode.dev/project-setup-hello-world-app-angular) of this series, we saw that once we type `ng serve --open` the "Hello, World!" page was served in the browser. The page that was actually getting served by this `ng serve` process was this **index.html** file.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678122547399/330dd646-4c52-44b2-9c8a-0002c2c0b478.png align="center")

If we see line number 11 in this file, we again see the &lt;app-root&gt; element here. This confirms that the page that was served in the browser and the **index.html** file are the same.

Similarly, if we open `app.component.ts` file, we see that there is a selector: 'app-root'. This specifies that the 'app-root' <mark>selector</mark> is used for recognizing the &lt;app-root&gt; element which is then used for selecting custom made template from <mark>templateUrl</mark> (HTML page `app.component.html`) and <mark>styleUrl</mark> (CSS page `app.component.css`).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678123081962/0b5f6fe8-8947-4830-9b3f-0b1711c2c435.png align="center")

Simply put, when a **&lt;app-root&gt;** component is present in **index.html** file, Angular knows that it has to serve `app.component.html`, `app.component.css` and `app.component.ts` files. It knows this because the &lt;app-root&gt; element is tied with the selector 'app-root'. (As seen above)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678123252905/55eac38b-fdc8-4419-b6a4-7e69a31b495f.png align="center")

This understanding of how angular loads is very important in future debugging processes.

And that's a wrap-up. I hope you have learned something from this blog. If it's helpful to you and your front-end development journey then do like, follow me on [Hashnode](https://hashnode.com/@rakshaa) and [Twitter](https://twitter.com/TheRakshaa) and do subscribe to my [Hashnode newsletter](https://rakshaa.hashnode.dev/newsletter) so that you don't miss any future posts. Thanks for reading and have a great day!

*Stay tuned for the upcoming articles in this series!*