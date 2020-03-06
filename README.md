# Quarkus Main Information.





## Contents at a Glance.
* [About.](#about)
* [Documentation.](#documentation)
* [Maven Commands.](#maven-commands)
* [Build a native executable.](#building-a-native-executable)
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
* `mvn quarkus:dev` Running the application in dev mode.
* `mvn compile quarkus:dev` Compile the application in dev mode.
* `mvn quarkus:list-extensions` Show list of extensions.
* `mvn quarkus:add-extension -Dextensions="groupId:artifactId"` Adding extension.
* `mvn package` For packaging application. Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/lib` directory.
* `mvn package -Pnative -Dquarkus.native.container-build=true` You can use Docker to build the native executable.
* `mvn package -Pnative` Compilation into native code.





## Building a native executable.
* [Building a native executable.](https://quarkus.io/guides/building-native-image)





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
* `$GRAALVM_HOME/bin/gu install --file native-image-installable-svm-svmee-java11-linux-amd64-20.0.0.jar`





## Help.
