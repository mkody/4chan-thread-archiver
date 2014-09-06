threaddl
========

Archive complete threads with images with a truncated 4chanX injected and
more features for more comfortable browsing of the threads.

Notes
-----

* Works on Android with the proper GNU tools (use Google to find these).
    **Please edit** the interpreter in the first line before using it on Android!
* This fork may not correctly work for you, since I'm using it at a `4chan` subdirectory from webroot AND I've put an another *gallery* viewer in this folder first. You can see how it looks for me [HERE](http://up.kdy.ch/4chan/) (Note: old threads were made by an another script)
* The script saves the thread to the current location of the console. So be at the /4chan/ website subfolder
* HTTPS protocol is ignored, HTTP is used for everything
* The thread's HTML is cleaned up of everything not necessary, which
    results in a very small filesize
* Deleted posts aren't prereserved, but if you started archiving the
    thread before the deletion of the post/image, the image will most
    likely be saved (if you find a way to preserve posts as well,
    post an issue or pull request to contact me)

Dependencies
------------

* Basic GNU tools
* sed
* wget
* Linux, Windows with cygwin (not tested on Mac)

Warning
--------

4chan has some nasty and/or illegal images. All images in a thread will
be downloaded! Images from ads are not downloaded. Author(s) shall not be
liable for any legal action result from use of this software. If you are
unsure if a thread will contain illegal images, use tmpfs. Keep that stuff
off your computer.

Copying
-------

Whatever

Archiving
---------

    ./threaddl.sh [4chan thread URL] <time value and/or thread name>

4chan thread URL: something like
https://boards.4chan.org/vg/thread/30100764#p30100764
or
http://boards.4chan.org/c/thread/2012645
or even
https://boards.4chan.org/vg/thread/69229732/tera-general-terag


**time value:**
* 1 -> Download once
* 10 - 999 -> Interval in seconds between fetches

**thread name:**
* Set the thread name to add to the end of the URL
* Default: none

Archive Layout
--------------

    <number of OP post>.html: the thread
    <board name>-<number of OP post>_<name of thread if provided>/: contains full resolution images
    misc/: contains thumbnails, css, logo image, gallery, misc stuff
