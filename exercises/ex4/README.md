# Exercise 4 - Consume SAP S/4HANA Event via Advanced Event Mesh Topic

In this exercise, we will consume an event on a second broker via a topic using the Try Me! tool that comes with Advanced Event Mesh.  


## Exercise 4.1 Consume events via a topic on a second broker

After completing these steps you will have consumed events via a topic from another broker in the Event Mesh. You will use the Try Me! feature of Advanced Event Mesh for this.

To put this into perspective: AEM provides an intelligent distribution of events throughout the mesh of Event Brokers. This is what you experience here. The event will be made available where ever there is an interested consumer.

1. Go to the cluster manager and select another broker in the mesh.

![Pic 1](/./images/ex4-1.png)   

2. Click Try Me!

![Pic 2](/./images/ex4-2.png)   

3. In the Subscriber section, click on show advanced settings

![Pic 3](/./images/ex4-3.png)   

4. The data in the Establish Connection section should be pre-filled. If not, fill the data in the Establish connection section. You can get this data in the connect part like before. Go to Connect and the Solace Web Messaging section. 

As said, it should be pre-filled for you so typically you just have to click connect.

5. Click on Connect

![Pic 4](/./images/ex4-4.png)  

The icon behind Establish Connection should change from Red to Green.

6. Fill your topic into Subscribe --> Add Topic

Your topic is: s4connect 

![Pic 5](/./images/ex4-5.png)   

7. Click on Subscribe

You should see your topic in Subscribed Topics

![Pic 6](/./images/ex4-6.png)   

8. Wait for the instructor to trigger an event in the S/4HANA system

9. Once an event is triggered, it should appear in the messages section

HINT: remember how your queue buffered events for you? This is not the case here. There is no buffering. Only events triggered while you are listening end up here. A topic works like a radio: you need to have your radio switched on in order to listed to the news.

## Exercise 4.2 Produce and Consume events via a topic 

You might have already noticed that there is not only a Subscriber section in Try Me! There is a Publisher Section as well. If you want to you can try to publish a few events or messages as well. These events go via the brokers.

1. Go to the publisher and connect

![Pic 7](/./images/ex4-7.png)   

2. Enter topic_000 (replace 000 with your user id)

Please do not publish to the topics we had used before in order to not spam the other participants.

![Pic 8](/./images/ex4-8.png)   

3. Add your topic to the Subscriber topic - add the topic into the Add Topic field and click Subscribe

![Pic 9](/./images/ex4-9.png)   

4. Click Publish in the Publisher.

![Pic 10](/./images/ex4-10.png)   

5. You should see your message in the Messages section of the Subscriber

![Pic 11](/./images/ex4-11.png)   

## Summary

You've now seen what a mesh looks like in Advanced Event Mesh. You consumed the events via a topic on an additional broker in the mesh. The forwarding of events has happened automatically based on your interest into the topic.

Continue to - [Exercise 5 - Explore Topic Hierarchies and Wildcards (optional)](../ex5/README.md)
