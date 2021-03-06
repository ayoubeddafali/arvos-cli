Arvos Utility Tool
=====================

CLI tool for running arvos.

Requirements
--------------------------

1. Python >= 3.9 and pip installed
2. Docker installed
3. Debugfs mounted ( sudo mount -t debugfs debugfs /sys/kernel/debug )


How to install
------------------

::

    $ pip install arvos


Usage
------

The following command will build an application image ( based on jdk 17 ) from the specified jar, run it, and run the tracer app for a period of 2 minutes.

::

    $ arvos scan --jar target/application.jar --trace-period 2 --pom pom.xml

Or  ( This will generate a .pdf report of the found vunlerable )

:: 

    $ arvos scan --jar target/java-app-0.0.1-SNAPSHOT.jar --trace-period 2 --save-report


If you do not have a ready Java 17 based application, you can use the following sample application: https://github.com/ayoubeddafali/spring-vulnerable-app. 

The .jar file can be downloaded from : https://github.com/ayoubeddafali/spring-vulnerable-app/releases/download/0.0.1-snapshot/java-app-0.0.1-SNAPSHOT.jar


Supported platforms
---------------------

Only Linux is supported.








