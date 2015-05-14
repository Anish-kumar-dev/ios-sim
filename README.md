ios-sim
=======

Supports Xcode 6 only since version 3.x.

The ios-sim tool is a command-line utility that launches an iOS application on
the iOS Simulator. This allows for niceties such as automated testing without
having to open Xcode.

Features
--------

* Choose the device family to simulate, i.e. iPhone or iPad. Run using "showdevicetypes" option to see available device types, and pass it in as the "devicetypeid" parameter.
* Setup environment variables.
* Pass arguments to the application.
* See the stdout and stderr, or redirect them to files.

See the `--help` option for more info.

Usage
-----

```
Usage: ios-sim <command> <options> [--args ...]

Commands:
  showsdks                        List the available iOS SDK versions
  showdevicetypes                 List the available device types
  launch <application path>       Launch the application at the specified path on the iOS Simulator
  start                           Launch iOS Simulator without an app

Options:
  --version                       Print the version of ios-sim
  --help                          Show this help text
  --verbose                       Set the output level to verbose
  --exit                          Exit after startup
  --env <environment file path>   A plist file containing environment key-value pairs that should be set
  --setenv NAME=VALUE             Set an environment variable
  --log <log file path>           The path where log of the app running in the Simulator will be redirected to
  --timeout <seconds>             The timeout time to wait for a response from the Simulator. Default value: 30 seconds
  --args <...>                    All following arguments will be passed on to the application
  --devicetypeid <device type>    The id of the device type that should be simulated (Xcode6+). Use 'showdevicetypes' to list devices.
                                  e.g "com.apple.CoreSimulator.SimDeviceType.Resizable-iPhone6, 8.0"
```

Installation
------------

With node.js (at least 0.10.20):

    $ npm install ios-sim -g

Download an archive:

    $ curl -L https://github.com/phonegap/ios-sim/zipball/3.0.0 -o ios-sim-3.0.0.zip
    $ unzip ios-sim-3.0.0.zip

Or from a git clone:

    $ git clone git://github.com/phonegap/ios-sim.git


Troubleshooting
------------

Make sure you enable Developer Mode on your machine:
    
    $ DevToolsSecurity -enable

Make sure multiple instances of launchd_sim are not running:
    
    $ killall launchd_sim
    
License
-------

This project is available under the MIT license. See [LICENSE][license].

[license]: https://github.com/phonegap/ios-sim/blob/master/LICENSE
