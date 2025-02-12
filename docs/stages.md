# stages
## fetch
download or clone source files
## unpack
unpack or copy fetched files to per-package work directory  
also apply patches
## configure
run `pkg_configure`
## build
run `pkg_build`
## install
run `pkg_install`, install files into the temporary image
## merge
merge installed image to system
## cleanup
remove work directory(not implemented)
