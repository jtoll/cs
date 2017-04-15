# Java on MacOS

Notes on how to get information about the Java components installed on your MacOS system.

### Find the location of Java applications and Java compilers.
```
$ which -a java javac
/usr/bin/java
/usr/bin/javac
```

Which are symlinks to elsewhere in the filesystem.
```
$ ls -l /usr/bin/java /usr/bin/javac
lrwxr-xr-x  1 root  wheel  74 Oct  1  2016 /usr/bin/java@ -> /System/Library/Frameworks/JavaVM.framework/Versions/Current/Commands/java
lrwxr-xr-x  1 root  wheel  75 Oct  1  2016 /usr/bin/javac@ -> /System/Library/Frameworks/JavaVM.framework/Versions/Current/Commands/javac
```


### Get version information for the application and compiler.
```
$ java -version
java version "1.7.0_80"
Java(TM) SE Runtime Environment (build 1.7.0_80-b15)
Java HotSpot(TM) 64-Bit Server VM (build 24.80-b11, mixed mode)
```
```
$ javac -version
javac 1.7.0_80
```


### Get configuration information from `java_home`
Actual location of any JDKs.  Apple uses `java_home`, to automagically direct the previous links to `java` and `javac`, to the appropriate JDK installed at the path below.

```
$ /usr/libexec/java_home -V
Matching Java Virtual Machines (1):
    1.7.0_80, x86_64:	"Java SE 7"	/Library/Java/JavaVirtualMachines/jdk1.7.0_80.jdk/Contents/Home

/Library/Java/JavaVirtualMachines/jdk1.7.0_80.jdk/Contents/Home
```


### Get version information about the browser JRE, if installed
```
$ /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin/Contents/Home/bin/java -version
java version "1.8.0_45"
Java(TM) SE Runtime Environment (build 1.8.0_45-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.45-b02, mixed mode)
```


### Other notable paths
```
~/.gradle/caches/minecraft/net/minecraftforge/forge/1.7.2-10.12.2.1133/unpacked/src/main/java
```


### References:
<https://docs.oracle.com/javase/8/docs/technotes/guides/install/mac_install_faq.html>
<https://docs.oracle.com/javase/8/docs/technotes/guides/install/mac_jdk.html>
<https://docs.oracle.com/javase/8/docs/technotes/guides/install/mac_jre.html>
<http://www.minecraftforge.net/wiki/Install_JDK>
