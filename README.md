<h1>timber-loggly <a href='https://peret.ci.cloudbees.com/job/timber-loggly/'><a href='https://peret.ci.cloudbees.com/job/timber-loggly/job/timber-loggly-SNAPSHOT/'><img src='https://peret.ci.cloudbees.com/buildStatus/icon?job=timber-loggly/timber-loggly-SNAPSHOT'></a></a></h1>
<sup>v1.0.0</sup>

A [Timber][2] tree for asynchronously posting log messages to [Loggly][1].

Usage
-----
1. Plant a `LogglyTree` with your [authorization token][4] from Loggly.
 ```java
 import android.app.Application;
 import com.github.peret.timber.loggly.LogglyTree;
 import timber.log.Timber;

 public class ExampleApp extends Application {

     @Override
     public void onCreate() {
         super.onCreate();

         final String LOGGLY_TOKEN = /* your loggly token */;
         Timber.plant(new LogglyTree(LOGGLY_TOKEN));
     }
 }
 ```

2. Use Timber API to log an event via `LogglyTree`...
 ```java
 Timber.tag("foo");
 Timber.i("hello world");
 ```

Download
--------

[timber-loggly-1.0.0.jar][5]

#### Gradle

```
compile 'com.github.peret:timber-loggly:1.0.0'
```

#### Maven

```xml
<dependency>
  <groupId>com.github.peret</groupId>
  <artifactId>timber-loggly</artifactId>
  <version>1.0.0</version>
</dependency>
```

Snapshots of the development version are available in [Sonatype's `snapshots` repository][3].


[1]: http://loggly.com
[2]: https://github.com/JakeWharton/timber
[3]: https://oss.sonatype.org/content/repositories/snapshots/com/github/peret/timber-loggly/
[4]: https://www.loggly.com/docs/customer-token-authentication-token/
[5]: http://goo.gl/Q0WPYU
