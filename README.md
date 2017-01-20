# mongodb-dev-ubuntu14
A vagrant box pre-configured using ansible for doing MongoDB dev on Ubuntu 14.

Currently setup to let you compile the following MongoDB Drivers:

- C Driver ~/mongo-c-driver
- C++ Driver ~/mongo-cxx-driver
- Java Driver ~/mongo-java-driver

You can build the drivers following the instructions on each driver's website. Please see the notes below for any particular gotchas that might trip you up building the drivers.

MongoDB is also buildable but only up to the 3.2.x releases. After that gcc 5.3.0 is required which would require building gcc from source.

- MongoDB ~/mongo

It will also come configured with these tools:

- MongoDB m
- MongoDB mtools

I am also including a few simple Java projects as quick jumping off points. For now I have one lone app:

- MongoDB Maven Starter ~/mongodb-maven-starter

## Building Notes

The Java Driver will install gradle but when it actually attempts to build the project it will fail since it doesn't know where the JDK is installed. The .bashrc file has been modified  to fix this to let gradle know where the JAVA_HOME path is for the OpenJDK that was installed.
