# XMRig

Unofficial releases of XMRig miner without hashing power donation *(0% dev fee)*. You can manually disable developer fee from source code.

### Building from source
Get the external [source code](https://github.com/xmrig/xmrig). Search for `donate` header file, change variable `kDefaultDonateLevel` and `kMinimumDonateLevel` value to `0`, and then see [Windows build](https://github.com/arris42/xmrig#windows-build) section below for building binary

Finally, configure `donate-level` value to `0` in `config.json` (if config file is not exist, create manually)

> Consider making a donation to [developer](https://github.com/xmrig/xmrig#donations) if you are using this binary or disable developer fee

- External [source](https://github.com/xmrig/xmrig)

## Windows build

Make sure to install [MSYS2](https://github.com/msys2/msys2-installer/releases) first, and follow XMRig build [steps](https://xmrig.com/docs/miner/build/windows). There is also MSYS [portable download](https://github.com/msys2/msys2-installer/releases/download/2023-01-27/msys2-base-x86_64-20230127.tar.xz) for advanced user

> You can use Microsoft Visual Studio if you have one and start build them. But if you are just building binaries AND you have slow-performance system, use MSYS2 instead.

## Other platform build

Visit [manual page](https://xmrig.com/docs/miner/build) to build XMRig on other platform
