---
title: How To Install PHP on Windows
published: 2025-05-19
tags: ["ZeroToDev", "PHP", "Windows"]
category: DevNotes
draft: false
---

# Guide On How To Install PHP on Windows

This is a guide i created because it is also my first time trying to code in Windows. Honestly i always prefer to code in Linux over Windows..but currently, i have no choice but to code on Windows. I guess i will make this opportunity as my learning opportunity.


## 1. Go to official PHP Website

The link is this:

```

https://www.php.net/

```

But honestly just search manually to be safe.

## 2. Click download button on the homepage

You will be directed to this page below.

```

https://www.php.net/downloads.php

```
Now there are versions you can choose, also even [official install documentation here](https://www.php.net/manual/en/install.general.php) but i want to make my own version so i can revisit everytime i feel confused.

Here choose the stable version example **PHP 8.4.7** then below there are few sections you can pick, choose **Windows Downloads**

## 3. Choose Zip Thread Safe Download

You will be redirected again to different page

```

https://windows.php.net/download#php-8.4

```

This time there are also different options to download, generally download the Thread Safe section with the zip file (the size is around 32-33 MB). Download It and save it somewhere.

## Extract Everyting, Rename and Relocate it

Go to the place where you have saved the file, extract the file with WinRar, 7Zip or any other alternatives. (you can choose right click option on file and pick "Extract to "php-(version)" folder")

Once extracted, rename it to something easy or simple. Generally recommended to rename it to php with their version example: php-8.4.7

After renaming it, choose a location where you want to store this folder, recommended location would be C: or D:

After that copy the location of the top bar in your file explorer tab (so if the location of your php is in C: then it would be C:/php-8.4.7)

## Update Environment and Variables

Once you copy the location of the PHP folder, we need to update the environment and variables in our windows. We can do this by going to search bar and search "Edit environment variables for your account"


## Choose Path Section and Click Edit

Once opened you will see User Variables and System Variables, choose User Variables and in Variable section find **"Path"** Usually its below OneDrive and Upward TEMP. Click/Highlight that and click edit button below.

## On New Line, paste the file path

On the new line, paste the folder path/directory. It should be working from here now.

## Verify it by running CMD

Go to/open your CMD and run this command:

```

php --version


```

The result should be like this

```

PHP 8.4.7 (cli) (built: May  6 2025 14:12:45) (ZTS Visual C++ 2022 x64)
Copyright (c) The PHP Group
Zend Engine v4.4.7, Copyright (c) Zend Technologies

```

If you got this then PHP is successfully installed.