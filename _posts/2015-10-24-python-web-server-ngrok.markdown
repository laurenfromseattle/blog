---
layout: post
title:  "Running a Local Server with Python and Accessing It Remotely with ngrok (Windows)"
date:   2015-10-24 14:33:40
categories: python ngrok
---
Looking to set up a web server on the fly? The **Python** SimpleHTTPServer is just as it sounds: simple to set up, simple to use. SimpleHTTPServer allows you to turn any directory on your local machine into a web server directory. Used in combination with **ngrok**, you can then access this local server remotely. How cool!

## Setting up SimpleHTTPServer

Here are the steps I took to set up a local web server with Python on my Windows machine.

1. Download and install Python (version 2.7.x)

    <https://www.python.org/downloads/>

2. Add Python to the System Path Variable.
    * Start
    * Right-click on Computer
    * Select Properties
    * Select Advanced System Settings
    * Under Advanced tab, select Environment Variables button
    * Under System variables, append (Edit) `C:\Python27` to end of Path variable.
    * Select OK for everything.

3. Now open PowerShell and make sure everything is working right by typing **>** `python`. It should show you something like this:

    <div>
    <code class="code-block-in-list"><pre>
    Windows PowerShell
    Copyright (C) 2009 Microsoft Corporation. All rights reserved.

    PS C:\Users\LT> python
    Python 2.7.10 (default, May 23 2015, 09:40:32) [MSC v.1500 32 bit (Intel)] on win32
    Type "help", "copyright", "credits" or "license" for more information.
    >>></code></pre>
    </div>

4. Type **>** `quit()` to get back to command prompt.

5. Navigate to the directory with your project and run the following command:

    `python -m SimpleHTTPServer 8080`

    <div>
    <code class="code-block-in-list"><pre>
    Windows PowerShell
    Copyright (C) 2009 Microsoft Corporation. All rights reserved.

    PS C:\Users\LT> cd d:/fend/blog
    PS D:\fend\blog> python -m SimpleHTTPServer 8080
    Serving HTTP on 0.0.0.0 port 8080 ...</code></pre>
    </div>

6. Now open your browser and navigate to `localhost:8080`. Voila! You should see your site!

## Setting up ngrok to access local server remotely

Now what if we want to view our site remotely, let's say from a mobile phone? That's where **ngrok** comes in. ngrok creates a secure public URL to a local webserver on your machine. Here are the steps to set that up.

1. Download ngrok and unzip

    <https://ngrok.com/download>

2. Open a new PowerShell window, navigate to ngrok directory, and run ngrok, selecting the same port as your local server:

    **>** `cd c:/ngrok`

    **>** `./ngrok http 8080`

    You should see something like this:

    <div>
    <code class="code-block-in-list"><pre>
    ngrok by @inconshreveable

    Tunnel Status                 online
    Version                       2.0.19/2.0.19
    Web Interface                 http://127.0.0.1:4040
    Forwarding                    http://479d339d.ngrok.io -> localhost:8080
    Forwarding                    https://479d339d.ngrok.io -> localhost:8080

    Connections                   ttl     opn     rt1     rt5     p50     p90
                                  0       0       0.00    0.00    0.00    0.00</pre></code>
    </div>

3. Now you can use the forwarding URL provided to access the site locally! If you would like to inspect the GET requests and things of that nature, navigate your browser to `localhost:4040`.

---

*This is my first blog post using Jekyll! I am currently a student of Udacity's Front-End Web Development Nanodegree program. I plan to keep track of my progress through the program by taking daily notes in this blog.*

*I am new to coding -- a noob! -- so I don't expect these notes to be terribly helpful to fellow coders. There also isn't going to be much in the way of logical organization, simply because every concept I encounter will be brand new and worth writing about!*

*Just thinking about new things I learned today is overwhelming: Jekyll, markdown, SimpleHTTPServer, ngrok... Every day I make another scratch on the surface of something I have not yet begun to understand.*
