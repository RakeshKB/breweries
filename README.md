Copied from: https://coursetro.com/posts/code/174/Angular-8-Tutorial-&-Crash-Course

Installation
First, you will need Node.js in order to install the Angular CLI. Head on over to http://nodejs.org , download and install it. After installation with the default settings, open up your command line / console and run the following command:
> npm -v
This should output a version number. If so, you're ready to install the Angular CLI (Command Line Interface), which is a command line tool that allows you to create and manage your Angular 8 projects.

To install the Angular CLI, issue the following command:

> npm install -g @angular/cli
 Great, now let's create a new Angular 8 project:

> ng new myapp
This will prompt you with a couple questions. Answer them according to the answers below:

? Would you like to add Angular routing? Yes                                                                          
? Which stylesheet format would you like to use? SCSS]  
Angular routing allows you to create routes between the components in your app. We'll be using Sass (SCSS) as well, so we're adding that too.

Let's hop into the folder where our new project is stored:

> cd myapp
At this point, I usually issue the command: code .  which opens up Visual Studio Code (the code editor I use) in the current folder.

Awesome, we're ready to rock now!

Running the Project
When you're developing your Angular 8 app, you will want to issue the following command in the terminal:

> ng serve -o
The -o flag is optional, but it opens up your default browser to the development location http://localhost:4200

Now, while you're developing your Angular app, every time you update a file, the browser will automatically reload (hot reloading) so that you can see the app and debug it in near real-time.

Note: When you want to deploy your Angular app, you will use a different command. We'll get to that later.

Folder Structure
It's worth dedicating a little bit of time to outline the important files and folders that you will commonly work in -- and also understand some of the under-the-hood stuff that makes Angular 8 work.

The folder and file structure looks like this in an Angular 8 project:

> e2e
> node_modules
> src
  > app
  > assets
  > environments
  ..index.html
  ..styles.scss
The e2e folder is for end to end testing. We won't be covering testing in this course, but I will do a separate tutorial on that.
node_modules is a folder you will never watch to touch, as it contains the project's dependencies.
/src contains much of your code.
/app is where you will spend the most of your time writing your Angular 8 code. It includes the routing, components, and more.
/index.html is the entry point to the app, and you generally don't touch this file.
/styles.scss is where your global CSS rulesets will reside.

Deployment
Let's say that we're happy with our app and we want to deploy it.

We first have to create a production build with the Angular CLI. Visit the console and issue the following command:

> ng build --prod
This will create a /dist folder. We can even run it locally with something like lite-server. To install lite-server:

> npm i -g lite-server
Hop into the folder: myapp\dist\myapp\ and run:

> lite-server
This will launch the production build in the browser!

At this point, you have a number of options for deploying it (Github Pages, Netlify, your own hosting, etc..).
