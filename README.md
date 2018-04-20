# IntelliJ Tutorials
These tutorials are not completely finished but should still provide some help to new IntelliJ IDEA users.

## Paths
(currently only one, more soon)
### Bukkit Path
The Bukkit path includes the basics of project setup, jar builds, and debugging, as well as plugin setup and testing.

#### IntelliJ IDEA Basics
If you have never used IntelliJ or don't understand run configurations and the debugger this is a good place to start.
###### [JDK Setup](https://goo.gl/aM42h8) (redo maybe)
Feel free to skip this step if you already added your JDK.
###### [New Project](https://goo.gl/t9FjKP)
IntelliJ is based on Projects instead of Workspaces like Eclipse. However it also has 'Modules' every project has at least one Module and each Module can be configured separately or even use different languages. To begin with you don't need to worry about them at all.
###### [Hello World](https://goo.gl/dTPA31)
In IntelliJ it's very simple to create packages and classes, you can even use the down arrow key to pick between class, interface enum, etc.
###### [Run Configuration](https://goo.gl/9VBqRG)
Run configurations are used to quickly run or debug project.
IntelliJ has a bunch of different types for various situations. The most basic is the 'Application' config, it simply runs your code starting at whatever main class you specify.
###### [Breakpoints](https://goo.gl/LZ2GGr)
Breakpoints allow you to pause your code and interact with it while it runs. It's often helpful to use it to check what values your variables have if you run into bugs. It might look intimidating so I recommend you do [this](https://goo.gl/LjvrAh) to make it simpler. The debugger is very powerful but there are only a few features you will need to start with.
- Variables, each variable and it's value is displayed [here](https://goo.gl/q47RzV). Values are also shown next to the variable in the code editor.
- Watches, you can add custom watches that display more complex information like [this](https://goo.gl/J2LtaC).
- Step Control, you can allow the code to run line by line using these controls.
	- [Step In](https://goo.gl/oTu3PC), if a method is called on this line it moves to the first line of that method. 
	- [Step Over](https://goo.gl/No8hDk), moves to the next line in the current method.


#### Basic Bukkit
###### [Bukkit Project](https://goo.gl/URsDsm)
The first step is to create a project using the maven dependency manager. Maven is not a requirement for a bukkit project, however it allows us to easily add dependencies including spigot itself. There are several key steps to this setup.
- Server the first step is creating a Server directory that we can use to test our plugin. I recommend you keep it within the plugin itself even if that means making a new copy of your server for each plugin. 
- Maven after creating a new maven project we need to use maven's pom.xml to specify our dependencies including spigot. We also need to tell maven to put the jar directly into our plugins folder using the shade plugin, which will in the future add our dependencies into our jar as well. To make it easier [here](https://gist.github.com/Exerosis/89cade862d386ef1b476e158b3ad208d) is all you need to add to your average plugin's project.
- Creating a run configuration is the last step, we need to tell IntelliJ to start by telling maven to create a jar using the maven 'package' command, then launch or restart our server whenever we want to test changes.(I will be releasing a system that uses reload in the future) This step is the simplest way to make debugging work, however it is not the only way I will explain some other ways in the future.
###### [Debugging Plugins](https://goo.gl/Gz1Bz6)
This is an example of one of the more advanced debug features. 'Evaluate code fragment' this allows you to run new code to test old code, or experiment even while your plugin is running. I find this to be one of the best ways to experiment with new features. (note: In the future I will release a system that freezes the minecraft client as well to prevent time outs)


# Index
#### Setup
- [JDK Setup](https://goo.gl/aM42h8) (redo maybe)
- [New Project](https://goo.gl/t9FjKP)
- [Hello World](https://goo.gl/dTPA31)
- [Bukkit No Maven](https://drive.google.com/uc?id=1w3GqvhDgqLEfk1HV3slefz10oB_Qf5y_)

#### Artifacts
- [Executable Jar](https://goo.gl/jexs8q)

#### Run Configurations
- [Application](https://goo.gl/9VBqRG)
- [Jar Application](https://goo.gl/zDWYQG)
- [Maven Build](https://goo.gl/ufYndg)

#### Debugging
- [Breakpoints](https://goo.gl/LZ2GGr)
- [Evaluation](https://goo.gl/Gz1Bz6)

#### Maven
- [New Project](https://goo.gl/BEZ1qD)
- [Fat Jar](https://goo.gl/C8tZLu)
- [Bukkit Project](https://goo.gl/URsDsm)

#### Gradle
- [New Project](https://drive.google.com/uc?id=1VGMx6ZqropObduXi5NBRglh0etHzJdV5)
- [Fat Jar](https://drive.google.com/uc?id=13N5YyxGZ58SxP0VMGenpc1D6ppxcSPX-)
- [Bukkit Plugin](https://drive.google.com/uc?id=13N5YyxGZ58SxP0VMGenpc1D6ppxcSPX-)
#### Resources
- [pom.xml](https://gist.github.com/Exerosis/89cade862d386ef1b476e158b3ad208d)
- [build.gradle](https://gist.github.com/Exerosis/6295bfa825c21bc63ada3fee20c890b0)


