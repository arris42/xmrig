# XMRig

Unofficial releases of XMRig miner without hashing power donation *(0% dev fee)*. You can manually disable developer fee from source code.

### How to build?
Search for `donate` header file, set `kDefaultDonateLevel` and `kMinimumDonateLevel` to `0`, and then see [Windows build](https://github.com/arris42/xmrig/edit/main/README.md#windows-build) section below for building binaries

Finally, in XMRig folder, disable donation fee from `config.json` by change `donate-level` value to `0`

> Consider making a donation to the [developer](https://github.com/xmrig/xmrig#donations) if you are using this binary or disable developer fee

- External [source](https://github.com/xmrig/xmrig)

## Windows build

Make sure to install [MSYS2](https://github.com/msys2/msys2-installer/releases), and follow XMRig build [steps](https://xmrig.com/docs/miner/build/windows). There is also MSYS [portable download](https://github.com/msys2/msys2-installer/releases/download/2023-01-27/msys2-base-x86_64-20230127.tar.xz) for advanced user

> You can use Microsoft Visual Studio if you have one, and start build them. But if you are just building binaries AND you have slow PC, use MSYS instead.
