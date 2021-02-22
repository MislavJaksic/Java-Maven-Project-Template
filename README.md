## Java Maven Project Template

[Maven Tutorial](https://github.com/MislavJaksic/Maven-Tutorial)

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

```
$: java "-DJAR_CLI=Run-Value" -jar target/template-0.0.1.jar  # run-time config
```

### target

```
$: mvn clean
$: mvn compile
```

```
$: mvn package "-DAPP_CLI_DEFINED=Build-Value"  # build-time config
$: mvn install "-DAPP_CLI_DEFINED=Build-Value"  # install to a local .m2 repository
```

#### site

```
$: mvn site

# Note: see the HTML project report in `target/site/index.html`
```

#### site/apidocs

```
$: mvn javadoc:javadoc

# Note: see Javadocs in target/site/apidocs/index.html
```

#### site/jacoco

```
$: mvn jacoco:prepare-agent test jacoco:report

# Note see test coverage report in `target/site/jacoco/index.html`
```

#### surefire-reports and site

```
$: mvn test surefire-report:report

# Note: see the XML test reports in `target/surefire-reports/TEST-**.xml`
# Note: see the HTML test reports in `target/site/surefire-report.html`
```

### Checks

```
$: mvn checkstyle:check  # check style
$: mvn pmd:check  # static code analysis
```
