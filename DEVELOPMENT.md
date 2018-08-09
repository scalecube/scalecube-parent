# Setting up development environment

## Install the necessary build tools
You require to have latest stable [Open JDK 8](http://openjdk.java.net/projects/jdk8u/), latest stable 
[Apache Maven](http://maven.apache.org/) and [Git](http://git-scm.com/) installed on your machine.

## Set up IntelliJ IDEA
ScaleCube project team uses [IntelliJ IDEA](http://www.jetbrains.com/idea/) as the primary IDE, although we are fine 
with using other development environments as long as you adhere to our coding style.

### Code style
ScaleCube project team uses [Google code style](http://google.github.io/styleguide/javaguide.html)

#### Note, in the past, we used an altered version of google code style. We now comply the google style guidelines fully

The best way to go is to format your code *before pushing*

You can use [google-java-format](https://github.com/google/google-java-format).
There are plugins for [IntelliJ](https://github.com/google/google-java-format#intellij) and [Eclipse](https://github.com/google/google-java-format#eclipse) 


## IntelliJ Users (that doesn't want to install the plugin for some reason) should:
0. Download [this code style configuration](https://github.com/google/styleguide/blob/gh-pages/intellij-java-google-style.xml)
Apply the configuration:

## Eclipse Users (that doesn't want to install the plugin for some reason) should:
0. Download [this code style configuration](https://github.com/google/styleguide/blob/gh-pages/eclipse-java-google-style.xml)
Apply the configuration: 
0. Opening Eclipse settings varies per OS. For example, on macOS open `Eclipse` -> `Preferences`. On Ubuntu it's `Window` -> `Preferences`
0. In the search bar on the left, type *formatter*, and select the `Java` -> `Code Style` -> `Formatter` menu item
0. Click **Import** and browse to the XML file you have downloaded in Step 1.
0. Ensure the **GoogleStyle** item is selected in the **Active profile** section.
0. The import order should be empty:
    0. Create a simple file with a single line in it `0=\#`
    0. Open Eclipse settings (same as above)
    0. In the search bar on the left, type *import*, and select the `Java` -> `Code Style` -> `Organize Imports` menu item
    0. Click **Import** and browse to the text file you have created in Step 1.

## verifying style
Whatever you do, It's OK, as long as a maven build: `mvn checkstyle:check -Dcheckstyle.config.location=google_checks.xml -Dcheckstyle.skip=false` finishes successfuly
