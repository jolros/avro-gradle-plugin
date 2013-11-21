avro-gradle-plugin
==================

Gradle Plugin for processing Avro files

Building is done through gradle, deploying is done through maven. It sucks, I know, but it works for now.

Steps:

 * Adjust code
 * Change Avro version in gradle.properties and pom.xml (check all occurrences)
 * gradle clean
 * gradle assemble
 * cp ./build/libs/avro-gradle-plugin-*.jar ./target/
 * mvn -e deploy
 * cp ./build/libs/avro-gradle-plugin-*.jar ./target/
 * mvn -e deploy

Yes, you have to run mvn-deploy twice, because it will upload a shell jar the first time.
