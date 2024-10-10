# python-armv7

This works:
```
bazel build //:main
```
This does not work:
```
bazel build --config=foo //:main
```
With the error:
```
Target '//:main' depends on toolchain '@@[unknown repo 'python_3_11_armv7-unknown-linux-gnu' requested from @@rules_python~~python~pythons_hub]//:python_runtimes', which cannot be found: no such package '@@[unknown repo 'python_3_11_armv7-unknown-linux-gnu' requested from @@rules_python~~python~pythons_hub]//': The repository '@@[unknown repo 'python_3_11_armv7-unknown-linux-gnu' requested from @@rules_python~~python~pythons_hub]' could not be resolved: No repository visible as '@python_3_11_armv7-unknown-linux-gnu' from repository '@@rules_python~~python~pythons_hub''
```
