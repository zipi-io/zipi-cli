# Overview 

This is the commmand line inteface to the Zipi Api manager and faciliates running api definition scripts and commands including:
* create a new api 
* stop an api 
* listing an api 
* changing the configuration of an api 

# Create An Api 

```
   api create api-definition.json
```

Where a simple api definition file is:

```
   {
     name: example,
     endpoint: http://example.com 
     initialVersion: 1.0,
     public : true,
     orgName : test
   }
```
# List Api's 
Once the api's are created we can list available api's with:

```
   zipi-cli list 
```
this will list the available api's

```
ApiName  Status   Published  Version
example  private  false       1.0
```

# Publish and UnPublish an Api 
In a similar mannner api can be published an un-published 

```
   zipi-cli publish example 
```
or naturally 

```
   zipi-cli unpublish example
```
# More Advanced Api Features - Security, Caching, Definitions and Time
Zipi provides an number of advanced features covered in this section including:
* security policies 
* swager, raml definitions
* caching
* time based configuration 

# Zipi Microservices 
The Api manager is often a gateway to microservices to interact with the api manager 

```
  zipi create-microservice exampleService
```  
will create a base microservice. Similarly the there a number of features and plugins of the microservice that can be configured via the json config file. 




