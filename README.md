Before anything, be sure to enable "view hidden files" by pressing cmd + shift + .

Java 8 - Follow instructions as per windows version
To find install location, use /usr/libexec/java_home -v 1.8 in terminal.
Set classpath by editing .bash_profile with any terminal or plaintext editor (Textedit) and inserting the lines

JAVA_HOME= /Library/Java/JavaVirtualMachines/jdk1.8.0_211.jdk/Contents/Home/

export JAVA_HOME;

Make sure that the version is correct and the path is the same as what the first command returned.

NetBeans - For NetBeans I suggest this installation script (https://github.com/carljmosca/netbeans-macos-bundle) someone posted on GitHub. This installs NetBeans 11.1.

To run the script, drag and drop the install.sh file into your terminal and hit enter. Follow the instructions. After the script is finished, you should have NetBeans in your Applications.

Follow step 7 in the Windows guide provided by Prof (Edit netbeans11\etc\netbeans.conf by uncommenting netbeans_jdkhome= and setting it to your path to JAVA_HOME) (Type  out the full thing)

There is no tab for activating Java in NetBeans Mac (for mine at least), so just go into Tools > Plugins and Check for Updates. Other funcationalities can be activated once they're needed (i.e when installing Glassfish later)
 

Glassfish - The procedure for installling glassfish is basically the same as the Windows version, just follow prof's guide. (Except that you probably want to install in your users folder since you dont have C:)

Once installed, edit the .bat file as per windows installation.

Then, add in

GLASSFISH_HOME=Your_Glassfish_Path_Here

export GLASSFISH_HOME;

into .bash_profile (im not sure if this is actually needed but might as  well)

To test, start the glassfish server within your NetBeans IDE, and if prompted, direct the application to use Java 8 to start the server by navigating to your Java home folder as per the Java 8 installation. Check localhost:8080 and localhost:4848 to make sure it runs fine. Once its okay, stop the server.

 

MySQL - For MySQL, you have to download the different parts manually since there is no all in one installer for mac. Just download and install accordingly.

As for the J connector, download and follow the instructions for the windows version. Note that your netbeans may not have an ide folder, and might directly just have the modules folder in the NetBeans11.1 folder.

Git - Use this installation link for Git (https://git-scm.com/download/mac) OR use Homebrew to install.

Not sure if you need to edit your path, but if you do, go back to .bash_profile and add the git install location into your path variable.

Jenkins - To install Jenkins, I suggest this guide (https://java2blog.com/install-jenkins-mac-os-x/). Just remember to change your port from 8080 to 8090.

This might not be 100% correct but I hope it helps you with installing the mac equivalent software.
