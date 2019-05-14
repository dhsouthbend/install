# Tweepy

[Tweepy](http://www.tweepy.org/) is a Python library for accessing the twitter API. It is installed via the [conda](conda.md) package managment system using the conda-forge package index.

## Pre-installation instructions for Mac users (Mac0S 10.14.x)

*Note: Users on MacOS 10.13.x and earlier can skip straight to "Install Tweepy" below.* 

Mac users who jump straight to the instructions below are almost certain to have their install fail, particularly if they're on a more recent version of MacOS. To avoid difficulties, please take the following steps *prior* to trying to install Tweepy (many thanks to commenters on this [conda issues discussion](https://github.com/conda/conda/issues/8440), particularly [schlepuetz](https://github.com/conda/conda/issues/8440#issuecomment-482082853) and [weimeng0123](https://github.com/conda/conda/issues/8440#issuecomment-491166980)), for the suggestions that helped us solve this installation problem).

1. *Give conda the permissions needed to write to your hard disk:*

    Open "System Preferences > Security & Privacy > Privacy"
    Grant "Full Disk Access" for the conda application (e.g.: ~/anaconda3/bin/conda)
    
2. Remove all files with a .app extension from the ~/anaconda3 and ~/anaconda3/bin directories. You can do this from the Finder, or, if you prefer, you can do it from the command line using the following terminal commands:

    `cd ~/anaconda3 && rm -rf *.app`
    `cd ~/anaconda3/bin && rm -rf *.app`
    
You may also want to run `conda update --all` from the Terminal.

Once you've completed these steps, you should be able to install Tweepy.

## Install Tweepy

1. *Open* a [windows](windows_terminal.md) or [OS/X](osx_terminal.md) terminal
2. *Type* the following into the terminal:

```shell
conda install tweepy -c conda-forge -y
```

The terminal should print something like the following:

```bash
Fetching package metadata .............
Solving package specifications: .

Package plan for installation in environment /Users/hannah/miniconda3/envs/installenv:

The following NEW packages will be INSTALLED:

    asn1crypto:        0.24.0-py36_0                 conda-forge
    blinker:           1.4-py_0                      conda-forge
    cffi:              1.11.5-py36_0                 conda-forge

        .... omitted text ....

oauthlib-2.1.0 100% |########################################################| Time: 0:00:00   1.06 MB/s
```

## Test Tweepy install
While still in the terminal, launch the Python interpreter by *typing* `Python`. You should then see something like:
```python
Python 3.6.5 |Anaconda, Inc.| (default, Apr 26 2018, 08:42:37) 
[GCC 4.2.1 Compatible Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

Then try to load tweepy by typing `import tweepy` If everything has installed correctly, you will then see a blank line starting with `>>>` underneath, as shown below. 
```python
Python 3.6.5 |Anaconda, Inc.| (default, Apr 26 2018, 08:42:37) 
[GCC 4.2.1 Compatible Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import tweepy
>>> 
```

If the installation failed, the terminal will print an error. 
