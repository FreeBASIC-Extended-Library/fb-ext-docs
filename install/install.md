<style type="text/css">
code {
  padding: 5px;
  border: 2px;
  border-style: solid;
  background-color: #c9c9c9;
}
</style>

# All Platforms

1.  [Optional] Download the HTML documentation.

# Windows

1.  Extract the downloaded package and open the resulting folder.
2.  Open a second Explorer window and navigate to your FreeBASIC installation directory, typically C:\FreeBASIC
3.  Copy the **lib** directory from the Ext package window and paste it into the FreeBASIC window, merging the folders.
4.  Copy the **inc** directory from the Ext package window and paste it into the FreeBASIC window, merging the folders.
5.  Keep a copy of the **bin** directory from the Ext package as you may need it's contents for your projects.

# Linux

You will need to [compile from source](http://ext.freebasic.net/user-guide/compiling-from-source).

1.  To make a debug ready version:

    `make && make MT=1 && make install`

2.  To make a release ready version:

    `make NDEBUG=1 && make NDEBUG=1 MT=1 && make install`

# DOS

The instructions are being worked on. At the time of writing the Developers do not have access to a working DOS build environment.
