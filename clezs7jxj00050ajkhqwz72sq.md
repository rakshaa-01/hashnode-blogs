---
title: "Angular Components"
seoTitle: "Angular Components"
datePublished: Wed Mar 08 2023 14:34:56 GMT+0000 (Coordinated Universal Time)
cuid: clezs7jxj00050ajkhqwz72sq
slug: angular-components
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678285972604/8433e93b-d00d-4002-b1af-06b60d49c377.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1678286048699/be584c19-fba6-4827-9be7-3273970089ea.jpeg
tags: angularjs, 2articles1week, devsintechblogs

---

Welcome to the sixth article in the series - **"A beginner's guide to understanding Angular"**. You can read the previous articles on this series from this [*link*](https://rakshaa.hashnode.dev/series/beginner-angular)*.*

## #1 Creating Components

We saw what components are from our [third article](https://rakshaa.hashnode.dev/angular-and-typescript-whats-the-relation). We saw that `app` is a component. Let's say we want to create another component similar to this. How do we do that?

For that, we need to create a new folder, (let's say app1) and create the three files, `app1.component.html`, `app1.component.css` and `app1.component.ts` and create the content in files similar to `app.component.html`, `app.component.css` and `app.component.css`. And instead of the 'app-root' selector as seen in the [fourth article](https://rakshaa.hashnode.dev/how-angular-loads), over here we need to use **'app-app1'** or any name you wish with the "app-" prefix. We should also import this newly created component into our `app.module.ts`. Sounds confusing to do all this, right?

Fret not, as there is a simple command to create a new component without all these steps using CLI!

```powershell
ng generate component app1
```

This command will go ahead and perform all the steps that I explained previously. As simple as that! We see that the new component is created with the selector as **'app-app1'** as we saw above.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678169023859/b3da4c88-4809-449b-abd3-4bc325cf2538.png align="center")

Now we have to link this with the `app` component that was existing by default. So go ahead and include the new component element &lt;app-app1&gt;&lt;/app-app1&gt; in `app.component.html`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678169379681/0b667937-1b8d-4847-9ce5-b1a1d7378eed.png align="center")

> If you are getting any errors as &lt;app-app1&gt; is not a known element, make sure to type line 5 extra and on line 9, type `App1Component` in `app.module.ts` file
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678169599406/0ecbf3f5-528b-439d-922d-8116e2f70676.png align="center")

Save all the changes and open the browser window.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678169750537/0bb99aad-bcd8-405d-a1ec-b9c8d4e66f65.png align="center")

***This proves that the newly created component also works properly!***

## #2 Components as selectors

Also, we saw that the components can be used as element selectors. But did you know that they can also be used as class selectors (.), property selectors, universal selectors (\*) etc? Let me explain that.

For example, If we put selector: '.app-app1', then it becomes a class selector

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678170519222/909ede21-0aef-4486-8729-b29416829bd3.png align="center")

That way, we can use 'app-app1' as a class, eg,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678172716882/973099c5-e91e-47fa-8aa1-b7a5e421be18.png align="center")

And that's a wrap-up. I hope you have learned something from this blog. If it's helpful to you and your front-end development journey then do like, follow me on [Hashnode](https://hashnode.com/@rakshaa) and [Twitter](https://twitter.com/TheRakshaa) and do subscribe to my [Hashnode newsletter](https://rakshaa.hashnode.dev/newsletter) so that you don't miss any future posts. Thanks for reading and have a great day!

*Stay tuned for the upcoming articles in this series!*