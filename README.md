# ccfancybuild

[ccsimplebuild](https://github.com/FarFetchd/ccsimplebuild) with an extra
feature hacked on: the ability to depend on and compile source files outside of
the main source directory (see sample2 and sample3). If you don't need
that - and you hopefully shouldn't - use ccsimplebuild instead.

ccfancybuild expects to be run in a directory full of .cc and .h files (must
use those suffixes, not cpp/hpp/etc). ccfancybuild will create a subdir named
"obj/", where it will make a .o for every .cc file.

To use, you can either:

* Run `ccfancybuild` with a file named default.ccbuildfile existing in that same
  directory. See the sample directories for buildfile examples.
* Run `ccfancybuild mycustombuildfilename` to load a buildfile named
  mycustombuildfilename, rather than default.ccbuildfile.

Suggested compilation command:
`g++ -std=c++17 ccfancybuild.cc -o ccfancybuild && sudo cp ccfancybuild /usr/local/bin/`
