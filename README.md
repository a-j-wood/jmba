Project has left GitHub
-----------------------

It is now here: [https://codeberg.org/a-j-wood/jmba](https://codeberg.org/a-j-wood/jmba)

This project was briefly hosted on GitHub.  GitHub is a proprietary,
trade-secret system that is not Free and Open Source Software (FOSS).

Read about the [Give up GitHub](https://GiveUpGitHub.org) campaign from
[the Software Freedom Conservancy](https://sfconservancy.org) to understand
some of the reasons why GitHub is not a good place to host FOSS projects.

Any use of this project's code by GitHub Copilot, past or present, is done
without permission.  The project owner does not consent to GitHub's use of
this project's code in Copilot.

![Logo of the GiveUpGitHub campaign](https://sfconservancy.org/img/GiveUpGitHub.png)


Introduction
------------

This is the README for "jmba", a junk mail buffering agent.  This program is
designed to queue email until the sender's email address has been verified,
at which point the original email is delivered.

JMBA is designed to be used in conjunction with a spam filter such as QSF
(http://www.ivarch.com/programs/qsf.shtml).  When the spam filter says it
thinks an email is spam, it can be passed to JMBA.  JMBA will queue it and
send an email to the sender containing a key; if the sender replies, the
original email is "unfrozen" from the queue and delivered.

Of course this assumes that senders of spam won't reply to their email. 
This is a fair assumption since at the moment the vast majority of spam is
sent with a forged (invalid) envelope sender, so replying direct to the
sender won't work and therefore JMBA will never receive a response to its
"please verify" message.


Requirements
------------

You will need "`procmail`" installed to use this package.  "`qsf`" is
recommended.


Documentation
-------------

A manual page is included in this distribution.  If you prefer plain text,
then look at "doc/quickref.txt" for a text version.


Compilation
-----------

To compile the package, type "`sh ./configure`", which should generate a
Makefile for your system.  You may then type "`make`" to build everything.

See the file "doc/INSTALL" for more about the "configure" script.

Developers note that you can do "`./configure --enable-debugging`" to cause
debugging support to be built in.  Also note that doing "`make index`" will
generate an HTML code index (using "`ctags`" and "`cproto`"); this index lists
all files used, all functions defined, and all TODOs marked in the code.


Author
------

This package is copyright (C) 2005 Andrew Wood, and is being distributed
under the terms of the Artistic License and other licenses.  For more
details, see the file "doc/COPYING".

You can contact me by using the contact form on my web page at
http://www.ivarch.com/.

The "jmba" home page is at:

  http://www.ivarch.com/programs/jmba.shtml

The latest version can always be found here.

Credit is also due to:

 * Ondrej Suchy - provided Czech (cs_CZ) translation
 * Nick Rosier - suggested logging

-----------------------------------------------------------------------------
