jdk7-ssl-patch
=======

A patch to SslEngine in Open JDK 7u5 to reduce memory usage

Compile
-----
mvn clean package

Install
-----

You need to copy jar file into endorsed dir of JRE:

      ENDORSED=$JAVA_HOME/jre/lib/endorsed
      sudo mkdir -p $ENDORSED
      sudo cp target/jdk7-ssl-patch-0.1.jar $ENDORSED

      # for mac, change $ENDORSED to
      ENDORSED=/Library/Java/Home/lib/endorsed

      # for tomcat, change $ENDORSED to
      ENDORSED=$CATALINA_HOME/endorsed

Version
-----
original openjdk source version is `openjdk-7u6-fcs-src-b24-28_aug_2012`. we
use this patch with Oracle JDK 1.7.0_07-b10 in production for months. and do
not see any significant problem.

The patch could not be compiled with latest JDK 7, however.
