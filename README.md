# gradle-plugins
Repository for gradle plugins


# Usage

## embulk-integration-test.gradle

Add 'integrationTest' task for embulk. The task search '*.yml' files and run it with embulk.
There are the log files after running embulk like '*.yml.run.log'. After running embulk,
these log files can use from test code under 'src/integration-test/java/'.

Right now, this task is skipped by default if there is no '-DenableIntegrationTest=true' flag
because this task is a platform dependent task. Please set the system property to run this task.

* Apply this gradle config file.

```
   apply from: 'https://raw.githubusercontent.com/hata/gradle-plugins/master/embulk-integration-test.gradle'
```

* Set dependency like this:

```
   project.tasks.integrationTest.dependsOn(classpath)
```

* To enable this plugin tasks

```
  $ ./gradlew -DenableIntegrationTest=true gem
```


