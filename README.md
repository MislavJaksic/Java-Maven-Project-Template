## Java Maven Project Template

```
# Note: install Java and Maven

$: mvn archetype:generate  # ->
  # Choose a number or apply filter (format: [groupId:]artifactId): 1446:
  #   default
  # Choose org.apache.maven.archetypes:maven-archetype-quickstart version:
  #   8: 1.4
  # Define value for property 'groupId':
  #   mislavj
  # Define value for property 'artifactId':
  #   template
  # Define value for property 'version' 1.0-SNAPSHOT: :
  #   0.0.1
  # Define value for property 'package' template: :
  #   default
```

### target

```
$: mvn clean
$: mvn compile  # compile source
```

#### reports and test-results

```
$: mvn test

TODO
# Note: see the HTML test reports in `build/reports/tests/test/index.html`
# Note: see the XML test reports in `build/reports/test-results/test/TEST-**.xml`
```

```
$: ./gradlew jacocoTestReport

# Note: see the test coverage reports in `build/reports/jacoco/test/html/index.html`
```



test, coverage, mocking, logging, packaging, docs, outside file config

TODO



```
$: ./gradlew tasks  # list tasks
$: ./gradlew properties  # list properties
$: ./gradlew clean build jacocoTestReport javadoc  # do everything
```

### build

```
$: ./gradlew clean
$: ./gradlew build  # compile, test, jar and javadoc all at once
```

```
$: ./gradlew build --scan  # create build scan
  # Do you accept these terms? yes
  # Publishing build scan...
# Note: if you want to view the scan you have to give your email
```

#### docs

```
$: ./gradlew javadoc
```

```
# Note: see Javadocs in `build/docs/javadoc/index.html`
```

#### libs

```
$: ./gradlew jar
```
```
$: jar xf build/libs/java-project-template-0.1.0.jar META-INF/MANIFEST.MF  # extract MANIFEST.MF into META-INF
```

#### reports and test-results

```
$: ./gradlew test

# Note: see the HTML test reports in `build/reports/tests/test/index.html`
# Note: see the XML test reports in `build/reports/test-results/test/TEST-**.xml`
```

```
$: ./gradlew jacocoTestReport

# Note: see the test coverage reports in `build/reports/jacoco/test/html/index.html`
```

### gradle

Home to the Gradle wrapper.  

### src

```
$: ./gradlew run  # runs application { mainClassName } in build.gradle
```

#### main/resources

Change configuration.  

### build.gradle

For project configuration:
* define and apply plugins
* repositories
* dependencies
* tests
* packaging
* executing

### gradlew and gradlew.bat

Gradle wrapper runners.  

### settings.gradle

For build configuration:
* root project
