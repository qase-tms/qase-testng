# Qase TMS TestNG Integration #
[ ![Download](https://api.bintray.com/packages/qase/maven/io.qase.qase-testng/images/download.svg?version=0.0.1) ](https://bintray.com/qase/maven/io.qase.qase-testng/0.0.1/link)
[![License](https://lxgaming.github.io/badges/License-Apache%202.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

## Описание ##
Позволяет выгружать в Qase TMS результаты выполнения автотестов.

Привязка автотестов к кейсам из Qase TMS осуществляется при помощи аннотации @CaseId

### Обязательные параметры ###
Все обязательные параметры передаются либо через системные переменные, либо через переменные окружения:

|  Ключ     | Описание |
| :----------: | :----------: |
| qase.project_code | Project Code |
| qase.run.id       | Run Id |
| qase.api.token    | API Token для доступа к Qase API |
| qase.case.list    | Список кейсов, разделенных запятой |


## Maven ##

Add the following dependency and repository to your pom.xml:
```xml
<dependency>
    <groupId>io.qase</groupId>
    <artifactId>qase-testng</artifactId>
    <version>0.0.1</version>
</dependency>
```


```xml
<repository>
    <id>io.qase</id>
    <url>https://dl.bintray.com/qase/maven/</url>
</repository>
```


## Пример передачи обязательных параметров ##

```
mvn clean test -Dqase.project_code=123 -Dqase.run.id=123 -Dqase.api.token=ebc2ifu21321edqwd2214 -Dqase.case.list=123,321,124
```