# tabbed - generic tabbed interface
=================================
tabbed is a simple tabbed X window container.

# patches
---------

Patches added are in the patches directory:

+icon patch
+hidetabs patch
+keyrelease patch(for showing tabs. Pres ctrl-shift to see the tabs)

## Requirements
------------
In order to build tabbed you need the Xlib header files.

## Installation
------------
clone and `sudo make install` or add my repository with my builds of packages in https://github.com/ashincoder/ashin-repo and `pacman -Sy tabbed-ashin`

## Editing
-------
You can edit the file from `/opt/tabbed-ashin-git/config.def.h`

Patches used are hidetabs and icons

## Running tabbed
--------------
Running tabbed with surf :
    `tabbed surf-e`
Running tabbed with st :
    `tabbed -r 2 st -w ''`

press Ctrl+Shift+Enter to open another tab in surf or st

See the man page for details.

