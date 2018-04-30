Modularized version of JSON-java (org.json)[ ![Download](https://api.bintray.com/packages/dua3/public/org.json/images/download.svg) ](https://bintray.com/dua3/public/org.json/_latestVersion)
===========================================

__Note:__ This fork just adds module definitions that make it possible to build standalone applications with jlink that use org.json. If you don't need modules or don't know about jlink, just use the [original version](https://github.com/stleary/JSON-java).

If something doesn't work feel free to contact me or open an issue. Please make sure that you don't report issues caused by my packaging upstream. If in doubt, report here.

# Binaries
Binaries are available at https://bintray.com/dua3/public/org.json.

##  Gradle dependency:
```
    repositories {
        ...
        maven { url  "https://dl.bintray.com/dua3/public" }
    }
    
    dependencies {
        compile 'org.json:json:20180130-jpms.1'
        ...
    }
```

## Maven dependency
After you have added the bintary repository, add: 
```
    <dependency>
        <groupId>org.json</groupId>
        <artifactId>json</artifactId>
        <version>20180130-jpms.1</version>
        <type>pom</type>
    </dependency>
```

# Module

In `module-info.java` in the root  of your source tree:
```
    requires org.json;
```

# Use the Module Path!

Don't forget that you have to add the Jar to the module path, not to the classpath!
