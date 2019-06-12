# Gateway API

This API is implemented in order to integrate front-end with Galaxy through a RestAPI.

## Requirements

- ### Build Project

    - [Java8](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
    - [Gradle](https://gradle.org/)

- ### Deploy Project

    - Application Server(i.e. [Tomcat](http://tomcat.apache.org/))

## Build:

1. Checkout project
2. Open command prompt
3. Navigate to project directory
4. Update the settings in the Java parameters file :
    ```sh
    vi src/main/java/gr/di/uoa/kk/gatewayApi/helpers/GenParameters.java
    ```
5. In the project directory :
    ```sh
    gradle clean
    ```
6. In the project directory :
    ```sh
    gradle war
    ```
7. In the project directory :
    ```sh
    cd build/libs
    ```
8. File .war is in this folder

## Deploy:
1. Install Application Server(i.e. [Tomcat](http://tomcat.apache.org/))
2. Stop Application Server if running(i.e. In [Tomcat](http://tomcat.apache.org/) navigate to root directory and run ```./bin/shutdown.sh ```)
3. Copy .war file in the application folder(i.e. In [Tomcat](http://tomcat.apache.org/) navigate to root directory and copy into webapps directory ```cp path/to/war webapps/ ```)
4. Start Application Server(i.e. In [Tomcat](http://tomcat.apache.org/) navigate to root directory and run ```./bin/startup.sh ```)