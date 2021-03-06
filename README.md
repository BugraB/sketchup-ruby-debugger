SketchUp Ruby API Debugger
==========================

This is a Ruby debugger framework for SketchUp 2014 and later. We currently support Windows only but Mac OS X support will be added soon. The ruby-debug-ide protocol has been mostly implemented so any Ruby IDE that supports this protocol should work. We have tested with Aptana RadRails, NetBeans (with Ruby community plugin) and RubyMine.

Setup instructions:
- The repository contains a pre-built dynamic library (SURubyDebugger.dll for Windows). Copy this DLL into the SketchUp installation folder:
```
C:\Program Files (x86)\SketchUp\SketchUp 2014\
```
- Run SketchUp with the following command line arguments:
```
SketchUp.exe -rdebug "ide port=7000"
```
- The port should match the remote debugger port setting configured in the IDE. Default port is 1234.
- SketchUp will start up and appear to be frozen. It is waiting for the debugger to show up.
- Launch remote debugging in the IDE, SketchUp should continue running. You should see breakpoints hit when Ruby code execution reaches the specified lines.

Most common debugging functionality has been implemented but there are few TODOs:
- Debugging of multi-threaded execution
- Exception breakpoints
- Conditional breakpoints
- What else are we missing ? Please report and contribute!

To contribute, please fork the repository, make your changes and submit a pull request.

Happy Debugging!
