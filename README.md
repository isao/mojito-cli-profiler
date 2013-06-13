# mojito-cli-profiler
<!-- [![Build Status](https://travis-ci.org/yahoo/mojito-cli-profiler.png)](https://travis-ci.org/yahoo/mojito-cli-profiler) -->

This package provides the `profiler` command for the [`mojito-cli`](https://github.com/yahoo/mojito-cli) tool. To install:

    npm install -g mojito-cli
    npm install -g mojito-cli-profiler

Note that this relies on the environment variable `$NODE_PATH` to include the path returned with `npm root -g`.

## Set Up

Your app's application.json file should have a perf config object, like:

    "perf": {
        "timeline": true,
        "mark": true
    },

You can also specify the output pathname in this config object like `"logFile": "/tmp/perf.log",`

Start your mojito application like

    mojito start --perf <logfilename>

Make server requests, then hit `ctrl-C`.

## Usage

After the preparation described above, there should be file created by the name provided above. To generate the perfomrance graph, you can now do:

    mojito profiler --input <logfilename>


Licensing and Contributions
---------------------------
This software is free to use under the Yahoo! Inc. BSD license. See LICENSE.txt.
