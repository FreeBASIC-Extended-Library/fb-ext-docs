[API Documentation](http://ext.freebasic.net/dev-docs/files/ext/config-bi.html)

* File to include: `ext/config.bi`

This module provides a way to configure your program easily using
the standard locations on each platform.  You do not need to distribute
a config file either, as it will be generated the first time you run
your application provided you set you default values in the getType
calls.  This configuration file is saved in somewhat human-readable
XML for advanced users to modify if they wish to do so at a standard location.

The Standard locations for each platform are:

* __Windows__ %APPDATA%\appname\config.xml
* __Linux__ $HOME/.config/appname/config.xml
* __DOS__ EXEPATH/appname.cfg

The configuration file is treated as a name-value store.
Each named item can consist of a Boolean value, integer or double value
and a String value.  If you wish to have more than one, you should make
sure that you call getString first so the name is properly created.
Also, please note that integers and doubles are stored in the same
location in name and will overwrite each other.

You should generally call the get* functions (with a default value)
and only call the set* functions if you need to change something after
loading the configuration, i.e. the user changes something or you are
saving a new window position at exit.

You must ensure that you call setAppName before calling load else your
application will have the default name of “UnnamedApp”.
