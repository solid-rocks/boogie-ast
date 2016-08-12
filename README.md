
Installing Boogie on Linux is not a piece of cake.
Boogie requires older version of Z3 (4.1.1). You may require a patch to
successfully build it.

```
$ git clone https://github.com/Z3Prover/z3
$ cd z3 ; git checkout z3-4.1.1
$ curl https://raw.githubusercontent.com/solid-rocks/boogie-ast/master/0001-fix-z3-build.patch | git apply -
$ autoconf && ./configure && make
$ cd -
```

Install prerequisites and build Boogie:

```
$ sudo apt-get install mono-complete mono-reference-assemblies-4.0
$ git clone https://github.com/boogie-org/boogie
$ cd boogie
$ wget https://nuget.org/nuget.exe
$ mono ./nuget.exe restore Source/Boogie.sln
# ln -s ../z3/bin/external/z3 Binaries/z3.exe
```


TODO
----

  - try CVC4
