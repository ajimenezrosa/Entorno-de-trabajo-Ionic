# React Native Configuration Windows
## Installing dependencies
#### You will need Node, the React Native command line interface, a JDK, and Android Studio.

#### While you can use any editor of your choice to develop your app, you will need to install Android Studio in order to set up the necessary tooling to build your React Native app for Android.

## Node, JDK
#### We recommend installing Node via [Chocolatey](https://chocolatey.org/install), a popular package manager for Windows.

#### If you want to be able to switch between different Node versions, you might want to install Node via [nvm-windows](https://github.com/ajimenezrosa/nvm-windows), a Node version manager for Windows.

#### React Native also requires [Java SE Development Kit (JDK)](https://openjdk.java.net/projects/jdk8/), which can be installed using Chocolatey as well.

#### Open an Administrator Command Prompt (right click Command Prompt and select "Run as Administrator"), then run the following command:
~~~~npm
choco install -y nodejs.install openjdk8
~~~~
# 
#### If you have already installed Node on your system, make sure it is Node 12 or newer. If you already have a JDK on your system, make sure it is version 8 or newer.

        You can find additional installation options on [Node's Downloads page.](https://nodejs.org/en/download/)

#### If you're using the latest version of Java Development Kit, you'll need to change the Gradle version of your project so it can recognize the JDK. You can do that by going to {project root folder}\android\gradle\wrapper\gradle-wrapper.properties and changing the distributionUrl value to upgrade the Gradle version. You can check out [here the lastest releases of Gradle.](https://gradle.org/releases/)

## Android development environment
# 
#### Setting up your development environment can be somewhat tedious if you're new to Android development. If you're already familiar with Android development, there are a few things you may need to configure. In either case, please make sure to carefully follow the next few steps.

## 1. Install Android Studio
#### [Download and install Android Studio](https://developer.android.com/studio/index.html). While on Android Studio installation wizard, make sure the boxes next to all of the following items are checked:

- Android SDK
- Android SDK Platform
- Android Virtual Device
- If you are not already using Hyper-V: Performance (Intel ® HAXM) [(See here for AMD or Hyper-V)](https://android-developers.googleblog.com/2018/07/android-emulator-amd-processor-hyper-v.html)
#### Then, click "Next" to install all of these components.

        If the checkboxes are grayed out, you will have a chance to install these components later on.

#### Once setup has finalized and you're presented with the Welcome screen, proceed to the next step.

## 2. Install the Android SDK
#### Android Studio installs the latest Android SDK by default. Building a React Native app with native code, however, requires the Android 10 (Q) SDK in particular. Additional Android SDKs can be installed through the SDK Manager in Android Studio.

#### To do that, open Android Studio, click on "Configure" button and select "SDK Manager".

[](https://www.tutorialesprogramacionya.com/javaya/androidya/androidstudioya/imagentema/foto004.jpg)



Android Studio Welcome

The SDK Manager can also be found within the Android Studio "Preferences" dialog, under Appearance & Behavior → System Settings → Android SDK.

Select the "SDK Platforms" tab from within the SDK Manager, then check the box next to "Show Package Details" in the bottom right corner. Look for and expand the Android 10 (Q) entry, then make sure the following items are checked:

Android SDK Platform 29
Intel x86 Atom_64 System Image or Google APIs Intel x86 Atom System Image
Next, select the "SDK Tools" tab and check the box next to "Show Package Details" here as well. Look for and expand the "Android SDK Build-Tools" entry, then make sure that 29.0.2 is selected.

Finally, click "Apply" to download and install the Android SDK and related build tools.

3. Configure the ANDROID_HOME environment variable
The React Native tools require some environment variables to be set up in order to build apps with native code.

Open the Windows Control Panel.
Click on User Accounts, then click User Accounts again
Click on Change my environment variables
Click on New... to create a new ANDROID_HOME user variable that points to the path to your Android SDK:
ANDROID_HOME Environment Variable

The SDK is installed, by default, at the following location:

%LOCALAPPDATA%\Android\Sdk
You can find the actual location of the SDK in the Android Studio "Settings" dialog, under Appearance & Behavior → System Settings → Android SDK.

Open a new Command Prompt window to ensure the new environment variable is loaded before proceeding to the next step.

Open powershell
Copy and paste Get-ChildItem -Path Env:\ into powershell
Verify ANDROID_HOME has been added
4. Add platform-tools to Path
Open the Windows Control Panel.
Click on User Accounts, then click User Accounts again
Click on Change my environment variables
Select the Path variable.
Click Edit.
Click New and add the path to platform-tools to the list.
The default location for this folder is:

%LOCALAPPDATA%\Android\Sdk\platform-tools
React Native Command Line Interface
React Native has a built-in command line interface. Rather than install and manage a specific version of the CLI globally, we recommend you access the current version at runtime using npx, which ships with Node.js. With npx react-native <command>, the current stable version of the CLI will be downloaded and executed at the time the command is run.