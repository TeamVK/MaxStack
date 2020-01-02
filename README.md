# MaxStack

Some of vk2gpz's plugins (such as MergedMob, TokenEnchant) may drop a large amount of items on the ground.  
Based on users request, this plugin was created to significantly reduce the items on the ground by merging those items into a special dropped item.

This plugin can handle any dropped Items on the ground for merging, and there are three different merging mode:

Any developers who wishes to use some APIs available in this plugin can use this resoruce through Maven repository in your dev environment.

## Using maven repository
`MaxStack` is hosted on TeamVK's public maven repository and you can reference it in your dev environment.

### Gradle
Here is an example of a fragment of the script you can add to your build.gradle.

```
plugins {
    id "com.github.unafraid.gradle.git-repo-plugin" version "2.0.4.1"
    id "java"
    id "maven-publish"
}

// this will allow you to use github() to specify the github hosted maven repository
apply plugin: "com.github.unafraid.gradle.git-repo-plugin"

repositories {
    jcenter()
    mavenCentral()
    github("teamvk", "maven-repository", "origin", "master", "release")
}

dependencies {
    // ... other dependencies
    compile group: 'org.spigotmc', name: 'spigot', version: '1.15.1'
    compile group: 'com.vk2gpz.maxstack', name: 'MaxStack', version: '2.6.0'
    // ... other dependencies
}
```

## [API Documentation](javadoc/index.html)

## [Donation](http://PayPal.Me/vk2gpz)
It would be greatly appreciated for your donation to continue providing support for this plugin.
