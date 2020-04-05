# Qase TMS TestNG Integration #
[ ![Download](https://api.bintray.com/packages/qase/maven/io.qase.qase-testng/images/download.svg?version=0.0.1) ](https://bintray.com/qase/maven/io.qase.qase-testng/0.0.1/link)
[![License](https://lxgaming.github.io/badges/License-Apache%202.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

## Description ##
This integration uploads test run results to Qase TMS via API.

To link autotest to test case in Qase TMS use annotation `@CaseId`

### Required params ###
All required params are passed through system properties or environment variables:

|  Key     | Description |
| :----------: | :----------: |
| qase.project.code | Project Code |
| qase.run.id       | Run Id |
| qase.api.token    | Qase API Token |
| qase.case.list    | A list of test cases with comma delimiter |


## Maven ##

Add the following dependency and repository to your pom.xml:
```xml
<dependency>
    <groupId>io.qase</groupId>
    <artifactId>qase-testng</artifactId>
    <version>1.0.0</version>
    <scope>test</scope>
</dependency>
```


```xml
<repository>
    <id>io.qase</id>
    <url>https://dl.bintray.com/qase/maven/</url>
</repository>
```


## Run example ##

```
mvn clean test -Dqase.project.code=PRJ -Dqase.run.id=123 -Dqase.api.token=ebc2ifu21321edqwd2214 -Dqase.case.list=123,321,124
```
