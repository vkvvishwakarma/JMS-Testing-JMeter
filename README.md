# JMS-Testing-JMeter

JMS Testing with JMeter
This repository contains a guide for testing Java Message Service (JMS) with JMeter. JMS is a messaging standard used for reliable and asynchronous messaging in enterprise systems, while JMeter is an open-source tool used for load testing and functional testing of web applications.

Getting Started
To test JMS with JMeter, you first need to set up a JMS test environment. This involves installing a JMS provider, creating a JMS queue or topic, and writing a JMS producer and consumer. Developer will provide the details for testing.
Ask developer to provide following details in order to configured in Jmeter for testing
1. QueueConnectionFactory
2. JNDI Name Request Queue: eg: "com.tibco.tiobjms.namingInitialContextFactory"
3. JNDI properties
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

1. Create a new test plan in JMeter.
2. Add user defined variable to the test plan
3. Http cookie manager to the test plan
4. Http cache manager to the test plan
5. Add a thread group to the test plan.
6. Configure a JMS Point-to-Point Sampler for sending messages and a JMS Subscriber Sampler for receiving messages. 
7. Add a View Results Tree Listener to the test plan to view the results of the JMeter JMS test. 
8. Refer to the "Viewing Results with View Results Tree Listener" section of the guide for more details.

By following these steps, you can test your JMS implementation using JMeter and validate its performance and reliability.

