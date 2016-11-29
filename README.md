# LearnMac

## How to display the Hidden files in Mac?

- Open the Terminal and run the below command.

```
defaults write com.apple.finder AppleShowAllFiles YES
```
- If you have finder open already, then close all the windows and press **control + option** and click on the touch pad . Press relaunch option.


## How to set up gradle in local

- Download gradle from the Gradle website.
- Open the **.bash_profile** that will be present in the **/Users/[username]/** folder.
- Add below lines in to the profile file.
- **GRADLE_HOME** - folder which has the downloaded path of Gradle.

```
GRADLE_HOME=/Users/[username]/Dilip/Soft/gradle-3.2.1;
export GRADLE_HOME
export PATH=$PATH:$GRADLE_HOME/bin
```
- Open a new terminal and type **Gradle** 

- Below message will be displayed. 
```

Welcome to Gradle 3.2.1.

To run a build, run gradle <task> ...

To see a list of available tasks, run gradle tasks

To see a list of command-line options, run gradle --help

To see more detail about a task, run gradle help --task <task>

BUILD SUCCESSFUL

Total time: 0.926 secs
```


