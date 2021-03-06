# Course Setup

Welcome young cadet! This will guide you through setting up for the course. Why bother? Well here are some awesome benefits you'll get:

- Never deal with Courseworks homeworks upload
- Have your homework graded *instantly* (or as soon as the robot TA gets to it)
- See your code in its beautiful form and have TAs look and comment at specific lines

This is done through Jarvis, GitHub, and (optionally) Scoreboard.


## GitHub

GitHub is a web-based Git repository hosting service that. It makes it easy to
collaborate and host code all while using Git either in a GUI or on the command
line. It also has a very powerful API that we've made use to make our jobs
easier.

## Jarvis

Jarvis [http://jarvis.xyz](http://jarvis.xyz) is a proprietary homework submission system built for this class. It helps you set up your repositories and teams on GitHub, listens for when you submit your homework, and helps you grade them automatically in our testing environment, giving you really quick feedback. (For the geekier ones among you, Jarvis is the front-end to our Continuous Integration service)

## Scoreboard

Scoreboard is a service provided by Jarvis that allows you to compete with other students based on the score tally of your homeworks. It is totally experimental and optional, but we have a feeling that you want to have some fun with this. To opt-in, check the checkbox for Scoreboard when registering on Jarvis.

## Setup

### Create a GitHub Account

If you don't already have a GitHub acccount, sign up for one here: [https://github.com/join](https://github.com/join). If you already have one, there's no need to create an additional one for this class. In fact, please don't do that -- it will create way more trouble for you. We built this to encourage you to own your first GitHub account.

### Register with Jarvis

Now that you have a GitHub account, you need to add yourself to Jarvis so that Jarvis can set up your GitHub team and repositories automatically. This will also add you to Jarvis' autograding system. During registration, you can also opt-in to **Scoreboard**.

1. Go to the [Jarvis](http://jarvis.xyz/)
2. Click on the **register** tab
3. Enter your UNI. If it gives you an error saying that you're not enrolled for the class, contact the Head TA [Linan Qiu lq2137@columbia.edu](mailto:lq2137@columbia.edu).
4. Choose whether you want to opt-in to the Scoreboard.
5. Click on **GitHub Login**. This will bring you to GitHub where you will have to give permission to Jarvis.
6. If for any reason this fails, email the Head TA [Linan Qiu lq2137@columbia.edu](mailto:lq2137@columbia.edu).

You should now be apart of the CS3134 Organization and should have access to a few different repositories:
- You should now have a repository setup just for your homework solutions. This should be located in the CS3134 organization and be called `homework-<uni>`. This is what you'll setup in the next section to allow you to write your homework answers and submit them. If the above didn't work, contact one of the TAs to help you out.
- You should also have access to the other public / organization-only repositories for homework solutions, notes, admin etc.

You should have also received an email with your nickname. If for any reason you don't receive the confirmation email, email the Head TA [Linan Qiu lq2137@columbia.edu](mailto:lq2137@columbia.edu).

### Install Git

Install Git by following the instructions here for your operating system: [https://help.github.com/articles/set-up-git/](https://help.github.com/articles/set-up-git/).

Then, set up your authentication keys here: [https://help.github.com/articles/caching-your-github-password-in-git/](https://help.github.com/articles/caching-your-github-password-in-git/).

If you wan to learn more about Git, check out this very handy video here: [https://www.youtube.com/watch?v=0fKg7e37bQE](https://www.youtube.com/watch?v=0fKg7e37bQE)

### Setting Up Homeworks

You should have finished creating an account on GitHub, registering with Jarvis, and installing Git.

You should download [https://github.com/cs3134/admin/blob/master/setup.sh](https://github.com/cs3134/admin/blob/master/setup.sh) and run the `.sh` file.

#### Mac

You need to download the Admin zip from GitHub [https://github.com/cs3134/admin](https://github.com/cs3134/admin):

That link points to the cs3134/admin repo on GitHub. To download it, click the link on the bottom right of the screen 'Download ZIP'.

Unzip it, then drag the `setup.sh` to a folder where you want your homework files to be, open up Terminal, `cd` into the directory where the `setup.sh` is, and run

```bash
$ sh setup.sh <youruni>
```

For example, for me, I'd run

```bash
$ sh setup.sh lq2137
```

You should see a series of commands being run.

```
➜  admin git:(master) sh setup.sh lq2137
Cloning into 'homework-master'...
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
Checking connectivity... done.
Original remote -v setup
origin  https://github.com/cs3134/homework-master.git (fetch)
origin  https://github.com/cs3134/homework-master.git (push)
Renamed remote -v setup
upstream    https://github.com/cs3134/homework-master.git (fetch)
upstream    https://github.com/cs3134/homework-master.git (push)
Final remote -v setup
origin  https://github.com/cs3134/homework-lq2137 (fetch)
origin  https://github.com/cs3134/homework-lq2137 (push)
upstream    https://github.com/cs3134/homework-master.git (fetch)
upstream    https://github.com/cs3134/homework-master.git (push)
On branch master
Your branch is up-to-date with 'upstream/master'.
nothing to commit, working directory clean
Branch master set up to track remote branch master from origin.
Everything up-to-date
```

If you want to use Eclipse, simply import the entire `homework-<youruni>` directory as a project. The guide to using Eclipse is here: [https://github.com/cs3134/admin/blob/master/eclipse.md](https://github.com/cs3134/admin/blob/master/eclipse.md)

#### Linux

Do pretty much the same as the Mac people.

If you use Eclipse, this guide will be useful for importing projects: [https://github.com/cs3134/admin/blob/master/eclipse.md](https://github.com/cs3134/admin/blob/master/eclipse.md)

#### Windows

(Contributed by [Windows Guru Nick Mariconda nm2812@columbia.edu](mailto:nm2812@columbia.edu))

In order to run setup.sh on a Windows machine, you need to install Cygwin. Cygwin (pronounced sig-win) is a Unix-like environment and command-line interface for Windows. It's a good idea for Windows users to be familiar with Cygwin.

First, install Cygwin from the Cygwin homepage: https://cygwin.com/install.html

When running setup.exe, make sure to check off all the git packages at the appropriate step of the installation, as shown below:

![1](https://raw.githubusercontent.com/cs3134/admin/master/course-screenshots/git-cygwin.png?raw=true)

The default options of the installation are fine; the installation itself can take a pretty long time (mine took a few hours). It's totally worth it -- the installation repays itself many times over.

Once it's installed, open it up and you should be at a command prompt. Now you just need to run the setup.sh script and you're good to go:

You need to download the Admin zip from GitHub [https://github.com/cs3134/admin](https://github.com/cs3134/admin):

That link points to the cs3134/admin repo on GitHub. To download it, click the link on the bottom right of the screen 'Download ZIP'.

A File Explorer window should pop up with an 'admin-master' folder. Enter the folder and you should find the 'setup' shell script. Copy it, and then paste it in the home/USERNAME directory of Cygwin. You should be able to find this directory in the Cygwin folder located in the C drive directory. My full directory path for it looks like this: C:\cygwin\home\nick

Once it's pasted in that directory, open up Cygwin. Enter (without the `$` sign. The `$` sign indicates what follows is something you should enter):

```bash
$ ls
```

And you should see the setup.sh file. Now run it:

```bash
$ ./setup.sh <UNI>
```

eg. `./setup.sh nm2812`

NOTE: If for some reason you already had an older version of Cygwin installed (like I did), setup.sh may hang. That's because there used to be a bug in prompting the user to enter the GitHub credentials. Just re-run Cygwin's setup.exe to update to the newest version and it should work.

If the script runs correctly, you should see some output. Enter the 'ls' command again, and you should now see a `homework-<youruni>` directory, as well as the setup.sh file. If you see that, the setup ran successfully and you're ready to complete homework 0.

The files that lie in this `homework-<youruni>` directory are ultimately the ones that you will be modifying and submitting. You're free to compile and run your code on any platform you wish. I recommend using Eclipse. Here's how to get the code back and forth from Cygwin and Eclipse:

From Eclipse you'd simply import the `homework-<youruni>` directory (my path to that directory looks like this):

```
C:\cygwin\home\nick\homework-nm2812
```

For a illustrated guide, see this: [https://github.com/cs3134/admin/blob/master/eclipse.md](https://github.com/cs3134/admin/blob/master/eclipse.md)

Then, from within Eclipse, you should have no problem finding the Jarvis3134.java file and making the required change for homework 0. After that, you have to export the file back to the Cygwin directory.

Then, when you're ready to submit your homework, return to Cygwin. Enter the following command:

```bash
$ cd homework-<youruni>/0
```

This will take you to the '0' folder in the homework directory. The instructions for HW0 specify how to commit and submit through git from here.

This should (hopefully) be straightforward, but getting Windows to behave like Unix can sometimes be a pain. If anything goes wrong and you can't get it to work, please send me an email: [nm2812@columbia.edu](mailto:nm2812@columbia.edu)

#### Manual Installation

1. Clone the current homework repository by issuing the following commands onto the command line in a directory where you want the homeworks to be:

```bash
$ git clone https://github.com/cs3134/homework-master.git
```

It will make a complete replica of the homework repository locally. 

If you get an error that looks like:

```bash
Cloning into 'homework'...
Permission denied (publickey).
fatal: Could not read from remote repository.
```

More likely the cause is that you just haven't finished setting up your GitHub account. You just need to [setup an SSH key](https://help.github.com/articles/generating-ssh-keys/) to allow pushing and pulling over HTTPS.

2. Now we are going to change it to point to your personal repository that was created for you in the previous section (so that you don't end up submitting to the master repository and getting rejected permission errors). If you're curious, here's whats happening:

Originally, when you clone the repository, the local repository is a "copy" of the `cs3134/homework-master.git`. That means when you push code, you are pushing to that repository.

```
your local folder -------> cs3134/homework-master.git
```

```
your local folder ----     cs3134/homework-master.git
                     |---> cs3134/homework-<youruni>.git
```

How we do that is as follows:

Assuming that you've just cloned the folder, then let's rename that folder and go into it:

```bash
$ mv homework-master homework-<youruni>
$ cd homework-<youruni>
```

By default the remote called `origin` is set to the location that you cloned the repository from. You should see the following:

```bash
$ git remote -v
origin https://github.com/cs3134/homework-master.git (fetch)
origin https://github.com/cs3134/homework-master.git (push)
```

We don't want that remote to be the origin, instead, we want to change it to point to your repository. To do that, issue the following command:

```bash
$ git remote rename origin upstream
```

And now you should see the following:

```bash
$ git remote -v
upstream https://github.com/cs3134/homework-master.git (fetch)
upstream https://github.com/cs3134/homework-master.git (push)
```

4. Lastly we need to give your repository a new `origin` since it is lacking
   one. Issue the following but substituting your GitHub username in place:

```bash
$ git remote add origin https://github.com/cs3134/homework-<youruni>.git
```

But substitute in your own UNI of course.

If you have an error that looks like the following:

```
Could not rename config section 'remote.[old name]' to 'remote.[new name]'
```

Or this error:

```
fatal: remote origin already exists.
```

This appears to happen to some depending on the version of Git they are using. To fix it, just issue the following command:

```bash
$ git remote set-url origin https://github.com/cs3134/homework-<youruni>.git
```

For reference, your final `git remote -v` should look like following when its setup correctly:

```bash
$ git remote -v
origin  https://github.com/cs3134/homework-<youruni> (fetch)
origin  https://github.com/cs3134/homework-<youruni> (push)
upstream    https://github.com/cs3134/homework-master.git (fetch)
upstream    https://github.com/cs3134/homework-master.git (push)
```

4. Let's test it out by doing a push of your master branch to GitHub by issuing
   the following:

```bash
$ git push -u -f origin master
```

   You should see something like the following:

```
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 294 bytes | 0 bytes/s, done.
Total 3 (delta 2), reused 0 (delta 0)
To https://github.com/cs3134/homework-<youruni>.git   f726472..545a4f0  master -> master
```

5. That last command was a bit special and only needs to be ran the first time to setup the remote tracking branches. Now we should be able to just run `git push` without the arguments. Try it and you should get the following:

```bash
$ git push
Everything up-to-date
```

If you don't know Git that well, this probably seemed very arcane. Just keep
using Git and you'll keep understanding more and more.
