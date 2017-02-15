# Breaking the Monolith by using hapi 
## Background
Let me get the disclaimer out of the way: I am not an expert on Hapi
I started looking into Hapi's ability to break components out.
This is my attempt to follow other tutorials from a hello world to a true component system.
I have broken this down into the following steps

| Project  | Description | Link |
|---|---|---|
|**hapi-tut-monolith-01**|A simple hello world hapi project| [https://github.com/quapaw/hapi-tut-monolith-01](github)|
|hapi-tut-monolith-02a|Add services - customers and products| [https://github.com/quapaw/hapi-tut-monolith-02a](github)|
|hapi-tut-monolith-02b|Adding Glue and externalizing config| [https://github.com/quapaw/hapi-tut-monolith-02b](github)|
|hapi-tut-monolith-02c|Moving services into their own folders| [https://github.com/quapaw/hapi-tut-monolith-02c](github)|
|hapi-tut-monolith-03-main|Moved service into own project.  This pulls the services in| [https://github.com/quapaw/hapi-tut-monolith-03-master](github)|
|hapi-tut-monolith-03-customer|Just the customer service| [https://github.com/quapaw/hapi-tut-monolith-03-customers](github)|
|hapi-tut-monolith-03-products|Just the produce service| _[https://github.com/quapaw/hapi-tut-monolith-03-products](github)|_

#HAPI Tutorial - Monolith - 1
## Simple Hello World
This is a simple hello world tutorial. 
I used this [Tutorial](https://hapijs.com/tutorials/getting-started?lang=en_US) for the pattern.  
Please go and follow it to create you hello world.  You can look back at this as a reference.

Items I added
* npm [shrinkwrap](https://docs.npmjs.com/cli/shrinkwrap)
~ A major problem with some of the tutorials I found is that the examples are outdated.<br/>
~ Shrinkwrap will capture all the versions of all components. <br/>
~ So hopefully you will be able to pull this code years from now and it will compile and work. :) <br/>


Instructions
* Pull the repository
* run ``npm install``
* run ``node index.js`` This should give you a printout ``Server running at: http://localhost:3000``
* Test the general welcome by hitting the following url ( http://localhost:3000) The Browser should return ``Hello, world``
* Test the by passing you first name as a param ( http://localhost:3000/Scott ) Change Scott to your first name.