jdk7-ssl-patch
=======

A patch to SslEngine in open jdk 7 to reduce memory usage

Compile
-----
mvn clean package

Install
-----

You need to copy jar file into endorsed dir of JRE:

      ENDORSED=$JAVA_HOME/jre/lib/endorsed
      sudo mkdir -p $ENDORSED
      sudo cp target/jdk7-ssl-patch-0.1.ar $ENDORSED

      # for mac, change $ENDORSED to
      ENDORSED=/Library/Java/Home/lib/endorsed

      # for tomcat, change $ENDORSED to
      ENDORSED=$CATALINA_HOME/endorsed
