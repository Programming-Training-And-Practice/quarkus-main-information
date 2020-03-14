# Quarkus Main Information.





## Contents at a Glance.
* [About.](#about)
* [Documentation.](#documentation)
* [Maven Commands.](#maven-commands)
* [Build a native executable.](#building-a-native-executable)
* [Articles.](#articles)
* [Conferences.](#conferences)
* [Conference Speakers.](#conference-speakers)
* [Help.](#help)





## About.





## Documentation.
* [Quarkus.](https://quarkus.io/)
* [QUTE REFERENCE GUIDE](https://quarkus.io/guides/qute-reference)
* [Hot Reload.]()
* [Reactive Programming Style.]()
* [DEPLOYING ON KUBERNETES AND OPENSHIFT](https://quarkus.io/guides/deploying-to-kubernetes)
* [EXTENSIONS.](https://quarkus.io/extensions/)
* [Platform Dependent Application.]()
 




## Maven Commands.
* `mvn io.quarkus:quarkus-maven-plugin:create`
* `mvn quarkus:dev` Running the application in dev mode.
* `mvn compile quarkus:dev` Compile the application in dev mode.
* `mvn quarkus:list-extensions` Show list of extensions.
* `mvn quarkus:add-extension -Dextensions="groupId:artifactId"` Adding extension.
* `mvn quarkus:add-extension -Dextensions="hibernate-*"` You can install all extensions which match a globbing pattern.
* `mvn package` For packaging application. Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/lib` directory.
* `mvn package -Pnative` Compilation into native code.
* `mvn verify -Pnative`
* `mvn verify -Pnative -Dquarkus.test.native-image-profile=test`
* `mvn failsafe:integration-test`
* `mvn package -Pnative -Dquarkus.native.container-build=true` You can use Docker to build the native executable.
* `mvn quarkus-bootstrap:build-tree` Displays the build dependency tree for the application.
* `mvn package -Pnative -Dquarkus.native.container-build=true` Support only JDK8
* `mvnw package -Pnative -Dquarkus.native.container-runtime=docker`
* `mvnw package -Pnative -Dquarkus.native.container-runtime=podman`





## Building a native executable.
* The native executable for our application will contain the application code, required libraries, Java APIs, and a 
  reduced version of a VM. The smaller VM base improves the startup time of the application and produces a minimal disk footprint.
* [Building a native executable.](https://quarkus.io/guides/building-native-image)
* [TIPS FOR WRITING NATIVE APPLICATIONS](https://quarkus.io/guides/writing-native-applications-tips)





## Preparation environment to build native executable.
* `sudo update-alternatives --install /usr/bin/java java /path/.../bin/java 13`
* `sudo update-alternatives --install /usr/bin/javac javac /path/.../bin/javac 13`
* `sudo update-alternatives --install /usr/bin/javadoc javadoc /path/.../bin/javadoc 13`.<br/><br/>
* `sudo update-alternatives --config java`
* `sudo update-alternatives --config javac`
* `java -version`
* `javac -version`.<br/><br/>
* `export JAVA_HOME=/pathToMainFolder`
* `echo $JAVA_HOME`
* `export PATH=$JAVA_HOME/bin:$PATH`.<br/><br/>
* `export GRAALVM_HOME=/pathToMainFolder`
* `echo $GRAALVM_HOME`
* `export PATH=$GRAALVM_HOME/bin:$PATH`.<br/><br/>
* `source /home/trl/.profile`.<br/><br/>
* `$GRAALVM_HOME/bin/gu install --file native-image-installable-svm-svmee-java11-linux-amd64-20.0.0.jar`<br/><br/>

* Or add a line "GRAALVM_HOME=$JAVA_HOME" in a file with a name ".profile". This file is in the home directory. 
  And when you change "JAVA_HOME", the "GRAALVM_HOME" will change.





## Articles.
* [Quarkus — новый взгляд на Cloud Native Java. Russian Version.](https://habr.com/ru/company/piter/blog/482968/)





## Conferences.
* [Secure your Quarkus Applications by Sebastien Blanc.](https://www.youtube.com/watch?v=tWHdkpVagXA)




## Conference Speakers.





## Help.
