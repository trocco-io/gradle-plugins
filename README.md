# gradle-plugins
Repository for gradle plugins


# Usage

## embulk-integration-test.gradle

Add 'integrationTest' task for embulk. The task search '*.yml' files and run it with embulk.
embulk log files are like '*.yml.run.log'. After running embulk, these log files can use
from test code under 'src/integration-test/java/'.

* Apply this gradle config file.

```
   apply from: 'https://raw.githubusercontent.com/hata/gradle-plugins/master/embulk-integration-test.gradle'
```

* Set dependency like this:

```
   project.tasks.integrationTest.dependsOn(classpath)
```

* To skip this plugin

```
  $ ./gradlew -DskipIntegrationTest=true gem
```


