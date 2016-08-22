# Android Studio Installation Instructions

~~~~  
## android studio prereq:
JDK
JRE

[2016-04-08 Fri 23:58]
http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
Windows x64	187.31 MB  	jdk-8u77-windows-x64.exe

install takes about 3 or 4 minutes
C:\Program Files\Java\jdk1.8.0_77\

http://docs.oracle.com/javase/8/docs/

[2016-04-09 Sat 00:13]
had to manually uninstall these two...
- from win10 programs and features applet
- which were installed on 2014-09-10
jdk1.8.0_20
jre1.8.0_20

[2016-04-09 Sat 00:16]
uninstalled android studio v1.0
- from win10 programs and features applet
C:\Program Files\Android\Android Studio\


javoc -version
does not work

java -version
java version "1.8.0_77"
Java(TM) SE Runtime Environment (build 1.8.0_77-b03)
Java HotSpot(TM) 64-Bit Server VM (build 25.77-b03, mixed mode)



android studio install:
http://developer.android.com/sdk/index.html
includes...
Android Studio IDE
Android SDK tools
- enable you to debug, profile and compile your app
Android 6.0 (Marshmallow) platform
Android 6.0 emulator system image with Google APIs
Android virtual device
- a preconfigured and optimized Android Virtual Device fore app testing on the emulator (recommended)
Performance (Intel HAXM)
- a hoardware-assisted virtualization engine (hypervisor)
- which speeds up Android emulation on your development computer (recommended)

HAXM:
hardware accelerated manager



[2016-04-09 Sat 00:24]
android-studio-bundle-143.2739321-windows.exe
1.1gb
4.2gb space required
leave the two options selected

C:\Program Files\Android\Android Studio
- 500mb required

C:\Users\Dimebag\AppData\Local\Android\sdk
- 3.2gb required


[2016-04-09 Sat 00:33]
Error launching Android Studio
The environment variable JAVA_HOME (with the value of C:\Program Files\Java\jdk1.8.0_20) does not point to a valid JVM installation.

solution...
right click start button -> system -> in left pane click Advanced System settings -> Advanced tab > Environment Variables button -> System variables section
 and add a new system variable JAVA_HOME
- that points to your JDK folder
- for example C:\Program Files\Java\jdk1.8.0_77
ref:
http://developer.android.com/sdk/installing/index.html

changed...
JAVA_HOME
C:\Program Files\Java\jdk1.8.0_77

JDK_HOME
C:\Program Files\Java\jdk1.8.0_77

also changed...
- for clojure
LEIN_JAVA_CMD
C:\Program Files\Java\jdk1.8.0_77\bin\java.exe


note:
I deleted....
ANDROID_HOME
C:\_devfw\adt-bundle-windows-x86_64-20140702\sdk

also deleted in 
User variables for Dimebag -> edit -> 
%ANDROID_HOME%\tools
%ANDROID_HOME%\platform-tools

also deleted...
C:\Users\Dimebag\.AndroidStudio1.5


[2016-04-09 Sat 00:52]
run android studio

Setup Type: Standard
SDK Folder: C:\Users\Dimebag\AppData\Local\Android\Sdk
Total Download Size: 197 MB
SDK Components to Download: Android Support Repository 197 MB

clicked the Finish button
It is now downloading
Downloading https://dl.google.com/android/repository/android_m2repository_r29.ziphttps://dl.google.com/android/repository/android_m2repository_r29.zip

Android SDK is up to date.
Running Intel® HAXM installer
Intel HAXM installed successfully!

took about a minute

[2016-04-09 Sat 00:56]
clicked Start a new android project

MyAndroidApp1
dimebag.example.com
C:\Users\Dimebag\AndroidStudioProjects\MyAndroidApp1

Minimum SDK
default is...
API 15: Android 4.0.3 (IceCreamSandwich)
97.3% of devices

I selected the Basic Activity

[2016-04-09 Sat 01:04]
clicked Allow access to windows firewall for...
C:\program files\java\jdk1.8.0_77\bin\java.exe

[2016-04-09 Sat 01:08]
Gradle build finished in 3m 17s 291ms


[2016-04-09 Sat 01:13]
added Nexus 5 AVD emulator
took a good 5 minutes, give it time



[2016-05-15 Sun 02:40]
add to the PATH envvar...
%USERPROFILE%\AppData\Local\Android\sdk\platform-tools
%USERPROFILE%\AppData\Local\Android\sdk\tools



Gradle Daemon:
https://docs.gradle.org/2.9/userguide/gradle_daemon.html
needed for react native

[2016-05-15 Sun 01:45]
gradle daemon install:
On Windows, this command will enable the Daemon for the current user:
(if not exist "%USERPROFILE%/.gradle" mkdir "%USERPROFILE%/.gradle") && (echo org.gradle.daemon=true >> "%USERPROFILE%/.gradle/gradle.properties")









android studio config:

java envvar: jdk envvar: envvar java:
- used for android studio install
in the "Environment Variables" dialog box -> click the New button
Adding two system environment variables.....
JDK_HOME
and...
JAVA_HOME
give each one this value...
C:\Program Files\Java\jdk1.7.0_25\
ref: http://stackoverflow.com/questions/16574189/android-studio-installation-on-windows-7-fails-no-jdk-found
works [2013-07-21 Sun 13:39]

note:
after installing jdk, I found this segment in the system path string...
C:\ProgramData\Oracle\Java\javapath;

[2014-09-19 Fri 17:36]
after installing the jdk, I added two entries, JDK_HOME and JAVA_HOME on acer laptop, each with this value....
C:\Program Files\Java\jdk1.8.0_20
then restart the CLI -> type 'set'

~~~~