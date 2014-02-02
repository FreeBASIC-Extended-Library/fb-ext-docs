## Basic Requirements

*   FreeBASIC Compiler version 0.24 or higher
*   GNU Make

## Windows:

The recommended (and only supported) build method on Windows is using the MinGW Environment that provides a unix-like shell and build tools. You can get the latest version on the [mingw-get download page](http://sourceforge.net/projects/mingw/files/Installer/mingw-get-inst/). You will also need to add the FreeBASIC compiler directory to the path so you don't have to provide the complete path to fbc.exe each time. If you are unsure how to modify the path [here is a great article showing how to modify the path](http://www.computerhope.com/issues/ch000549.htm) on [Windows 7/Vista](http://www.computerhope.com/issues/ch000549.htm#0) and [XP/2000](http://www.computerhope.com/issues/ch000549.htm#1). Once that is complete you can open the MinGW shell from Start &gt; All Programs &gt; MinGW &gt; MinGW Shell.

## Linux:

Beyond the [standard compiler requirements](http://www.freebasic.net/wiki/wikka.php?wakka=CompilerRequirements), you will also need the development headers for Freetype, libjpeg, libgif, sqlite3 and zlib.

<!-- Part two -->

To get the latest source you will be using Git, the distributed version control system. Linux users can install the git package. Windows users have several choices depending on how comfortable you are with Git. We recommend [this excellent git guide](http://rogerdudler.github.io/git-guide/) for all users.

If you are using a graphical client then the URL you want to clone is:

<pre><span>https://github.com/FreeBASIC-Extended-Library/fb-ext-lib.git</span></pre>

<span>If you are using the command line you would use the command:</span>

<pre><span><span>git clone https://github.com/FreeBASIC-Extended-Library/fb-ext-lib.git ext</span>
</span></pre>

Once the download is complete you will have the latest source code in the ext directory (or where ever you saved it.) If you want to check for updates then you will use the pull and update commands, e.g.:

<pre>git pull</pre>
<pre>git checkout master</pre>
<!-- Part three -->

To compile a development version, with debugging symbols included, you will just need to issue the command:

<pre>make &amp;&amp; make MT=1</pre>

If you would like to compile a release version without the debugging symbols you will need to use:

<pre>make NDEBUG=1 &amp;&amp; make MT=1 NDEBUG=1</pre>

Remember if you had previously built a different type of build (developement or release) you will need to clean up the files so that you get what you want. You do this with the command:

<pre>make clean-all</pre>

You can also run the included test suite (very useful if you have made changes) by running:

<pre>make tests</pre>

And if you want to generate the API documentation you would use:

<pre>cd docs &amp;&amp; make docs NATURALDOCS_DIR=/path/to/naturaldocs/directory</pre>

Note that you will need to have NaturalDocs installed to build the documentation. The NATURALDOCS_DIR option is required and points to the directory where NaturalDocs is located, not to the program itself.

Other options recognized by make:

*   <tt>PROFILE=1</tt>&nbsp;Builds a version of the library with profiling information included
*   <tt>EXX=1</tt>&nbsp;Builds the library with null pointer and array out of bounds checking included, also uses the built-in memory leak detector.
*   <tt>OPT="pass to fbc"</tt>&nbsp;Passes other parameters to fbc, i.e. -w pedantic (-w all is used by default)
*   <tt>install</tt>&nbsp;Will install the library files to the default location depending on platform.
*   <tt>INSTALLDIR=/path/to/freebasic</tt>&nbsp;Overrides the location to install to.

## Installing

Installation is very simple and can be done with make as well. To install using make use the command:

make install INSTALLDIR=/path/to/freebasic

You can also use your file manager of choice to copy the ext directory located in inc to your freebasic/inc directory and then the lib/platform files to the freebasic/lib/platform directory.
