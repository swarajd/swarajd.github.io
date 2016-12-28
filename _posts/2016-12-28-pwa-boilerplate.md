---
layout: post
title: create PWAs quickly with pwa-boilerplate
---

I read all these articles all over the internet on how to add this aspect of performance to your code, whether it be through code-splitting, or utilizing service workers, or tree-shaking, or something like that. And these articles are all great, but they all tend to be extremely complex and difficult for the beginner to follow.

I want there to be a way for any web developer to create an application that will be performant and progressive, and I have done so with [this](https://github.com/swarajd/swaraj-pwa-boiler) (work still very much in progress).

#### Getting Started

You'll need the following dependencies:  
  
- [yarn](https://yarnpkg.com/en/docs/install) (or you can use npm, but make sure it's the latest version)
- [node v7+](https://nodejs.org/en/)
  
##### Step 1. Clone the repository

First get the code by running the following:

~~~~~~~~
$ git clone https://github.com/swarajd/swaraj-pwa-boiler.git  
$ cd swaraj-pwa-boiler
~~~~~~~~

##### Step 2. Install the dependencies

Next, install the dependencies by running ```$ yarn``` or ```$ npm install```. (From here on out, I'll just refer to yarn but you can still use npm).

##### Step 3. Get coding!

Finally, get up and running by editing ```src/index.html``` and/or ```src/index.js```, and running ```$ yarn start```. This will start ```webpack-dev-server``` on port 8080 and will reload whenever you make changes to your app!

##### Step 4. Building your PWA and deploying 

Once you've finished building your PWA, you can build it by running ```yarn build```, which will build the PWA in the ```build/``` directory complete with a ```service-worker.js``` and a ```manifest.json```. You can deploy the ```build/``` folder using any service such as [surge](http://surge.sh/) or [now](https://zeit.co/now). An example of 
deploying using surge looks as follows:

~~~~~~~~
$ surge

    Surge - surge.sh

              email: swaraj.dhumne@gmail.com
              token: *****************
       project path: build
               size: 11 files, 34.1 KB
             domain: ready-floor.surge.sh
             upload: [====================] 100%, eta: 0.0s
   propagate on CDN: [====================] 100%
               plan: Free
              users: swaraj.dhumne@gmail.com
         IP Address: 45.55.110.124

    Success! Project is published and running at ready-floor.surge.sh
~~~~~~~~

And if you access this url: [https://ready-floor.surge.sh/](https://ready-floor.surge.sh/) and peer into devtools, you will see a service worker HAS been registered, but there is no code (yet!).



