# JMS-Testing-JMeter

JMS Testing with JMeter
This repository contains a guide for testing Java Message Service (JMS) with JMeter. JMS is a messaging standard used for reliable and asynchronous messaging in enterprise systems, while JMeter is an open-source tool used for load testing and functional testing of web applications.

Getting Started
To test JMS with JMeter, you first need to set up a JMS test environment. This involves installing a JMS provider, creating a JMS queue or topic, and writing a JMS producer and consumer. Developer will provide the details for testing.

The details for configuring JMeter for testing will be provided by the developer, such as the QueueConnectionFactory, JNDI Name Request Queue, JNDI properties, URL, body, username, and password. For more details find as below:

1. QueueConnectionFactory
2. JNDI Name Request Queue: eg: "com.tibco.tiobjms.namingInitialContextFactory"
3. Configured following in JNDI properties:
   1. java.naming.security.principle = userName
   2. java.naming.security.credential= password
   3. optional: if connection does not get stablish then configured following JNDI properties
      1. com.tibco.tibjms.naing.security_protocol=ssl
      2. com.tibco.tibjms.naming.ssl_vendor=j2se-default
      3. com.tibco.tibjms.naming.ssl_enable_verify_host = false
5. URL : eg:"ssl://ttibaassmp.abcduat.com:45690
6. Body: eg: "xml body
7. userName
8. password


To perform JMS testing with JMeter, follow these steps:

Set up the JMS test environment by installing a JMS provider, creating a JMS queue or topic, and writing a JMS producer and consumer. Refer to the "Setting up JMS Test Environment".
1. Start JMeter using jmeter.bat

Eg:- Thread Group-ComponentUpdate

Set Number of Threads (users): 5
Ramp-Up Period (in seconds): 1
1. Create a new test plan in JMeter.
2. Right click on Test Plan -> Add -> user defined variable to the test plan
3. Right click on Test Plan -> Add -> Http cookie manager to the test plan
4. Right click on Test Plan -> Add -> Http cache manager to the test plan
5. Add a thread group to the test plan.
6. Right click on Test Plan -> Add -> Threads(Users) -> Thread Group. Rename this Thread Group.
7. Configure a JMS Point-to-Point Sampler for sending messages and a JMS Subscriber Sampler for receiving messages. 
8. Add a View Results Tree Listener to the test plan to view the results of the JMeter JMS test. 
9. Refer to the "Viewing Results with View Results Tree Listener" section.

By following these steps, you can test your JMS implementation using JMeter and validate its performance and reliability.

