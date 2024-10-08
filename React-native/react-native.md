# Setting up the development environment
#### This page will help you install and build your first React Native app.

#### If you are new to mobile development, the easiest way to get started is with Expo CLI. Expo is a set of tools built around React Native and, while it has many features, the most relevant feature for us right now is that it can get you writing a React Native app within minutes. You will only need a recent version of Node.js and a phone or emulator. If you'd like to try out React Native directly in your web browser before installing any tools, you can try out Snack.

#### If you are already familiar with mobile development, you may want to use React Native CLI. It requires Xcode or Android Studio to get started. If you already have one of these tools installed, you should be able to get up and running within a few minutes. If they are not installed, you should expect to spend about an hour installing and configuring them.

# 
## React Native CLI Quickstart
# 

#### Follow these instructions if you need to build native code in your project. For example, if you are integrating React Native into an existing application, or if you "ejected" from Expo, you'll need this section.

#### The instructions are a bit different depending on your development operating system, and whether you want to start developing for iOS or Android. If you want to develop for both Android and iOS, that's fine - you can pick one to start with, since the setup is a bit different.
#
# Linux
## Installing dependencies#
#### You will need Node, the React Native command line interface, a JDK, and Android Studio.

#### While you can use any editor of your choice to develop your app, you will need to install Android Studio in order to set up the necessary tooling to build your React Native app for Android.

## Node
# 

Follow the [installation instructions for your Linux distribution](https://nodejs.org/en/download/package-manager/) to install Node 12 or newer.

## Java Development Kit
#### React Native requires at least the version 8 of the Java SE Development Kit (JDK). You may download and install [OpenJDK](http://openjdk.java.net/) from [AdoptOpenJDK](https://adoptopenjdk.net/) or your system packager. You may also [Download and install Oracle JDK 14](https://www.oracle.com/java/technologies/javase-downloads.html) if desired.    


## Android development environment
#### Setting up your development environment can be somewhat tedious if you're new to Android development. If you're already familiar with Android development, there are a few things you may need to configure. In either case, please make sure to carefully follow the next few steps.



## 1. Install Android Studio
#
#### Download and install Android Studio. While on Android Studio installation wizard, make sure the boxes next to all of the following items are checked:

-Android SDK
-Android SDK Platform
-Android Virtual Device
#### Then, click "Next" to install all of these components.
~~~
If the checkboxes are grayed out, you will have a chance to install these components later on.
~~~

#### Once setup has finalized and you're presented with the Welcome screen, proceed to the next step.


## 2. Install the Android SDK
#
#### Android Studio installs the latest Android SDK by default. Building a React Native app with native code, however, requires the Android 10 (Q) SDK in particular. Additional Android SDKs can be installed through the SDK Manager in Android Studio.

#### To do that, open Android Studio, click on "Configure" button and select "SDK Manager".
~~~
The SDK Manager can also be found within the Android Studio "Preferences" dialog, under Appearance & Behavior → System Settings → Android SDK.
~~~
#### Select the "SDK Platforms" tab from within the SDK Manager, then check the box next to "Show Package Details" in the bottom right corner. Look for and expand the Android 10 (Q) entry, then make sure the following items are checked:

- Android SDK Platform 29
- Intel x86 Atom_64 System Image or Google APIs Intel x86 Atom System Image
#### Next, select the "SDK Tools" tab and check the box next to "Show Package Details" here as well. Look for and expand the "Android SDK Build-Tools" entry, then make sure that 29.0.2 is selected.

#### Finally, click "Apply" to download and install the Android SDK and related build tools.
#
## 3. Configure the ANDROID_HOME environment variable

#### The React Native tools require some environment variables to be set up in order to build apps with native code.

#### Add the following lines to your $HOME/.bash_profile or $HOME/.bashrc (if you are using zsh then ~/.zprofile or ~/.zshrc) config file:
~~~javascript
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
~~~
~~~
.bash_profile is specific to bash. If you're using another shell, you will need to edit the appropriate shell-specific config file.
~~~

#### Type source $HOME/.bash_profile for bash or source $HOME/.zprofile to load the config into your current shell. Verify that ANDROID_HOME has been set by running echo $ANDROID_HOME and the appropriate directories have been added to your path by running echo $PATH.

#### Please make sure you use the correct Android SDK path. You can find the actual location of the SDK in the Android Studio "Preferences" dialog, under Appearance & Behavior → System Settings → Android SDK.

## Watchman
#### Follow the [Watchman installation guide](https://facebook.github.io/watchman/docs/install.html) to compile and install Watchman from source.

[Watchman](https://facebook.github.io/watchman/docs/install.html) is a tool by Facebook for watching changes in the filesystem. It is highly recommended you install it for better performance and increased compatibility in certain edge cases (translation: you may be able to get by without installing this, but your mileage may vary; installing this now may save you from a headache later).




# Colocar la version de node que me permite trabajar con angular

~~~sql
  sudo npm install n -g
  sudo n 14.14
  sudo n 12.14
~~~

# Instalar Angular
 ~~~sql
 sudo npm install -g @angular/cli
~~~
# Instalar Nodejs
Instalar nodejs
~~~npm
  sudo apt install nodejs
  sudo apt install node
  sudo apt remove nodejs
~~~


# Instalar angular e Ionic
~~~npm
   sudo npm install -g @angular/cli
   sudo npm install -g @ionic/cli
~~~
# Instalar Pre Load para hacer el equipo mas rapido
~~~npm
sudo apt install preload
~~~



# Versiones de java instalados en el equipo
~~~npm
openjdk 11.0.11 2021-04-20
OpenJDK Runtime Environment (build 11.0.11+9-Ubuntu-0ubuntu2)
OpenJDK 64-Bit Server VM (build 11.0.11+9-Ubuntu-0ubuntu2, mixed mode, sharing)
~~~
# ==========================================================================