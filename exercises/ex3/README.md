# Exercise 3 - Consume Event in Advanced Event Mesh

In this exercise, we will consume an event from our queue in SAP Integration Suite, advanced event mesh. For that we will use the Queue Consumer HTML/JS application and you will connect against the AEM broker

## Exercise 3.1 Start your Queue Consumer Application and connect to Advanced Event Mesh

After completing these steps you will have connected your Queue Consumer application to Advanced Event Mesh

1. As part of the Getting Started you have downloaded or cloned the basic samples from GitHub. Go to the folder that you have downloaded or cloned to.

2. Go to the folder teched2023-IN261-main

3. Go to the directory tools/AEM Samples/src/basic-samples/QueueConsumer

![Pic 1](/./images/ex3-1.png)

4. Open up the QueueConsumer.html file with an editor (e.g. VisualStudio by right clicking on the file)

5. Go to the line

        // create the consumer, specifying name of the queue
        subscriber = new QueueConsumer('L2W_000');
        
and replace L2W_000 with the name of your queue in Advanced Event Mesh, which should be L2W_*** where *** is your individual number.

![Pic 2](/./images/ex3-2.png)

6. Save the file after you have made the changes.

7. Double click on QueueConsumer.html and open in a browser.

![Pic 3](/./images/ex3-3.png)

8. Go to Advanced Event Mesh

9. Click on Cluster Manager

![Pic 4](/./images/ex3-4.png)

10. Click on the tile for your broker

![Pic 5](/./images/ex3-5.png)

11. Click on Connect

![Pic 6](/./images/ex3-6.png)

12. Expand Solace Web Messaging 

![Pic 7](/./images/ex3-7.png)

13. Copy Username, Password, Message VPN and Secured Web Messaging Host into the respective fields of your Queue Consumer

14. In the Queue Consumer, click Connect. 

![Pic 8](/./images/ex3-8.png)

You should get a success message indicating that the connection has worked.

![Pic 9](/./images/ex3-9.png)

## Exercise 3.2 Consume and explore events in Queue Consumer 

After completing these steps you will have consumed events using the Queue Consumer

1. In order to consume messages from your queue, click on *Consume Messages*. If you would like to stop consuming later on, click *Stop Consuming*.

![Pic 10](/./images/ex3-10.png)

2. In case there were events in your queue, they automatically get consumed.

3. Your instructors will update Business Partners in the SAP S/4HANA system frequently. If everything works, you should now receive the BusinessPartner.changed event in your Queue consumer.

![Pic 11](/./images/ex3-11.png)

HINT: potentially you will receive several events at the same time. These events had been buffered for you in your queue, that had already been subscribed to events while you were seeting up you client app.

4. Leave your browser window open and your consuming app up and running

## Summary

You have now connected your queue consumer to your queue in Advanced Event Mesh and have consumed your first events.

It is important to note that the queue is subscribed to a topic and that events get buffered in the queue until they are picked up.

Please continue with [Exercise 4](../ex4/README.md)




