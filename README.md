# Z3 Rise4Fun

Z3 tutorials from the rise4fun website.

Known problems:
- Non smtlib commands don't work. Probably because of the function we're using to call z3 being a stock smtlib function.
- On main thread, so a tough Z3 query can make the tab unusable. I think there is a emscripten flag for this
- I can't find copies of some of the smtlib commands that do not appear to be on the archive.org site.

Notes: 
- I made some edits to the build script in particular to include pthreads to make z3 work.
- https://github.com/gzuidhof/coi-serviceworker was very helpful for fixing SharedBufferArray problems
- I copy and pasted the source of the archive versions of rise4fun. I made some janky helper scripts in helper.js to traverse these pages and replace the old interactive pieces driven by `<a>` tags to ones that use `<textarea>` and `<buttons>`. I made some other small updates. Rise4fun was using a very old version of z3?
- Github discussion of rise4fun being down: <https://github.com/Z3Prover/z3/discussions/5473>





==========

Z3 WASM
=========

This repository contains scripts that makes interaction
with the Z3 solver from a browser using WASM easier.

* `build.sh` contains commands to fetch and compile Z3 using emscripten.
* `api/` contains a C API which exposes the Z3 API to Javascript, and 
  the `api.js` file contains some glue code that enables easier interaction
  with the C API.
* `example/` contains an example of how to use the `api.c` module using a dynamically linked native version of the Z3 library, this cannot be used from the browser.
* `index.html` contains an example on how to load and use the Z3 Javascript glue code.

Both the location of the Z3 repository and the Z3 version can be controlled
using environment variables. `Z3_BASE_DIR` controls the location of the 
cloned Z3 repository, while `Z3_VERSION` alters the version that is 
fetched from Github.

## Related repositories

Clément Pit-Claudel has performed similar steps as I have taken here. 
However, its scripts are meant to be used on Ubuntu or Debian derivates, 
and do not work nicely on other distributions of Linux. Furthermore, its
Z3 version is outdated, and numerous users have reported either compilation
issues or issues while using the library.

There are many Z3 in browser projects.

- <https://github.com/cpitclaudel/z3.wasm>
- <https://github.com/Z3Prover/z3/issues/1298>
- <https://github.com/babelsberg/z3.js>
- <https://github.com/sim642/z3em>
- <https://github.com/mjyc/z3js>
- <https://github.com/stahlbauer/z3.ts>


