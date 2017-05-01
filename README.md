## Java EE 7 Tutorial: Java Message Service (JMS) API

[Java Platform, Enterprise Edition: The Java EE Tutorial. Oracle](https://docs.oracle.com/javaee/7/tutorial/) - web version

[The Java EE Tutorial. Oracle](https://docs.oracle.com/javaee/7/JEETT.pdf) - pdf
___
#### - **websimplemessage**

Web applications can use using managed beans to send messages and to receive messages synchronously

It uses sending and receiving Facelets pages as well as corresponding backing beans. When a user enters a message in the text field of the sending page and clicks a button, the backing bean for the page sends the message to a queue and displays it on the page. When the user goes to the receiving page and clicks another button, the backing bean for that page receives the message synchronously and displays it

![The websimplemessage Application](https://docs.oracle.com/javaee/7/tutorial/img/jeett_dt_035.png)

1. To activate the message flow in a aplication server WildFly it is necessary to start a full instance of the application server with the following command:
   ><HOME_WILDFLY/bin>$ ./standalone.sh -c standalone-full.xml

2. *JMS Connection Factories* and *JMS Destinations* available on the application server can be viewed, created and modified through the administration interface WildFly (Configuration> Subsystems> Messaging - ActiveMQ> default> Queues / Topics).

   For a correct execution it is necessary to create a new Connection Factory with name **"java:/jms/factoriaConexiones"** and connector type "in-vm" in your aplication server from the administration console.

   For a correct execution it is necessary to create a new target queue **"java:/jms/queue/exampleQueue"** in your aplication server from the administration console.