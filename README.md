# Simple package manaager for CMake 3.11 and above

This is a simple extension around CMake 3.11's FetchContent module.

For details related to FetchContent check https://cmake.org/cmake/help/latest/module/FetchContent.html.

Additions to FetchContent are as follows:
 - Warns if a different version of an external project has been added beforehand.
 - Optionally calls `add_subdirectory` with `EXCLUDE_FROM_ALL` if the external project root contains a `CMakeLists.txt` file and `SKIP_ADD_SUBDIR` has not been added as an argument.
 - Arguments to subdirectories can be passed as a `<key>=<value>` list, and policies can be passed similarly as `<policy id>=<NEW|OLD>`.
