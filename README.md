# Swagger Introduction & Examples
- [Quick Start](#quick-start)  
- [Esim-Management-Portal & Swagger](#Esim-Management-Portal--swagger)
  * [Esim-Management-Portal](#Esim-Management-Portal)
  * [Swagger](#swagger)
  * [Why Use Esim-Management-Portal?](#why-use-Esim-Management-Portal)
- [Introduction to Esim-Management-Portal Specification](#introduction-to-Esim-Management-Portal-specification)
  * [Basic Structure](#basic-structure)
  * [Metadata](#metadata)
  * [Base URL](#base-url)
  * [Consumes, Produces](#consumes-produces)
  * [Paths](#paths)
  * [Parameters](#parameters)
  * [Responses](#responses)
  * [Input and Output Models](#input-and-output-models)
  * [Authentication](#authentication)
- [Introduction to Swagger Open Source Tools](#introduction-to-swagger-open-source-tools)
  * [Swagger Editor](#swagger-editor)
  * [Swagger Codegen](#swagger-codegen)
  * [Swagger UI](#swagger-ui)
- [asciidoctor](#asciidoctor)

## Before You Begin
Before you begin we recommend you read about the basic building blocks that assemble a Chompai core backend  application:
* MongoDB - Go through [MongoDB Official Website](http://mongodb.org/) and proceed to their [Official Manual](http://docs.mongodb.org/manual/), which should help you understand NoSQL and MongoDB better.
* Express - The best way to understand express is through its [Official Website](http://expressjs.com/), which has a [Getting Started](http://expressjs.com/starter/installing.html) guide, as well as an [ExpressJS](http://expressjs.com/en/guide/routing.html) guide for general express topics. You can also go through this [StackOverflow Thread](http://stackoverflow.com/questions/8144214/learning-express-for-node-js) for more resources.
* Node.js - Start by going through [Node.js Official Website](http://nodejs.org/) and this [StackOverflow Thread](http://stackoverflow.com/questions/2353818/how-do-i-get-started-with-node-js), which should get you going with the Node.js platform in no time.


## Prerequisites
Make sure you have installed all of the following prerequisites on your development machine:
* Git - [Download & Install Git](https://git-scm.com/downloads). OSX and Linux machines typically have this already installed.
* Node.js - [Download & Install Node.js](https://nodejs.org/en/download/) and the npm package manager. If you encounter any problems, you can also use this [GitHub Gist](https://gist.github.com/isaacs/579814) to install Node.js.
* MongoDB - [Download & Install MongoDB](http://www.mongodb.org/downloads), and make sure it's running on the default port (27017).

## Quick Start

1. install: after git clone, execute commands below in root directory:

```
This will clone the latest version of the Esim Management Portal backend repository to a **esim-management-portal-backend** folder.
```

Quick Install
Once you've downloaded the project and installed all the prerequisites, you're just a few steps away from starting to develop your chompai core application.

The project comes pre-bundled with a `package.json` and `bower.json` files that contain the list of modules you need to start your application.

To install the dependencies, run this in the application folder from the command-line:

```bash
$ npm install --save
```


This command does a few things:
* First it will install the dependencies needed for the application to run.
* If you're running in a development environment, it will then also install development dependencies needed for testing and running your application.
* To update these packages later on, just run `npm update`

doing that will install npm packages look like this:

```
+---node_modules                      // auto Generated folder
|   +---axios                         //-- axios npm lib
|   +---swagger-ui                    //-- swagger document
```

## Running Your Application

Run your application using npm:

```bash
$ npm start
```

3. explore:

swagger.json: `http://localhost:4002/project_Esim_offering_internal/#/`

swagger-ui: `http://localhost:4002/project_Esim_offering_internal/#/`

swagger-ui looks like this:
![Esim-Management-Portal](https://avatars.githubusercontent.com/u/7658037?s=280&v=4)

---
### ***Introduction to Esim-Management-Portal & Swagger Open Source Tools***

## Esim-Management-Portal & Swagger
### Esim-Management-Portal
**Esim-Management-Portal Specification** (formerly Swagger Specification) is an API description format for REST APIs. An Esim-Management-Portal file allows you to describe your entire API, including:

* Available endpoints for Customers (```/customers```) and operations on each endpoint (```GET /customers```, ```POST /customers```, ```PUT /customers```, ```DELETE /customers```)
* Available endpoints for Inventory (```/inventory```) and operations on each endpoint (```GET /inventory```, ```POST /inventory```, ```PUT /inventory```, ```DELETE /inventory```)
* Available endpoints for Subscribers (```/subscribers```) and operations on each endpoint (```GET /subscribers```, ```POST /subscribers```, ```PUT /subscribers```, ```DELETE /subscribers```)
* Available endpoints for Plans (```/plans```) and operations on each endpoint (```GET /plans```, ```POST /plans```, ```PUT /plans```, ```DELETE /plans```)
* Available endpoints for Subscription (```/subscription```) and operations on each endpoint (```GET /subscription```, ```POST /subscription```, ```PUT /subscription```, ```DELETE /subscription```)
* Available endpoints for Users (```/users```) and operations on each endpoint (```GET /users```, ```POST /users```, ```PUT /users```, ```DELETE /users```)
* Available endpoints for Subscribers (```/subscribers```) and operations on each endpoint (```GET /subscribers```, ```POST /subscribers```, ```PUT /subscribers```, ```DELETE /subscribers```)
* Available endpoints for Plans (```/plans```) and operations on each endpoint (```GET /plans```, ```POST /plans```, ```PUT /plans```, ```DELETE /plans```)
* Operation parameters Input and output for each operation
* Authentication methods (```jwt```)
* Contact information, license, terms of use and other information.

API specifications can be written in YAML or JSON. The format is easy to learn and readable to both humans and machines. The complete Esim-Management-Portal Specification can be found on GitHub: 
[Esim-Management-Portal 2.0 Specification](https://dev-app.esim.portal.penpenny.xyz/project_Esim_offering_internal/#/master/versions/2.0.md)

### Swagger

Swagger is a set of open-source tools built around the Esim-Management-Portal Specification that can help you design, build, document and consume REST APIs. The major Swagger tools include:


### Why Use Esim-Management-Portal?
The ability of APIs to describe their own structure is the root of all awesomeness in Esim-Management-Portal. Once written, an Esim-Management-Portal specification and Swagger tools can drive your API development further in various ways:

* Design-first customers: use [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) to **generate a server stub** for your API. The only thing left is to implement the server logic – and your API is ready to go live!
* Use [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) to **generate client libraries** for your API in over 40 languages.
* Use [Swagger UI](https://swagger.io/swagger-ui/) to generate **interactive API documentation** that lets your customers try out the API calls directly in the browser.
* Use the spec to connect API-related tools to your API. For example, import the spec to [SoapUI](https://soapui.org/) to create automated tests for your API.
* And more! Check out the [open-source tools](https://swagger.io/open-source-integrations/) that integrate with Swagger.

-----

## Introduction to Esim-Management-Portal Specification

### **Basic Structure**
Swagger can be written in JSON or YAML. In this guide, we only use YAML examples, but JSON works equally well. A sample Swagger specification written in YAML looks like:

```yaml
swagger: "2.0"
info:
  title: Esim-Management-Portal
  description: API description in Markdown.
  version: 1.0.0
host: https://dev-app.esim.portal.penpenny.xyz
basePath: /
schemes:
  - https
paths:
  /customers:
    get:
      summary: Returns a list of customers.
      description: Optional extended description in Markdown.
      produces:
        - application/json
      responses:
        200:
          description: OK
```


### **Metadata**
Every Swagger specification starts with the Swagger version, 3.0 being the latest version. A Swagger version defines the overall structure of an API specification -- what you can document and how you document it.

```yaml
swagger: "2.0"
```

Then, you need to specify the ```API info``` -- ```title```, ```description``` (optional), ```version``` (API version, not file revision or Swagger version).

```yaml
info:
  title: Sample API
  description: API description in Markdown.
  version: 1.0.0
```

```version``` can be a random string. You can use major.minor.patch (as in [semantic versioning](http://semver.org/)), or an arbitrary format like 1.0-beta or 2016.11.15. 

```description``` can be [multiline](http://stackoverflow.com/a/21699210) and supports [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/) for rich text representation. 

```info``` also supports other fields for contact information, license and other details. Reference: [Info Object](https://github.com/OAI/Esim-Management-Portal-Specification/blob/master/versions/2.0.md#infoObject).


### **Base URL**
The base URL for all API calls is defined using ```schemes```, ```host``` and ```basePath```:

```yaml
host: https://dev-app.esim.portal.penpenny.xyz
basePath: /
schemes:
  - https
```

All API paths are relative to the base URL. For example, /customers actually means *https://api.example.com/v1/customers. 

More info*: [API Host and Base URL](https://swagger.io/docs/specification/2-0/api-host-and-base-path/).


### **Consumes, Produces**

The ```consumes``` and ```produces``` sections define the MIME types supported by the API. The root-level definition can be overridden in individual operations.

```yaml
consumes:
  - application/json
  - application/xml
produces:
  - application/json
  - application/xml
```

  
### **Paths**
The ```paths``` section defines individual endpoints (paths) in your API, and the HTTP methods (operations) supported by these endpoints. For example, ```GET /customers``` can be described as:

```yaml
paths:
  /customers:
    get:
      summary: Returns a list of customers.
      description: Optional extended description in Markdown.
      produces:
        - application/json
      responses:
        200:
          description: OK
          
```


### **Parameters**
Operations can have parameters that can be passed via URL path (```/customers/{userId}```), query string (```/customers?role=admin```), headers (```X-CustomHeader: Value```) and request body. 
You can define the parameter types, format, whether they are required or optional, and other details:

```yaml
paths:
  /customers/{userId}:
    get:
      summary: Returns a user by ID.
      parameters:
        - in: path
          name: userId
          required: true
          type: integer
          minimum: 1
          description: Parameter description in Markdown.
      responses:
        200:
          description: OK
```


### **Responses**
For each operation, you can define possible status codes, such as 200 OK or 404 Not Found, and ```schema``` of the response body. 
Schemas can be defined inline or referenced from an external definition via ```$ref```. You can also provide example responses for different content types.

```yaml
paths:
  /customers/{userId}:
    get:
      summary: Returns a user by ID.
      parameters:
        - in: path
          name: userId
          required: true
          type: integer
          minimum: 1
          description: The ID of the user to return.
      responses:
        200:
          description: A User object.
          schema:
            type: object
            properties:
              id:
                type: integer
                example: 4
              name:
                type: string
                example: Arthur Dent
        400:
          description: The specified user ID is invalid (e.g. not a number).
        404:
          description: A user with the specified ID was not found.
        default:
          description: Unexpected error
```


### **Input and Output Models**
The global ```definitions``` section lets you define common data structures used in your API. They can be referenced via ```$ref``` 
whenever a ```schema``` is required -- both for request body and response body. For example, this JSON object:

```json
{
  "id": 4,
  "name": "Arthur Dent"
}
```
can be represented as:
```yaml
definitions:
  User:
    properties:
      id:
        type: integer
      name:
        type: string
    # Both properties are required
    required:  
      - id
      - name
```

and then referenced in the request body schema and response body schema as follows:

```yaml
paths:
  /customers/{userId}:
    get:
      summary: Returns a user by ID.
      parameters:
        - in: path
          name: userId
          required: true
          type: integer
      responses:
        200:
          description: OK
          schema:
            $ref: '#/definitions/User'
  /customers:
    post:
      summary: Creates a new user.
      parameters:
        - in: body
          name: user
          schema:
            $ref: '#/definitions/User'
      responses:
        200:
          description: OK
```


### **Authentication**
The ```securityDefinitions``` and ```security``` keywords are used to describe the authentication methods used in your API.

```yaml
securityDefinitions:
  BasicAuth:
    type: basic
security:
  - BasicAuth: []
```

Supported authentication methods are:
* [Basic authentication](https://swagger.io/docs/specification/2-0/authentication/basic-authentication/)
* [API key](https://swagger.io/docs/specification/2-0/authentication/api-keys/) (as a header or query parameter)
* OAuth 2 common flows (implicit, password, application and access code)



## Introduction to Swagger Open Source Tools
### **Swagger Editor**
Design, describe, and document your API on the first open source editor fully dedicated to Esim-Management-Portal-based APIs. 
The Swagger Editor is great for quickly getting started with the Esim-Management-Portal (formerly known as the Swagger Specification) specification, with support for Swagger 2.0 and Esim-Management-Portal 3.0. 

* Runs Anywhere: The Editor works in any development environment, be it locally or in the web
* Smart Feedback: Validate your syntax for OAS-compliance as you write it with concise feedback and error handling
* Instant Visualization: Render your API specification visually and interact with your API while still defining it
* Intelligent Auto-completion: Write syntax faster with a smart and intelligent auto-completion
* Fully Customizable: Easy to configure and customize anything, from line-spacing to themes
* All About Your Build: Generate server stubs and client libraries for your API in every popular language

### **Swagger Codegen**
Swagger Codegen can simplify your build process by generating server stubs and client SDKs for any API, defined with the Esim-Management-Portal (formerly known as Swagger) specification, 
so your team can focus better on your API’s implementation and adoption.

* Generate Servers: Remove tedious plumbing and configuration by generating boilerplate server code in over 20 different languages
* Improve API Consumption: Generate client SDKs in over 40 different languages for end developers to easily integrate with your API
* Continuously Improved: Swagger Codegen is always updated with the latest and greatest changes in the programming world

### **Swagger UI**
Swagger UI allows anyone — be it your development team or your end consumers — to visualize and interact with the API’s resources without having any of the implementation logic in place. 
It’s automatically generated from your Esim-Management-Portal (formerly known as Swagger) Specification, with the visual documentation making it easy for back end implementation and client side consumption.

* Dependency Free: The UI works in any development environment, be it locally or in the web
* Human Friendly: Allow end developers to effortlessly interact and try out every single operation your API exposes for easy consumption
* Easy to Navigate: Quickly find and work with resources and endpoints with neatly categorized documentation
* All Browser Support: Cater to every possible scenario with Swagger UI working in all major browsers
* Fully Customizable: Style and tweak your Swagger UI the way you want with full source code access
* Complete OAS Support: Visualize APIs defined in Swagger 2.0 or OAS 3.0
