# LearnMac

## Where is Java installation path in Mac?

Path - /Library/Java/JavaVirtualMachines/jdk1.8.0_101.jdk/Contents/Home

# How to kill a java process in mac?  

```
ps ax | grep java

kill -TERM <processid>

```

## How to check the memory size of folders?

```
du -hd 2 .
```


## How to sudo  in Mac ?

```
sudo su
```


## How to kill a process in Mac ?

-   Open Terminal and type this command 

```
top
```

-   This will list all the process.

Let us say that you want to delete the java process that is already running.

-   Check for the PID java process in the list that is displayed by running the **top** command.
-   Run this command 

```
kill -9 [PID]
```

## How to kill a java process running on a particular port?

```
sudo lsof -i :8080
```
```
kill -9 [PID]
```

## How to display the Hidden files in Mac?

- Open the Terminal and run the below command.

```
defaults write com.apple.finder AppleShowAllFiles YES
```
- If you have finder open already, then close all the windows and press **control + option** and click on the touch pad . Press relaunch option.

## How to determine the Ip Address?
```
ifconfig |grep inet

http://osxdaily.com/2010/11/21/find-ip-address-mac/

```


## How to display the environment variables ?

- Open Terminal
- Type **printenv** in the terminal.This command will prints out all the environment variables.

## How to encode and decode using base64 encoding?

```
z001qgd@6c4008c0f7fa ~ $ echo 'mystring' | openssl base64
bXlzdHJpbmcK
z001qgd@6c4008c0f7fa ~ $ echo 'bXlzdHJpbmcK' | openssl base64 -d
mystring
```

# Chrome 

## How to open developer Tools ?

Cmd + Opt + I

Follow the below link for more options:

https://developers.google.com/web/tools/chrome-devtools/inspect-styles/shortcuts


## How to minimize the window?

```
command + m
```

## How to switch between windows of the same app ?

```
command + `
```

# Git

## How to display the current Working Branch in Terminal(Mac) ?

- Add the below piece of code at the bottom of the **.bash_profile** file.

```
# Git branch in prompt.

parse_git_branch() {

    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'

}

export PS1="\u@\h \W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "

```

# Brew

## How to install Brew ?

Run the below command.

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

```

# PostGresSql

## How to install PostGres?

Run the below command : 

```
brew install postgres

```

How to Start PostGres?

```
brew services start postgresql
```

How to Stop PostGres?

```
brew services stop postgresql

```

#### How to Create a user in Postgres via command line?  

https://www.postgresql.org/docs/9.1/static/app-createuser.html

```
createuser -h localhost -p 5432 -S -D -R -e postgres

```

#### How to create a DB in Postgres via command line?  

https://www.postgresql.org/docs/9.1/static/app-createdb.html

```
createdb -p 5432 -h localhost -e localDB

```


## PostGres Client

Download the postgres client **pgAdmin** from the below link. 

[PostGres Client](https://www.postgresql.org/ftp/pgadmin3/pgadmin4/v1.1/macos/)

# Gradle 
## How to set up gradle in local

- Download gradle from the Gradle website from the following link [Gradle Download](https://gradle.org/gradle-download/)
- Download the complete distribution and unzip it.
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
## Gradle Commands

**gradle assemble** - This will build the project and places the artifact in the build folder.

