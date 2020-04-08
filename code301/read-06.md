# Node.js
Many web applications have a divide between the client-side (the browser) and the server side. The front end is written in one laguage and the back end is written in another. Node.js erases that divide. It is a runtime environment powered by chrome's V8 engine that allows javascript to run on your local machine or server, where before it could only run on the browser. With it javascript can create servers, monitor traffic, deal with server requests and responses and work with databases.

Node.js also differs from how most other server side work. PHP, for example, creates a new thread for every I/O operation the server received. This call lead to many threads, bogging down the server. Node.js is event, driven, asychronous, and single-threaded. When it receives a new request, it deals with it and moves on.

Paired with node, is npm, or node package manager. Npm is both an online open repo for modules, it also a way to interact with those modules. Once it and the modules are installed, a package.json file can be created with a `npm init`. This file include dependencies listing the files your application needs. This makes it easier for the modules to be installed on another developer's computer/server.