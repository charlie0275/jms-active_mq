Reference : http://www.pretechsol.com/2013/08/jms-with-activemq-example.html
JMS with ActiveMQ

#. download ActiveMQ

#. 啟動 ActiveMQ
   $ cd <ActiveMQ_HOME>/bin/macosx
   $ . activemq start

#. Open ActiveMQ Console :  http://localhost:8161/admin (admin-admin)

￼

#. Create a JMS project

   1. add jars to project
   操作：click project > properties > Java Build Path > Add External JARs
   choose : j2ee.jar, choose <ActiveMQ_HOME>/lib/*.jar

   2. new MessageProducerExample.java
      new MessageConsumerExample.java

#. Send Message I
   
   操作：Run as MessageProducerExample.java
   Open Browser : http://localhost:8161/admin/queues.jsp
￼ 
   操作：Run as MessageConsumerExample.java
   See sts console : Text Message is Helloworld
  
#. Send Message II

   Open Browser : http://localhost:8161/admin/queues.jsp
   操作：
   1. create Queue : testQ
￼

   2. click “Send To”
￼

   3. input some message into Message body and Send
￼

   4. Run as MessageConsumerExample.java
      See sts console : Text Message is I am Charlie.


#. shutdown ActiveMQ
   $ cd <ActiveMQ_HOME>/bin/macosx
   $ . activemq stop


