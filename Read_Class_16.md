# Serverless

### What is Serverless?

Serverless is a cloud application development and execution model that lets developers build and run code without managing servers, and without paying for idle cloud infrastructure.

 'Serverless' describes the developer’s experience with those servers—they are are invisible to the developer, who doesn't see them, manage them, or interact with them in any way.
 
 ### Examples for Serverless Services
 
 Amazon Web Services (AWS Lambda), Microsoft Azure (Azure Functions), Google Cloud (Google Cloud Functions) and IBM Cloud (IBM Cloud Code Engine). 



### What is the uses for serverless  

- Serverless and microservices: The most common use case of serverless today is supporting microservices architectures. The microservices model is focused on creating small services that do a single job and communicate with one another using APIs. 
- API backends: Any action (or function) in a serverless platform can be turned into a HTTP endpoint ready to be consumed by web clients. When enabled for web, these actions are called web actions. Once you have web actions, you can assemble them into a full-featured API with an API gateway 
- Data processing: Serverless is well-suited to working with structured text, audio, image, and video data, around tasks such as data enrichment, transformation, validation, cleansing


### Attributes of serverless

- Small, discrete units of code. Often services written using serverless architecture are comprised of a single function.

- Event-based execution. The infrastructure needed to run a function doesn't exist until a function is triggered. Once an event is received an ephemeral compute environment is created to execute that request. The environment may be destroyed immediately, or more commonly stays active for a short period of time, commonly 5 minutes.

- Scale to zero. Once a function stops receiving requests the infrastructure is taken down and completely stops running. This saves on cost since the infrastructure only runs when there is usage. If there's no usage, the environment scales down to zero.

- Scale to infinity. The FaaS takes care of monitoring load and creating additional instances when needed, in theory, up to infinity. This virtually eliminates the need for developers to think about scale as they design applications. A single deployed function can handle one or one billion requests without any change to the code.

- Use of managed services. Often serverless architectures make use of cloud provided services for elements of their application that provide non-differentiated heavy lifting such as file storage, databases, queueing, etc. For example, Google's Firebase is popular in the serverless community as a database and state management service that connects to other Google services like Cloud Functions.




## Things I want to know more about

i want to know how to use it, what is the best uses for it and when should i use it.

also training and do a real expamle using it and how i can use it in my projects 
