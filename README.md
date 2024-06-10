xcodebuild-scripts
==================

A collection of scripts for xcodebuild.


Installation
------------

### Prerequisites

- [jq](https://jqlang.github.io/jq/)
- [xcpretty](https://github.com/xcpretty/xcpretty)


### Installation Steps

```console
$ cd path/to/your/project
$ mkdir -p Scripts
$ git submodule add https://github.com/Kuniwak/xcodebuild-scripts ./Scripts/xcodebuild-scripts
$ ./Scripts/xcodebuild-scripts/test 'iOS-17-' 'iPhone '
```


Usage
-----

### Test

```console
$ ./test -h
usage: test [<options>] <scheme> <os> <device>

Run tests on the specified devices

OPTIONS
        -h, --help    print this usage

EXAMPLES
        $ ./test 'iOS-17-' 'iPhone SE'
```


### List Devices

```console
$ ./list-devices -h
usage: list-devices [<options>]

List device informations.

OPTIONS
        -h, --help    print this usage

EXAMPLE
        $ ./list-devices
        iOS-17-2        iPhone SE (3rd generation)      E52F4060-8786-4122-94B3-87C81DEDB0AA    Shutdown
        ...
```


### Select Device

```console
$ ./select-device -h
usage: select-device [<options>] <os> <device>

Write UDID that matches the specified OS and Device name

OPTIONS
        -h, --help    print this usage

EXAMPLE
        $ ./select-device iOS-17- iPhone
        846C496B-0320-497C-BF3C-1B80E9C3A474
        ...
```


License
-------

[MIT License](./LICENSE)