~/dev
❯ cd esp8266/
❯ git clone https://github.com/MabezDev/rust-xtensa
Cloning into 'rust-xtensa'...
remote: Enumerating objects: 1406798, done.
remote: Total 1406798 (delta 0), reused 0 (delta 0), pack-reused 1406798
Receiving objects: 100% (1406798/1406798), 649.00 MiB | 3.22 MiB/s, done.
Resolving deltas: 100% (1132878/1132878), done.
Updating files: 100% (26818/26818), done.

~/dev/esp8266 took 4m15s
❯ cd rust-xtensa/

rust-xtensa on  xtensa-target via 🦀 v1.48.0
❯ ./configure --experimental-targets=Xtens
configure: processing command line
configure:
configure: llvm.experimental-targets := Xtens
configure: build.configure-args := ['--experimental-targets=Xtens']
configure:
configure: writing `config.toml` in current directory
configure:
configure: run `python /home/rajput/dev/esp8266/rust-xtensa/x.py --help`
configure:

rust-xtensa on  xtensa-target via 🦀 v1.48.0
❯ ./x.py build
/usr/bin/env: ‘python’: No such file or directory

rust-xtensa on  xtensa-target via 🦀 v1.48.0
❯ sudo apt install python
Reading package lists... Done
Building dependency tree
Reading state information... Done
Note, selecting 'python-is-python2' instead of 'python'
The following NEW packages will be installed:
  python-is-python2
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 2496 B of archives.
After this operation, 10.2 kB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu focal/universe amd64 python-is-python2 all 2.7.17-4 [2496 B]
Fetched 2496 B in 1s (3298 B/s)
Selecting previously unselected package python-is-python2.
(Reading database ... 84280 files and directories currently installed.)
Preparing to unpack .../python-is-python2_2.7.17-4_all.deb ...
Unpacking python-is-python2 (2.7.17-4) ...
Setting up python-is-python2 (2.7.17-4) ...

rust-xtensa on  xtensa-target via 🐍 v2.7.18 via 🦀 v1.48.0 took 3s
❯ ./x.py build
Updating only changed submodules
Updating submodule src/tools/rust-installer
Submodule 'src/rust-installer' (https://github.com/rust-lang/rust-installer.git) registered for path 'src/tools/rust-installer'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/tools/rust-installer'...
remote: Enumerating objects: 848, done.
remote: Counting objects: 100% (79/79), done.
remote: Compressing objects: 100% (42/42), done.
remote: Total 848 (delta 42), reused 56 (delta 34), pack-reused 769
Receiving objects: 100% (848/848), 262.73 KiB | 2.05 MiB/s, done.
Resolving deltas: 100% (519/519), done.
Submodule path 'src/tools/rust-installer': checked out '5254dbfd25d5284728ab624dca1969d61427a0db'
Updating submodule src/doc/nomicon
Submodule 'src/doc/nomicon' (https://github.com/rust-lang/nomicon.git) registered for path 'src/doc/nomicon'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/doc/nomicon'...
remote: Enumerating objects: 2046, done.
remote: Counting objects: 100% (99/99), done.
remote: Compressing objects: 100% (79/79), done.
remote: Total 2046 (delta 52), reused 36 (delta 20), pack-reused 1947
Receiving objects: 100% (2046/2046), 1.19 MiB | 2.99 MiB/s, done.
Resolving deltas: 100% (1336/1336), done.
Submodule path 'src/doc/nomicon': checked out 'bbf06ad39d1f45654047e9596b750cc6e6d1b693'
Updating submodule src/tools/cargo
Submodule 'src/tools/cargo' (https://github.com/rust-lang/cargo.git) registered for path 'src/tools/cargo'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/tools/cargo'...
remote: Enumerating objects: 82856, done.
remote: Counting objects: 100% (357/357), done.
remote: Compressing objects: 100% (200/200), done.
remote: Total 82856 (delta 172), reused 312 (delta 152), pack-reused 82499
Receiving objects: 100% (82856/82856), 29.14 MiB | 3.18 MiB/s, done.
Resolving deltas: 100% (59719/59719), done.
Submodule path 'src/tools/cargo': checked out '43b129a20fbf1ede0df411396ccf0c024bf34134'
Updating submodule src/doc/reference
Submodule 'src/doc/reference' (https://github.com/rust-lang/reference.git) registered for path 'src/doc/reference'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/doc/reference'...
remote: Enumerating objects: 8425, done.
remote: Counting objects: 100% (167/167), done.
remote: Compressing objects: 100% (134/134), done.
remote: Total 8425 (delta 96), reused 70 (delta 33), pack-reused 8258
Receiving objects: 100% (8425/8425), 3.38 MiB | 3.58 MiB/s, done.
Resolving deltas: 100% (6046/6046), done.
Submodule path 'src/doc/reference': checked out 'f02b09eb6e8af340ad1256a54adb7aae2ff3163e'
Updating submodule src/doc/book
Submodule 'src/doc/book' (https://github.com/rust-lang/book.git) registered for path 'src/doc/book'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/doc/book'...
remote: Enumerating objects: 32401, done.
remote: Total 32401 (delta 0), reused 0 (delta 0), pack-reused 32401
Receiving objects: 100% (32401/32401), 35.33 MiB | 2.02 MiB/s, done.
Resolving deltas: 100% (22687/22687), done.
Submodule path 'src/doc/book': checked out 'e724bd826580ff95df48a8533af7dec1080693d4'
Updating submodule src/tools/rls
Submodule 'src/tools/rls' (https://github.com/rust-lang/rls.git) registered for path 'src/tools/rls'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/tools/rls'...
remote: Enumerating objects: 11507, done.
remote: Counting objects: 100% (89/89), done.
remote: Compressing objects: 100% (58/58), done.
remote: Total 11507 (delta 41), reused 56 (delta 27), pack-reused 11418
Receiving objects: 100% (11507/11507), 8.84 MiB | 6.96 MiB/s, done.
Resolving deltas: 100% (7495/7495), done.
Submodule path 'src/tools/rls': checked out '3bd7215d48ba05f18401cc340ae8d71af002ba6d'
Updating submodule src/tools/rustfmt
Submodule 'src/tools/rustfmt' (https://github.com/rust-lang/rustfmt.git) registered for path 'src/tools/rustfmt'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/tools/rustfmt'...
remote: Enumerating objects: 34689, done.
remote: Counting objects: 100% (110/110), done.
remote: Compressing objects: 100% (65/65), done.
remote: Total 34689 (delta 56), reused 51 (delta 44), pack-reused 34579
Receiving objects: 100% (34689/34689), 12.55 MiB | 6.52 MiB/s, done.
Resolving deltas: 100% (25285/25285), done.
Submodule path 'src/tools/rustfmt': checked out '7de6968ee22696b7feb6b477a05656de89275291'
Updating submodule src/tools/miri
Submodule 'src/tools/miri' (https://github.com/rust-lang/miri.git) registered for path 'src/tools/miri'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/tools/miri'...
remote: Enumerating objects: 27559, done.
remote: Counting objects: 100% (382/382), done.
remote: Compressing objects: 100% (178/178), done.
remote: Total 27559 (delta 197), reused 354 (delta 189), pack-reused 27177
Receiving objects: 100% (27559/27559), 7.12 MiB | 4.26 MiB/s, done.
Resolving deltas: 100% (18533/18533), done.
Submodule path 'src/tools/miri': checked out '4cf36f285084f8f841f3cff7b29d44b1d95ee1dd'
Updating submodule src/doc/rust-by-example
Submodule 'src/doc/rust-by-example' (https://github.com/rust-lang/rust-by-example.git) registered for path 'src/doc/rust-by-example'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/doc/rust-by-example'...
remote: Enumerating objects: 328129, done.
remote: Counting objects: 100% (118/118), done.
remote: Compressing objects: 100% (109/109), done.
remote: Total 328129 (delta 59), reused 12 (delta 8), pack-reused 328011
Receiving objects: 100% (328129/328129), 136.28 MiB | 3.17 MiB/s, done.
Resolving deltas: 100% (253681/253681), done.
Submodule path 'src/doc/rust-by-example': checked out 'f633769acef68574427a6fae6c06f13bc2199573'
Updating submodule library/stdarch
Submodule 'library/stdarch' (https://github.com/rust-lang/stdarch.git) registered for path 'library/stdarch'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/library/stdarch'...
remote: Enumerating objects: 21366, done.
remote: Counting objects: 100% (451/451), done.
remote: Compressing objects: 100% (242/242), done.
remote: Total 21366 (delta 277), reused 321 (delta 186), pack-reused 20915
Receiving objects: 100% (21366/21366), 10.14 MiB | 3.55 MiB/s, done.
Resolving deltas: 100% (17219/17219), done.
Submodule path 'library/stdarch': checked out '9c732a56f67f54d12a0b4fd99993154906c95ea6'
Updating submodule src/doc/rustc-dev-guide
Submodule 'src/doc/rustc-dev-guide' (https://github.com/rust-lang/rustc-dev-guide.git) registered for path 'src/doc/rustc-dev-guide'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/doc/rustc-dev-guide'...
remote: Enumerating objects: 7947, done.
remote: Counting objects: 100% (287/287), done.
remote: Compressing objects: 100% (100/100), done.
remote: Total 7947 (delta 211), reused 243 (delta 186), pack-reused 7660
Receiving objects: 100% (7947/7947), 6.19 MiB | 3.38 MiB/s, done.
Resolving deltas: 100% (5743/5743), done.
Submodule path 'src/doc/rustc-dev-guide': checked out '7adfab42bab045a848126895c2f1e09927c1331a'
Updating submodule src/doc/edition-guide
Submodule 'src/doc/edition-guide' (https://github.com/rust-lang/edition-guide.git) registered for path 'src/doc/edition-guide'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/doc/edition-guide'...
remote: Enumerating objects: 4701, done.
remote: Counting objects: 100% (17/17), done.
remote: Compressing objects: 100% (14/14), done.
remote: Total 4701 (delta 5), reused 6 (delta 3), pack-reused 4684
Receiving objects: 100% (4701/4701), 4.07 MiB | 3.10 MiB/s, done.
Resolving deltas: 100% (3378/3378), done.
Submodule path 'src/doc/edition-guide': checked out 'b91a9a881ee007c12e74e844460ec407cf07a50f'
Updating submodule src/llvm-project
Submodule 'src/llvm-project' (https://github.com/espressif/llvm-project) registered for path 'src/llvm-project'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/llvm-project'...
remote: Enumerating objects: 3985824, done.
remote: Counting objects: 100% (605/605), done.
remote: Compressing objects: 100% (121/121), done.
remote: Total 3985824 (delta 497), reused 484 (delta 484), pack-reused 3985219
Receiving objects: 100% (3985824/3985824), 1.23 GiB | 3.06 MiB/s, done.
Resolving deltas: 100% (3158060/3158060), done.
Submodule path 'src/llvm-project': checked out '72de7ca254b47a76ff7f34202cfb4cc73c288301'
Updating submodule src/doc/embedded-book
Submodule 'src/doc/embedded-book' (https://github.com/rust-embedded/book.git) registered for path 'src/doc/embedded-book'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/doc/embedded-book'...
remote: Enumerating objects: 2221, done.
remote: Counting objects: 100% (107/107), done.
remote: Compressing objects: 100% (53/53), done.
remote: Total 2221 (delta 52), reused 86 (delta 47), pack-reused 2114
Receiving objects: 100% (2221/2221), 2.35 MiB | 5.16 MiB/s, done.
Resolving deltas: 100% (1352/1352), done.
Submodule path 'src/doc/embedded-book': checked out 'ceec19e873be87c6ee5666b030c6bb612f889a96'
Updating submodule src/tools/rust-analyzer
Submodule 'src/tools/rust-analyzer' (https://github.com/rust-analyzer/rust-analyzer.git) registered for path 'src/tools/rust-analyzer'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/src/tools/rust-analyzer'...
remote: Enumerating objects: 137469, done.
remote: Counting objects: 100% (2187/2187), done.
remote: Compressing objects: 100% (953/953), done.
remote: Total 137469 (delta 1589), reused 1703 (delta 1217), pack-reused 135282
Receiving objects: 100% (137469/137469), 36.10 MiB | 4.59 MiB/s, done.
Resolving deltas: 100% (90453/90453), done.
Submodule path 'src/tools/rust-analyzer': checked out '1a59f75cdaa730c16a694a4294eccf6dfe6fe0ad'
Updating submodule library/backtrace
Submodule 'library/backtrace' (https://github.com/rust-lang/backtrace-rs.git) registered for path 'library/backtrace'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/library/backtrace'...
remote: Enumerating objects: 3860, done.
remote: Counting objects: 100% (39/39), done.
remote: Compressing objects: 100% (30/30), done.
remote: Total 3860 (delta 15), reused 17 (delta 5), pack-reused 3821
Receiving objects: 100% (3860/3860), 1.12 MiB | 3.54 MiB/s, done.
Resolving deltas: 100% (2449/2449), done.
Submodule path 'library/backtrace': checked out 'af078ecc0b069ec594982f92d4c6c58af99efbb5'
Submodule 'backtrace-sys/src/libbacktrace' (https://github.com/rust-lang/libbacktrace) registered for path 'library/backtrace/crates/backtrace-sys/src/libbacktrace'
Cloning into '/home/rajput/dev/esp8266/rust-xtensa/library/backtrace/crates/backtrace-sys/src/libbacktrace'...
remote: Enumerating objects: 363, done.
remote: Total 363 (delta 0), reused 0 (delta 0), pack-reused 363
Receiving objects: 100% (363/363), 846.61 KiB | 1.68 MiB/s, done.
Resolving deltas: 100% (262/262), done.
Submodule path 'library/backtrace/crates/backtrace-sys/src/libbacktrace': checked out '5c88e094a691bb803d4bba342403a10459abad9e'
Submodules updated in 712.50 seconds
downloading https://static.rust-lang.org/dist/2021-02-11/rust-std-1.50.0-x86_64-unknown-linux-gnu.tar.xz
################################################################################################################################################################################################################################# 100.0%
extracting /home/rajput/dev/esp8266/rust-xtensa/build/cache/2021-02-11/rust-std-1.50.0-x86_64-unknown-linux-gnu.tar.xz
downloading https://static.rust-lang.org/dist/2021-02-11/rustc-1.50.0-x86_64-unknown-linux-gnu.tar.xz
################################################################################################################################################################################################################################# 100.0%
extracting /home/rajput/dev/esp8266/rust-xtensa/build/cache/2021-02-11/rustc-1.50.0-x86_64-unknown-linux-gnu.tar.xz
downloading https://static.rust-lang.org/dist/2021-02-11/cargo-1.50.0-x86_64-unknown-linux-gnu.tar.xz
################################################################################################################################################################################################################################# 100.0%
extracting /home/rajput/dev/esp8266/rust-xtensa/build/cache/2021-02-11/cargo-1.50.0-x86_64-unknown-linux-gnu.tar.xz
    Updating crates.io index
  Downloaded version_check v0.9.1
  Downloaded regex-syntax v0.6.22
  Downloaded libc v0.2.85
  Downloaded regex v1.4.3
  Downloaded autocfg v1.0.0
  Downloaded serde v1.0.118
  Downloaded getopts v0.2.21
  Downloaded serde_derive v1.0.118
  Downloaded 8 crates (1.2 MB) in 1.31s
   Compiling proc-macro2 v1.0.19
   Compiling unicode-xid v0.2.1
   Compiling syn v1.0.38
   Compiling autocfg v1.0.0
   Compiling version_check v0.9.1
   Compiling memchr v2.3.3
   Compiling lazy_static v1.4.0
   Compiling serde_derive v1.0.118
   Compiling cfg-if v0.1.10
   Compiling libc v0.2.85
   Compiling log v0.4.11
   Compiling serde v1.0.118
   Compiling regex-syntax v0.6.22
   Compiling ryu v1.0.5
   Compiling same-file v1.0.6
   Compiling serde_json v1.0.59
   Compiling fnv v1.0.7
   Compiling cc v1.0.60
   Compiling itoa v0.4.6
   Compiling bootstrap v0.0.0 (/home/rajput/dev/esp8266/rust-xtensa/src/bootstrap)
   Compiling unicode-width v0.1.8
   Compiling build_helper v0.1.0 (/home/rajput/dev/esp8266/rust-xtensa/src/build_helper)
   Compiling opener v0.4.1
   Compiling thread_local v1.0.1
   Compiling walkdir v2.3.1
   Compiling bstr v0.2.13
   Compiling quote v1.0.7
   Compiling time v0.1.43
   Compiling num_cpus v1.13.0
   Compiling filetime v0.2.12
   Compiling regex v1.4.3
   Compiling globset v0.4.5
   Compiling ignore v0.4.16
   Compiling merge_derive v0.1.0
   Compiling merge v0.1.0
   Compiling toml v0.5.7
    Finished dev [unoptimized + debuginfo] target(s) in 6m 57s

Couldn't find required command: ninja
You should install ninja, or set ninja=false in config.toml

failed to run: /home/rajput/dev/esp8266/rust-xtensa/build/bootstrap/debug/bootstrap build
Build completed unsuccessfully in 0:19:29

rust-xtensa on  xtensa-target via 🐍 v2.7.18 via 🦀 v1.48.0 took 19m29s
❯ sudo apt install ninja
[sudo] password for rajput:
Reading package lists... Done
Building dependency tree
Reading state information... Done
E: Unable to locate package ninja

rust-xtensa on  xtensa-target via 🐍 v2.7.18 via 🦀 v1.48.0 took 3s
❯ sudo apt install ninja-build
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following NEW packages will be installed:
  ninja-build
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 107 kB of archives.
After this operation, 338 kB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu focal/universe amd64 ninja-build amd64 1.10.0-1build1 [107 kB]
Fetched 107 kB in 1s (104 kB/s)
Selecting previously unselected package ninja-build.
(Reading database ... 84284 files and directories currently installed.)
Preparing to unpack .../ninja-build_1.10.0-1build1_amd64.deb ...
Unpacking ninja-build (1.10.0-1build1) ...
Setting up ninja-build (1.10.0-1build1) ...
Processing triggers for man-db (2.9.1-1) ...

rust-xtensa on  xtensa-target via 🐍 v2.7.18 via 🦀 v1.48.0 took 2s
❯
