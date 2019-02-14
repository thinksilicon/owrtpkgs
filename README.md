# OpenWRT packages by Thinksilicon

Collection of packages missing in OpenWRT repositories.

## Image::Scale for openwrt

This will build the fast, high-quality fixed-point image resizing for openwrt platforms.
It depends on the packages/lang/perl repository and needs libjpeg and libpng.

Currently I don't know how to properly set the include-directories. If the build fails
set the correct directory in the .patch-file.


## forks for openwrt

drop-in replacement for Perl threads using fork(). Comes with all dependencies:

Exporter::Tiny, List::MoreUtils, Sys::SigAction, Acme::Damn, Time::HiRes, ...


## cu for openwrt

cu is part of the UUCP source but has been split into its own package because it can be useful even if you do not use uucp. 
