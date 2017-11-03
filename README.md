# BintrayUpload

## 根目录build.gradle添加如下代码

```
repositories {
        jcenter()
        mavenCentral()
    }
    
classpath 'com.github.dcendents:android-maven-gradle-plugin:1.5'
classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.7.2'
```
## Library目录下build.gradle底部添加如下代码

```
apply from: 'https://raw.githubusercontent.com/chaichuanfa/BintrayUpload/master/bintrayUpload.gradle'
```
## gradle.properties添加如下配置信息

```
#project
#项目名称
project.name=emoji-compat
#项目组ID，通常情况下如果你的包名为com.example.test，那么项目组ID就是com.example
project.groupId=com.github.chaichuanfa
#项目ID，通常情况下如果你的包名为com.example.test，那么项目ID就是test
project.artifactId=emoji-compat
#包类型，Android库是aar
project.packaging=aar
#项目官方网站的地址，没有的话就用Github上的地址
project.siteUrl=https://github.com/chaichuanfa
#项目的Git地址
project.gitUrl=https://github.com/chaichuanfa/EmojiCompat.git

#javadoc 生成的javadoc打开后主页显示的名称，通常跟项目名称一样即可
javadoc.name=emoji-compat
```
## local.properties添加如下配置信息

```
#bintray
bintray.user=***
bintray.apikey=***

#developer
developer.id=***
developer.name=***
developer.email=***
```
## 上传Bintray
```
gradle bintrayUpload
```