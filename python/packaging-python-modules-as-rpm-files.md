To package a Python module as an RPM with needed RPM dependencies, add this to
your `setup.cfg`:

```
[bdist_rpm]
provides = python3-dnspython
requires = python3
    python3-requests
    python3-requests-toolbelt
packager = UMIACS Staff
```
