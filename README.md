# Deployment-Slots
Azure Deployment slots

Azure Deployment slot is a very useful feature of the Azure App Service. Azure deployment slots let us deploy different versions of our web app to different URLs by creating one or more deployment slots. And special thing is, we can swap these deployment slots without causing any downtime for end users. 

![image](https://user-images.githubusercontent.com/58148717/104237021-0cc5b380-541d-11eb-8ae3-74d2af12f3b4.png)

Few cool features of Azure deployment slots.

Staging the environments
When we create our first deployment slot in our app service after we deployed our app in Azure App Service, it’s called staging. Then this is a slot where we use to deploy our new version of the app.

![image](https://user-images.githubusercontent.com/58148717/104237218-5b734d80-541d-11eb-944f-d2540bef8c36.png)

After check the new version of the app we can swap it with our production slot.

Multi versions of the same app.

With deployment slots, we can maintain multi-version of the same app. It is a very important feature. Because we can maintain our multi versions of the same app with different slots and then we can check changes of each version with different deployment slots. And also we can set up configurations for each slot.

![image](https://user-images.githubusercontent.com/58148717/104237370-91183680-541d-11eb-8edf-03cb6ce1560f.png)

Then we can check each version with different configurations. Also Azure will create a specific URL for each slot. Then we can use each URL for each version.

![image](https://user-images.githubusercontent.com/58148717/104237536-d0df1e00-541d-11eb-9119-f531639d50c1.png)

After we did the swapping, the production slot becomes the staging slot and the staging slot becomes the production slot.

Also if there is any issue then we can roll back our changes by swapping back. This feature is very useful and amazing.

Testing in Production

Testing in production is the general practice of utilizing production traffic to test a new deployment before fully releasing it. Testing in production is essentially Azure’s implementation of a canary test. Basically we do canary testing by releasing a small subset of users to new features from the production. we can do this with the Azure deployment slot. You can see a small column called traffic. We can release a small subset of users (traffic) to our new version from the production.

![image](https://user-images.githubusercontent.com/58148717/104237671-0421ad00-541e-11eb-8f0b-466222b21189.png)

For example, we can release 5% traffic to the new version from the production. Then the production traffic will be 95%. If we don’t notice any issues, we can continue this until we have reached 100%.

Conclusion:

We can do deployment without the downtime. Also, we can test the new version before putting new version to production. Also if something fails on production, we can swap it back easily and can get the last working version to production. So this is a very important and amazing feature to release our web app (production) with a good state.

For more info: https://docs.microsoft.com/en-us/azure/app-service/deploy-staging-slots


















