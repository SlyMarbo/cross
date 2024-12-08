# cross

This is a fairly minimal reproduction of (what seems to be) a rules_go issue.

The repo was produced as follows:

```
$ mkdir -p vendor/golang.org/x
$ cd vendor/golang.org/x/
$ git clone https://go.googlesource.com/sys
$ rm -rf .* C* L* P* R* co* go*    # Delete files
$ rm -rf cpu execabs plan9 windows # Delete other packages
$ # Write basic WORKSPACE and MODULE.bazel
$ # Run Gazelle to generate a working BUILD.bazel for golang.org/x/sys/unix
$ # Edit the BUILD.bazel to add an alternative build target
$ # Write a basic main.go and add build targets to the top level BUILD.bazel
```
