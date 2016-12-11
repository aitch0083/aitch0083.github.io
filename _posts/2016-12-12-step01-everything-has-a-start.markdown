---
title:  "Step01 Everything has a start"
date:   2016-12-12 00:50:00 +0800
categories: basics
---

###Goal: To start a kraken.js server with modified text
###How I do this

First, I need to install the kraken.js in the working enviroment. The process is simple, just open a terminal (I love terminal, btw) and type:

```
npm install -g yo generator-kraken bower grunt-cli
```
This line install 4 things yo, kraken, bower and grunt-cli. Holy shi*t, why is so complicated to install a runnable template? I just want to have that `Hello world` impact when I first learned **Turbo C**. So it means I have to have the basic knowledge of these 4 things:

1. [Yo](https://www.npmjs.com/package/yo#whats-yeoman)
2. [Kraken](http://krakenjs.com/#templates)
3. [Bower](https://bower.io/)
4. [Grunt](http://gruntjs.com/)

Not to mention these 4 are not the most cutting-edge stuff on the table, like, WebPack, Gulp, and you know...

Alright, even they aren't the latest, but I like Kraken. I tried [Sails.js](http://sailsjs.com/) before. It's great, but its Waterline (I always recall it as Waterpipe) is like:

![oh-no-hell-no](http://www.relatably.com/m/img/sassy-black-woman-memes/51202167.jpg)


And I found Kraken, with introduction like:

> It's an [Express]() middleware!

Oh man, that's exact what I want. Since it's a middleware, I can plug in/off any middleware I think it's suitable. Kraken comes with other 4 companies:

+ Lusca (Application Security)
+ Kappa (NPM Proxy)
+ Makara (Dust i18N)
+ Adaro (Dust Templating)

I am gonna use React as my template engine, so I just pass Adaro and Makara. 

**Enough of the trash talk!**

After installing the node modules, run:

```
yo kraken
```

You shall SEE:

```
     ,'""`.
hh  / _  _ \
    |(@)(@)|   Release the Kraken!
    )  __  (
   /,'))((`.\
  (( ((  )) ))
   `\ `)(' /'

Tell me a bit about your application:
```
Then you have to answer the questions of Norns! Nothing special really, just being cautious when it comes to:

```
? Template library? (Use arrow keys)
  Dust (via Makara 2)
  Dust
❯ None
```
Choose `None` here, since I am determined to use React. And:

```
? Include i18n support? (Use arrow keys)
  Yes
❯ No
```
Hell no, I am gonna use [react-intl](https://github.com/yahoo/react-intl) (or not~).

For the following questions:

+ `Bower` for Front end package manage
+ `None` for CSS preprocessor library
+ `None` for JavaScript library

After answering these questions. Kraken has to fight with Norns, it might take few minutes, it's a good time to take a leak. Run the server with:

```
$ I-AM-CONSOLE > nodemon server
```

Thou shall see:
``` 
{ name: 'index' }; //it's a plain JSON object, since there is no rendering engine setup yet
```

Play with the model class in `models/index.js` to see the different output. That's it. 

Let's keep the rendering part to the next post.