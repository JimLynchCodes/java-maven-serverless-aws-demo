# Java Maven Serverless AWS Demo

Example of a Java API project!

# Commands

Commands for working with this project.

Note there are two options for each command:

1) Run commands in the terminal command line

2) Run as IDE configuration in an IDE like Eclipse or Jetbrains IDEA.

## Build Project
```bash
mvn build
```

Or create a _Run Configuration_ for "Maven build" using your desired JRE version.


## Run Unit Tests

Tests here are using JUnit library.

```bash
mvn test
```

Or create a _Run Configuration_ for "JUnit run tests" selecting your test directory.

Run unit tests to check that your functions work as expected!

## Run Unit Tests With Code Coverage

Code coverage reports can show you where you are missing tests!

Add this plugin to your pom.xml:
```xml
<!-- Code Coverage report generation -->
<plugin>
    <groupId>org.jacoco</groupId>
    <artifactId>jacoco-maven-plugin</artifactId>
    <version>0.7.9</version>
    <executions>
        <execution>
            <goals>
                <goal>prepare-agent</goal>
            </goals>
        </execution>
        <execution>
            <id>generate-code-coverage-report</id>
            <phase>test</phase>
            <goals>
                <goal>report</goal>
            </goals>
        </execution>
    </executions>
</plugin>
```

Then run the normal test command:
```bash
mvn test
```

Then view the HTML report under ./target/site/jacoco/*.html

## Run Mutation Tests

Mutation tests can show you where you are missing assertions!

Check the [PIT tests maven quick start](https://pitest.org/quickstart/maven/) guide for more info on running these tests.

Or create a _Run Configuration_ for "PIT mutation tests" selecting your test directory.

## Run E2e Tests
End-to-end testing can give you confidence that everything works together properly!

Run e2e Java tests using [Rest-Assuredh](https://rest-assured.io/)

## Serverless CLI

Scaffolded with the [serverless cli](https://www.serverless.com/) tool and the "java-maven-aws" template.
