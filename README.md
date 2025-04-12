# Setup of Basic Gradle Using CLI
```agsl
gradle init
```
The above command will setup a basic gradle project

```agsl
gradlew.bat build
```
The above command can Build your code 

```agsl
gradlew.bat jar
```
The above command creates a JAR file for the project in `build\libs` folder which is executable, you need to setup `MANIFEST` property to identify what is the main class to execute in build.gradle

```grrovy
jar{
    manifest {
        attributes(
                'Main-class' : 'org.example.App'
        )
    }
}
```

```agsl
java -jar app\build\libs\app.jar
```
The above command will run the project with this JAR file 
