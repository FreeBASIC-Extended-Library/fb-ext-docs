The logging module is meant to be a very simple log that is also
very capable. For basic usage absolutely no configuration is needed,
just start using the DEBUG, INFO, WARN or FATAL logging macros.

[API Documentation](http://ext.freebasic.net/dev-docs/files/ext/log-bi.html)

There are built-in log destinations for printing to the screen,
logging to a file (plaintext or XML), or you can create your own method
if you require something more advanced.

## Simple example

[gist:8776078]

## Multithreading notes

When using this module in a multithreaded environment all logging
happens asynchronously in a single background thread. This uses the
CommChannel provided by the threading module.
