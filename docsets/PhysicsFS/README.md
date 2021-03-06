# PhysicsFS 3.0.2 docset

[PhysicsFS](https://www.icculus.org/physfs/) (v3.0.2) docset for [Dash](http://kapeli.com/dash).

This docset has been generated by [superzazu](https://github.com/superzazu).

# How to build

1. Download [PhysicsFS](https://www.icculus.org/physfs/downloads/physfs-3.0.2.tar.bz2)
2. Go to `docs` and update `Doxyfile` with those values:

```
DISABLE_INDEX     = YES
SEARCHENGINE      = NO
GENERATE_TREEVIEW = NO
FULL_PATH_NAMES   = NO
# The following should be appended at the end of the file:
GENERATE_DOCSET = YES
DOCSET_FEEDNAME = "PhysicsFS"
DOCSET_BUNDLE_ID = physfs
```

3. Run `mkdir build && cd build && cmake .. && make docs` to generate docs.
4. Run `cd docs/html && make` to generate the docset file.
5. Replace `Info.plist` with those values:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>CFBundleIdentifier</key>
    <string>physfs</string>
    <key>CFBundleName</key>
    <string>PhysicsFS</string>
    <key>DocSetPlatformFamily</key>
    <string>physfs</string>
    <key>DashDocSetFamily</key>
    <string>doxy</string>
</dict>
</plist>
```
