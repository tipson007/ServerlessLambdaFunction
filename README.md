# ServerlessLambdaFunction
Let's build a Serverless webpage with Was lambda


# AWS Lambda enables you to run code while not provisioning or managing servers. You pay just for the figure time you consume.
With Lambda, you'll be able to run code for nearly any style of application or backend service - all with zero administration. simply transfer your code and Lambda takes care of everything needed to run and scale your code with high availableness. you'll be able to originated your code to mechanically trigger from alternative AWS services or decision it directly from any net or mobile app.

## sumary

In this project you'll be to create a lambda function from scratch, add a trigger, configure an API gateway request, create an s3 bucket, use the bucket to host a static website, and register a domain name using route 53.
Getting started

# Step 1

Create a function, in getting started you are required to pick any from the 3 options. Author from scratch, Blueprints or Aws Serverless Application Repository.
From this project, you'll be required to create from scratch. On this screen you will be required to name your function, choose your runtime environment (python 3.7 is what I'll be using) or a custom environment. Create a role from template. At the policy template, you want a "simple microservice permission". Then click on create function. This will take some minutes.

## Step 2

Designer
Here, you'll need to understand what can trigger a lambda function. When you scroll down to the bottom of your console page, you'll find the IDE where you can modify your code.
Using visual studio code editor, I will copy my written python code and then paste it in the IDE.
If anything invokes the code, it will respond with my name.
Down on the console, we leave everything as default and then modify the basic settings by adding a description. Below is the memory function whereby you can allocate how much memory is delivered to the function as well as the timeout allocated before the function times out. Then click save.
Configure a trigger
This will Create an API gateway, you'll leave everything as default and Modify the role. The click save.
So, what this has done is that, it has created a new API endpoint.Click on the first API link and you'll be redirected to this page.
Click on action then click on delete method. What you'll do is create a new method and specify a GET request.
Click on the box (use lambda proxy integration) and then find your function. After that click save and a pop up window asks about granting permission to API gateway. Click ok.
Next you'll deploy an API. In the deployment stage make it default and name it. After that, click on GET then click on the link "invoke URL:…." Then you'll be able to see your name as written in the python script.
You'll need to add the API gateway link into your html file as shown in the figure.
What this is doing is when you click it, it will call this function and send a GET request to the API gateway.

## Step 3

Create an S3 bucket
Ensure you have your domain name registered
Ensure your bucket object permission is public
Ensure your bucket name is same as your domain name registered.

Next you'll go to properties and click on static website hosting in order to use this bucket to host your website. Now upload your index.html and error.html files in your S3 bucket and make them public.
click on the index.html file and see how the link redirects you to the webpage. which looks like the figure below.
That's the project done| but if you want to go further, you can hook up Route53 to your bucket. Go to your domain and create a record set for your domain name. when this is linked, DNS takes some few seconds to propagate so don't get upset if the page doesn't load. Just have it on your mind that " its not DNS|it can't be DNS|it was DNS".
Eventually when the webpage load, it will be communicating with API gateway which is talking to Lambda and passing the response back to API gateway, which then passes the response back to the browser.
That's all for this project.

## Languages
Python
Html

## Services
Lambda
API gateway
S3
Route 53

## Tools for visualization
Cloudcraft
