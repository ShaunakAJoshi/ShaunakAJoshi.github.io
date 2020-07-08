---
layout: post
title: AutoMoodle
permalink: /projects/automoodle/
---
**What it is**: At IIT Bombay, all instructors share files and resources on a platform called Moodle. Each course has a dedicated page which contains a discussion forum and the uploaded resources.

**What’s wrong**: Downloading these files is a tedious job as it involves the following steps:

* Log in using LDAP credentials
* Navigate to each course page
* Click download on *every* file you want. No option for batch downloads!

**The solution**: I wrote a Python script which uses the popular web-testing tool Selenium to automatically login using the LDAP credentials which are stored in a config file. It also contains the list of courses which need to be tracked. The user has the freedom to choose these courses. Then, the script scrapes the portal for all the course pages and downloads the posted resources in the specified location. Needless to say, it keeps track of previously downloaded resources to avoid downloading them again.

You can find the GitHub repo [here](https://github.com/methi1999/autoMoodle.git).

(Update: The script no longer works due to changes to Moodle.)