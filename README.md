# Documentation :: pitest by org.apache.easyant.plugins

# Description

Provides pitest integration (mutation testing)
	
# Example

```xml
<ea:plugin organisation="org.apache.easyant.plugins" module="pitest" revision="0.1"/>
```
Organisation attribute is optional. If not specified default one will be used.

```xml
<ea:plugin module="pitest" revision="0.1"/>
```

## Available targets

|target name|description|extension point|depends|
|-----------|-----------|---------------|-------|
|pitest:run|process mutation coverage|||
|pitest:init||||

## Imported module

|organisation|module|revision|Import type|prefix|
|------------|------|--------|-----------|------|
|org.apache.easyant.plugins|abstract-test|0.10|import||

## Module parameters

### Properties

|property|description|required|default value|
|--------|-----------|--------|-------------|
|pitest.reportdir|Output directory for the reports|false|${target.reports}/pitest|
|pitest.target.tests|A list of globs can be supplied to this parameter to limit the tests available to be run. This parameter can be used to point PIT to a top level suite or suites. Custom suites such as ClassPathSuite are supported. Tests found via these suites can also be limited by the distance filter.|false|*|
|pitest.target.classes|The classes to be mutated|false|*|
|pitest.nbthread|The number of threads to use when mutation testing|false|1|

## Ivy Configurations

|name|description|extends|visibility|deprecated|
|----|-----------|-------|----------|----------|
|default|runtime dependencies artifact can be used with this conf|[]|public||
|test|this scope indicates that the dependency is not required for normal use of the application, and is only available for the test compilation and execution phases.|[]|private||
|provided|this is much like compile, but indicates you expect the JDK or a container to provide it. It is only available on the compilation classpath, and is not transitive.|[]|public||

## Dependencies Overview

|Organisation|Module|Revision|
|------------|------|--------|
|org.pitest|pitest-ant|1.0.0|
|org.pitest|pitest|1.0.0|

