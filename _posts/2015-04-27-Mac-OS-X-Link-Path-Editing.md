---
layout: post
title: Mac OS X Link Path Editing
---

Dynamically linked libraries sometimes go missing under Mac OS X.
Maybe you updated that old library you compiled against a year ago and you do not feel like recompiling your code right now
or maybe you got this executable from a trusted source, but your system doesn't find the library at path `/Users/iusedstaticpaths/lib.dylib`.

Regardless, there is a solution: `install_name_tool`.

First, check the library dependencies of your executable or dynamic library (`-D`) with:
`otool -L /path/to/my/runtime`

Then, call `install_name_tool` to replace any path you want:

`install_name_tool -change "/path/to/unknown/lib.0.0.dylib" lib.dylib runtime`

In this example I also removed the version numbering, which is not always recommended, but will commonly work if your lib hasn't undergone significant API changes.

Lastly, if your dynamic library still can't be found,  make sure it is inside the `DYLD_LIBRARY_PATH` or maybe `DYLD_FALLBACK_LIBRARY_PATH`.
For more options please read `man install_name_tool`.
