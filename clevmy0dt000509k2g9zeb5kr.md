---
title: "Angular and Typescript - What's the relation?"
seoTitle: "Angular and Typescript - What's the relation?"
datePublished: Sun Mar 05 2023 16:56:28 GMT+0000 (Coordinated Universal Time)
cuid: clevmy0dt000509k2g9zeb5kr
slug: angular-and-typescript-whats-the-relation
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678034579679/34d9566c-f7c1-4215-95b1-dae4b9fd3a5c.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1678035346428/94ecafdc-93a1-4f86-80e2-7e9bf7d4f52a.jpeg
tags: angularjs, typescript, frontend-development, devsintechblogs

---

Welcome to the third article in the series - **"A beginner's guide to understanding Angular"**. You can read the previous articles on this series from this [*link*](https://rakshaa.hashnode.dev/series/beginner-angular)*.*

### Explaining the `app` module -

Even though you displayed **"Hello, World!"** by now on your screen, most probably you would not have been able to understand how this happened, right?

**How Angular actually works?**

An angular app is divided into various modules (eg., `app` module we see below). And each module is divided into various components. The `app` module as you can see has the following components:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677913229992/ea89fac2-c00a-426f-b1d4-95380bfcfda6.png align="center")

Every component has at least three files,

* An HTML file, which gives the template of the app -- `app.component.html`
    
* A CSS file, which gives styling to the template -- `app.component.css`
    
* A TypeScript (TS) file, which gives the logic contained in the app -- `app.component.ts`
    

In addition to these files, we see

* `app.module.ts` -- All the imports made to the `app.component.ts` file are given here
    
* `app.component.spec.ts` -- This file contains unit tests for individual components (it is required for testing and not required in development now).
    

Now, if we see the code we wrote yesterday in the file `app.component.ts`, we observe that the language we wrote was a little different from JavaScript. It is written in TypeScript. So what is TypeScript? And why it was not written in JavaScript?

### What is TypeScript?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678033011772/c1abfe27-5817-43ef-9b27-c890e3dd6be5.png align="center")

**TypeScript**, as you can see is a **superset of JavaScript**. It is a strongly typed, object-oriented language. In simple terms, anything that is included in JavaScript is included in TypeScript as well. But the reverse is not true! *TypeScript is generally used when we want to create a JavaScript-based application that can scale at an industrial level.* In the end, TypeScript compiles down to JavaScript and this compilation task is accomplished by the Angular Command Line Interface (Angular CLI).

And that's a wrap-up. I hope you have learned something from this blog. If it's helpful to you and your front-end development journey then do like, follow me on [Hashnode](https://hashnode.com/@rakshaa) and [Twitter](https://twitter.com/TheRakshaa) and do subscribe to my [Hashnode newsletter](https://rakshaa.hashnode.dev/newsletter) so that you don't miss any future posts. Thanks for reading and have a great day!

*Stay tuned for the upcoming articles in this series!*