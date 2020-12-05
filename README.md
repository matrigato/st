matrigato's build of st
============================

st - simple terminal
--------------------
[st](https://st.suckless.org/) is a simple terminal emulator for X which sucks less.

Patches
-------
The following patches were applied:

- [alpha](https://st.suckless.org/patches/alpha/)

To manually apply a patch, run:

	patch -p1 < path/to/patch.diff

To revert it, add the -R option:

	patch -p1 -R < path/to/patch.diff

Remember that patches only modify config.def.h, so you will need to manually replace/delete/update config.h before compiling.

Sometimes, after multiple patches, patching may fail and will require manual intervention. In that case, manually apply the unsuccessful modifications found in a newly generated file ending in a .rej extension.

Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

	make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

	tic -sx st.info

See the man page for additional details.

Configuration
-------------
The configuration of st is done by creating a custom config.h
and (re)compiling the source code.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

License
-------
In jurisdictions that recognize copyright laws, the following licenses apply:

[st](https://git.suckless.org/st/) is available under the [MIT/X Consortium License](LICENSES/MIT).

Everything made by me is under [The Unlicense](LICENSES/UNLICENSE).

For patches, refer to their individual pages linked above for details.