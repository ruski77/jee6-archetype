A simple Servlet 3.0 Java project running on Tomcat 7.

To build and run locally

 mvn clean package tomcat7:run

To build and deploy to AWS

1. upload and create application

    mvn package beanstalk:upload-source-bundle beanstalk:create-application-version beanstalk:create-environment

2. upload and update application (incurs downtime)

    mvn package beanstalk:upload-source-bundle beanstalk:create-application-version beanstalk:update-environment

3. upload and update application (zero downtime)

    mvn package beanstalk:upload-source-bundle beanstalk:create-application-version beanstalk:replace-environment