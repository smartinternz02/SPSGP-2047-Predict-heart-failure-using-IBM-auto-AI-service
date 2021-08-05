# INSURANCE-PREMIUM PREDICTION

![image](https://user-images.githubusercontent.com/66083579/127749094-52cc501d-cdb1-4c57-8d33-ec011b8aee62.png)


CATEGORY OF THIS PROJECT :  Artificial Intelligence And  Machine   Learning

Skills Associated With this Project : Python Programming , Data  Pre-processing ,Data  visulaisations using seaborn and matplotlib,
                                       Handling the null  values, working with spyder application in anaconda,
                                        Working with Ibm and Deploying  a Model and getting
                                        Insights from it,  Integrating a model withy NODE-RED , Creating A  U.I(user  interface) using                                              node-red.
                                        
 Description Of the Project: In this project, we  are predicting the insurance claim  of the various people  by taking  certain  inputs  
                               like  no  of childrens in their family, age , sex , smoking  habit , body mass index  and  to  which part
                               of  the  country he  belongs to  based  on these  inputs  we  are  going to  calculate the total
                                insurance  premium of that  particular person . 
                                
  Solution : 
                So, In this project,  by taking the inputs   like no  of childrens in their family, age , sex , smoking  habit , body mass                      index  and  to  which part of  the  country he  belongs to   our  auto  ai  model  is going  to  predict  the                          insurance  p-remium  value  by taking  this  inputs .  we  will train  the  model  and  get  the  insights  from  it  and                   integrate    with  the  node  read  application   as  a   user interface  where  any person   can  check  his insurance
                 premium value  based  on the  inputs  thta he had  given  to  the  model  for  prediction  of  results.
                 
                 
  STEPS  INVOLVED  IN THIS  PROJECT :
  
  PROJECT OBJECTIVES :
  
      After completing this project, you will learn how to 
      Work with Watson Studio
      Create a project in Watson Studio
      Use Auto Ai experiment to create a model
      Deploy the ML model as a webserver
      Integrating Model and Node-RED Service
      Build an Application using Node-RED which takes inputs from the user and showcases the prediction on UI
      
PROJECT FLOW: 
  This is the project flow to complete the project
  Log in to IBM account
  Create IBM Watson Studio and Node-RED Service
  Create a Watson studio project
  ADD Auto AI Experiment 
   Run the Auto AI Experiment to build a Machine learning model on the desired dataset
   Save the model 
   Deploy the model as a web server and generate scoring End Point
   
   
 TECHNICAL  ARCHITECTURE:
   ![image](https://user-images.githubusercontent.com/66083579/127749752-12ccfc02-cbe0-4261-b443-c25cd7fc682f.png)
   
   
  1. Create an IBM Cloud API key
To use the Watson Machine Learning service programmatically we'll need an API key. Even though this isn't used until later on, let's create one now.
![image](https://user-images.githubusercontent.com/66083579/127749813-167cd2e0-d9da-43ed-9753-a2832832015b.png)


Give it a name and description, hit OK. Write down the API key somewhere.

![image](https://user-images.githubusercontent.com/66083579/127749832-134de062-6775-400b-81a3-321d5afdb001.png)



2. Create a new Cloud Pak for Data project
Log into IBM's Cloud Pak for Data service (formally known as Watson Studio). Once in, you'll land on the dashboard.

Create a new project by clicking Create a project.

![image](https://user-images.githubusercontent.com/66083579/127749840-7accdb41-f9bf-45ab-86f7-c3fcd9f9788f.png)


Choose an Empty project.

![image](https://user-images.githubusercontent.com/66083579/127749872-b353ec17-5edd-47cf-a6ee-900ad80fe9fe.png)


Enter a Name and associate the project with a Cloud Object Storage service.


![image](https://user-images.githubusercontent.com/66083579/127749879-5c4f4e35-ac7f-4078-8461-cb0ee0d4ec6f.png)


NOTE: By creating a project in Watson Studio a free tier Object Storage service will be created in your IBM Cloud account. Select the Free storage type to avoid fees.

At the project dashboard click on the Assets tab and upload the data set associated with this repo. Insurance.csv


SAMPLE  DATA  DROM THE  DATASET:  

![insurance data](https://user-images.githubusercontent.com/66083579/127750024-035a7238-c498-48b0-9c24-53bdc2d2aab9.JPG)


3. Build a model with AutoAI
Now we're going to build a model from the data using IBM's AutoAI. A tool that will automatically create multiple models and test them, giving us the best result. Data science made easy!

Start by clicking on Add to project and choosing AutoAI experiment.


![image](https://user-images.githubusercontent.com/66083579/127750041-7f031407-ed2b-4b50-bf1f-add3533c616f.png)

Give it a Name and specify a Watson Machine Learning instance.

Choose to use data from your project.

Choose the Insurance.csv option.


For the "What do you want to predict?" option, choose Insurance Premium.


The experiment will take a few minutes to run. Once completed hover over the top option to make the Save as button appear. Click it.

![image](https://user-images.githubusercontent.com/66083579/127750077-8df22bd2-3571-44d4-8c7e-e90ecb7167b3.png)


Choose to save the experiment as a Model. You can optionally download a generated Jupyter Notebook that can be used to re-create the steps that were taken to create the model.


You model will be saved. Click the dialog to view it in your project.

![image](https://user-images.githubusercontent.com/66083579/127750113-ea8fca1f-c27c-48b2-a6fb-a0cd417edf1e.png)


Once you're at the model overview choose the button Promote to deployment space
![image](https://user-images.githubusercontent.com/66083579/127750129-d4c21a8e-4c0a-4ff2-a059-677b59a14ee7.png)

4. Deploy the model with WML
To promote the model to deployment you must specify a deployment space. If no space is created choose the New space + option to create one. This action will associate the model with the space.

![image](https://user-images.githubusercontent.com/66083579/127750145-0ab42362-ef66-4cee-8bbb-f4f139ee8594.png)


Navigate to the space using the hamburger menu (☰) on the top right and choose to View all spaces.


Click on the space you saved the model to.

Choose the deploy the model by clicking the rocket ship icon.

Choose the Online deployment option and give it a name.
Your new deployment will appear.


Click on the API reference tab and save the Endpoint. We'll be using this in our application.

![image](https://user-images.githubusercontent.com/66083579/127750195-9bc7ac15-017b-49b4-bfe9-ce8f26f82a86.png)


5. Run the Node.js application
You can deploy this application as a Cloud Foundry application to IBM Cloud by simply clicking the button below. This option will create a deployment pipeline, complete with a hosted Git lab project and devops toolchain.


You may be prompted for an IBM Cloud API Key during this process. Use the Create (+) button to auto-fill this field and the others. Click on the Deploy button to deploy the application.

Before using the application go to the Runtime section of the application and in the Environment variables tab add in your API_KEY and DEPLOYMENT_URL values from steps 1 and 4.

TIP Do NOT wrap these values with double quotes.

Once updated your application will restart and you can visit the application by clicking on Visit App URL.


![image](https://user-images.githubusercontent.com/66083579/127750227-2d1dea04-e849-4cde-af0c-0de560ebaa36.png)

The app is fairly self-explantory, simply fill in the data you want to score and click on the Classify button to test how those figures would score against our model. The model predicts the  insurance  premium.

NODE-RED  WORKING AREA  AND   VARIOUS  PIPELINES  IN IT  FOR  UI BUILDING :

![node red](https://user-images.githubusercontent.com/66083579/127750373-9d501ee3-ed1c-4ffa-b4b1-382b0c377445.JPG)


After  integrating the  ML  model  with  NODE-RED  the  USER INTERFACE(U.I)  LOOKS  LIKE: 

![ui](https://user-images.githubusercontent.com/66083579/127750408-37d56da9-ba1b-445e-a180-574f376e0012.JPG)






  -------------------THANK  YOU ------------------------------------------
