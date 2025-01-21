# Micronaut Boostrap
Open-Source [Micronaut](https://micronaut.io) Java library, with baseline 17, for [Bootstrap components](https://getbootstrap.com). This library is licensed under Apache 2.0 License.

## Installation

The library is available in Maven Central. 

## License Management

This template uses the [Spotless Gradle Plugin](https://github.com/diffplug/spotless) to ensure every file contains a license matching the template in `config/spotless.license.java`.

## Checkstyle

The template applies the [Checkstyle Gradle Plugin](https://docs.gradle.org/current/userguide/checkstyle_plugin.html). You can configure it with `config/checkstyle/checkstyle.xml` and `config/checkstyle/supressions.xml`

## Code Coverage

The template applies the [JaCoCo Gradle Plugin](https://docs.gradle.org/current/userguide/jacoco_plugin.html) to get code coverage and the [JaCoCo report Aggregation Plugin](https://docs.gradle.org/current/userguide/jacoco_report_aggregation_plugin.html). 

Run `./gradlew testCodeCoverageReport` and you can access the HTML report `open code-coverage-report/build/reports/jacoco/testCodeCoverageReport/html/index.html`.

## GraalVM Native Image

The template applies the [Gradle Build Native Image Plugin](https://graalvm.github.io/native-build-tools/latest/gradle-plugin.html). You can run the Gradle task `./gradlew nativeTest` to ensure your library is compatible with Native Image.  

## Publish to Sonatype OSSRH (OSS Repository Hosting)

- Bump up version. Ensure `projectVersion` does not contain `-SNAPSHOT`. 
- Tag it. E.g. `v1.0.0`
- `./gradlew publishToSonatype closeSonatypeStagingRepository --info`