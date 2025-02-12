# variables and functions provided by ezpkg for ezbuild
## `$pkg`
package name
## `$ver`
package version
## `$ezbuild`
absolute path of the ezbuild file
## `$pkgworkdir`
absolute path of the per-package working directory(e.g. `$workdir/$pkg-$ver`)
## `$src_root`
absolute path of the primary source directory(e.g. `$pkgworkdir/src/$pkg-$ver`)  
if the default value is not correct, ezbuild can fix it
## `inherit()` `$1=libname ...`
find and source ezlibs from repositories
## `panic()` `$@=message`
exit ezpkg with message

# variables ezbuild should provide
## `$src`(optional)
array of urls to download  
currently supports git and http(s)
## `$git_${name}_commit`(optional)
commit hash or tag name or branch name of the `${name}` repository in `${src}`
## `$patches`(optional)
array of path of patches to apply  
each filename will be concatenated to the dirname of the ezbuild file  
these patches are applied to `${src_root}`
## `pkg_patch()`(optional)
called after unpacking sources to apply complex patches
## `pkg_configure()`(optional)
called to run `./configure` like scripts  
be careful to respect `$prefix` variables set in config
## `pkg_build()`(optional)
called to run `make` like scripts  
be careful to respect `$makeargs` variables set in config
## `pkg_install()`(optional)
called to run `make install` like scripts  
be careful to respect `$destdir` variables set by ezpkg
