Spring Hibernate Example
=========================

This is the sample, fully configured Spring Hibernate based working application for task tracking purpose.


How to Use?
============
1. Git clone this repository.

2. Import into eclipse.

3. Right click -> Run As -> Maven build... -> jetty:run

4. Head over to 127.0.0.1:8080, You should get the welcome page.

5. You can also visit 127.0.0.1:8080/greeting.html - You should get the Hello World! message.

6. To add a new transient task, point your browser to 127.0.0.1:8080/tasks.html and you should get a form to add a new task!
    * This task is not persisted anywehere. This example is used just to demonstrate the spring mvc without JPA persisnce.

8. To add a task that needs to be persisted, visit 127.0.0.1:8080/tasks/persistence.html. This will actually add a task into your DB and returns you the Id of the same.
    * If you come across any issue, check if your DB is properly configured as expected. Read the DB Configuration section next for more details.


DB Configuration:
=================
1. Make sure mysql is running on port 3306. If not run, 
    * _sudo service mysql start_

2. Make sure you are able to login using username=root, and password=password.

3. Create an empty DB instance by running, 
    * _create database taskTracker;_


Changing default DB configuration parameters:
=============================================
If you want to configure the DB specific parameters, you can update the jpaContext.xml file located under src/main/resources. You can modify the same by changing the values of the parameters configured for datasource bean. The parameters that can be modified include:

1. The DB location - update the url property.

2. The DB instance Name - update the url property.

3. Username - update the username property.

4. Password - update the password property.



