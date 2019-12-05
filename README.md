# LAB - l34-todo-login-and-auth

## Todo Login-and-Auth

### Author: Jonathan Kimball

### Links and Resources
* [submission PR](https://github.com/401-advanced-javascript-kimball/l34-todo-login-and-auth/pull/1)
* [travis](https://travis-ci.com/401-advanced-javascript-kimball/l34-todo-login-and-auth)

* [back-end](http://xyz.com) (when applicable)
* [front-end](http://xyz.com) (when applicable)

#### Documentation
* [api docs](http://xyz.com) (API servers)
* [jsdoc](http://xyz.com) (Server assignments)
* [styleguide](http://xyz.com) (React assignments)

### Modules
#### `modulename.js`
##### Exported Values and Methods

###### `foo(thing) -> string`
Usage Notes or examples

###### `bar(array) -> array`
Usage Notes or examples

### Setup
#### `.env` requirements
* `PORT` - Port Number
* `MONGODB_URI` - URL to the running mongo instance/db

#### Running the app
* `npm start`
* Endpoint: `/foo/bar/`
  * Returns a JSON object with abc in it.
* Endpoint: `/bing/zing/`
  * Returns a JSON object with xyz in it.
  
#### Tests
* How do you run tests?
* What assertions were made?
* What assertions need to be / should be made?

#### UML
Link to an image of the UML for your application and response to events

----------

# LAB -  `<Login />` and `<Auth />`

Using Login Context, "protect" the To Do application by restricting access to the various application features based on the users' login status and capabilities.

## Before you begin
Refer to *Getting Started*  in the [lab submission instructions](../../../reference/submission-instructions/labs/README.md) for complete setup, configuration, deployment, and submission instructions.

## Getting Started

Starter code has been provided for you in the `/lab/starter-code` folder.

Open [Code Sandbox](http://codesandbox.io) and Create a new application. When prompted, choose "From GitHub" and then paste in the URL to today's starter code folder from your fork of the class repository.

You will be submitting the URL to this working sandbox as part of your assignment.


## Practice - Complete and Optimize the `<Login />` and `<Auth />` components
You have been provided, in the `starter-code/practice` folder, a working application using the `<Login />` and `<Auth />` components built during class.

**Assignment: Refactor the application to use functional components and multiple pages**
* You will notice that the login system is fundamentally broken
  * What doesn't work?
  * Why?
  * ... Fix It before you move on
* Convert both the `<Login />` and `<Auth />` components to be implemented as 'function' components instead of 'class' components
  * Which hook will you use?
* Add a menu/nav to the `<App />` with links to 2 routes: `/` and `/content` along with the `<Login />`
* Replace the `<EditLink />` and `<DeleteLink />` components with `<Route>s` that will show the appropriate content (below)
* Add 2 "pages" (implemented as functional components) to the application
  * `<Home />` should respond to the `/` route
    * This should always show "Hello World" as an `<h1>`
  * `<Content />` should respond to the `/content` route
    * The link to this page should be hidden if you're not logged in
    * When visible, this component should render 3 divs conditionally:
      * One if you're logged in, which says "You are logged in"
      * One if you're logged in and have edit permissions, which says "You can edit"
      * One if you're logged in and have delete permissions, which says "You can delete"

### Testing
* Write unit tests for the Login Context Component
* Write unit tests for the Login/Auth components
  * Hide/Show based on status
* You will need to create some mocking interface to fake a server/login to simulate.

## To Do Application Refactor
You have been provided, in the `starter-code/todo` folder, a working To Do list application, written using standard React Component State

**Assignment: Implement Login and Authorization into an existing application**

### Requirements
* Hide the entire interface until the user has logged in.
  * Provide a login and logout option in the header of the app
* Implement the following RBAC rules:
    * Logged In Users with 'read' permissions can see the summary/count
    * Logged In Users with 'read' permissions can see the list of To Do Items
    * Logged In Users with 'delete' permissions can click the records to mark them as complete
    * Logged In Users with 'update' permissions can edit existing items
    * Logged In Users with 'create' permissions can create new items

### Notes
* You may use the working login/auth component system from your practice assignment
* You may not alter the functionality of the existing application
* You may only grant access using RBAC
* You must test/implement with a live API server
  * Use .env in your React app to configure it's connection
* You may use your own API Server, which support login and auth or you may use the official API deployment at https://api-js401.herokuapp.com
  * Note: The deployed API server has the following user accounts (username:password) that you can use to login as a user with varying permissions
    * admin:ADMIN (create, read, update, delete)
    * editor:EDITOR (create, read, update)
    * user:USER (read)

### Testing
* Write a suite of UI tests that assert the existence of components based on user login state. This is an assertion of wiring, not logic.
* Your previous Login/Auth tests are going to be sufficient for the core functionality

### Assignemnt Submission Instructions
Refer to the the [lab submission instructions](../../../reference/submission-instructions/labs/README.md) for the complete lab submission process and expectations

----------

remote: Create a pull request for 'submission' on GitHub by visiting:
remote:      https://github.com/401-advanced-javascript-kimball/l34-todo-login-and-auth/pull/new/submission
remote:
To github.com:401-advanced-javascript-kimball/l34-todo-login-and-auth.git
 * [new branch]      submission -> submission
Submission Link:
https://github.com/401-advanced-javascript-kimball/l34-todo-login-and-auth/blob/submission/README.md
