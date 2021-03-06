# safe_ffi

[![](https://img.shields.io/badge/Project%20SAFE-Approved-green.svg)](http://maidsafe.net/applications) [![](https://img.shields.io/badge/License-GPL3-green.svg)](https://github.com/maidsafe/crust/blob/master/COPYING)


**Primary Maintainer:**     Spandan Sharma (spandan.sharma@maidsafe.net)

**Secondary Maintainer:**   Krishna Kumar (krishna.kumar@maidsafe.net)

|Linux/OS X|Windows|Coverage|Issues|
|:--------:|:-----:|:------:|:----:|
|[![Build Status](https://travis-ci.org/maidsafe/safe_ffi.svg?branch=master)](https://travis-ci.org/maidsafe/safe_ffi)|[![Build status](https://ci.appveyor.com/api/projects/status/5nqc5h06v3vsp2ad/branch/master?svg=true)](https://ci.appveyor.com/project/MaidSafe-QA/safe-ffi/branch/master)|[![Coverage Status](https://coveralls.io/repos/maidsafe/safe_ffi/badge.svg?branch=master&service=github)](https://coveralls.io/github/maidsafe/safe_ffi?branch=master)|[![Stories in Ready](https://badge.waffle.io/maidsafe/safe_ffi.png?label=ready&title=Ready)](https://waffle.io/maidsafe/safe_ffi)|

| [API Documentation - master branch](http://maidsafe.net/safe_ffi/master) | [SAFE Network System Documentation](http://systemdocs.maidsafe.net) | [MaidSafe website](http://maidsafe.net) | [Safe Community site](https://forum.safenetwork.io) |
|:------:|:-------:|:-------:|:-------:|

###Pre-requisite:
`libsodium` is a native dependency for [sodiumxoide](https://github.com/dnaq/sodiumoxide). Install sodium by following the instructions [here](http://doc.libsodium.org/installation/index.html).

For windows:

- Download [prebuilt libsodium library](https://download.libsodium.org/libsodium/releases/libsodium-1.0.2-mingw.tar.gz)
- Extract `libsodium.a` for x86/x64 from the corresponding folder in the archive to your local filesystem
- Add this local path to `%SODIUM_LIB_DIR%` (`setx SODIUM_LIB_DIR <path-to-extracted-libsodium.a-dir>`). Restarting the command-prompt maybe necessary after this.

###Build Instructions:
`safe_ffi` can interface with Client modules conditionally built against either the routing crate or a mock used for local testing.

To use it with the Mock:
```
cargo build --features "use-mock-routing"
cargo test --features "use-mock-routing"
```

To interface it with actual routing (default):
```
cargo build
cargo test
```
##TODO
### [0.0.1]
- [ ] [MAID-1231](https://maidsafe.atlassian.net/browse/MAID-1321) safe_ffi - Make reading for file relative to serice home dir
- [ ] [MAID-1232](https://maidsafe.atlassian.net/browse/MAID-1322) safe_ffi - changes according to other crates and update test cases
