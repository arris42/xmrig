# XMRig

Unofficial XMRig miner windows release without hash power donation *(0% dev fee)*. You need to manually disable donation fee from source code. ✨

## Release builds
👉 Just [grab it](https://github.com/arris42/xmrig/releases)

## Building from source
If you feel my builds contains stupid malware. Or you are a *hobbyist* compiler, follow these steps how to build on windows :

### Prerequisites
- [CMake](https://cmake.org/download/) Make sure to `add CMake to the system PATH`
- [MSYS](https://github.com/msys2/msys2-installer/releases/)

### Installing
Open MSYS2 and execute following commands :
- `pacman -Syu` (might need to restart afterwards)
- `pacman -S mingw-w64-ucrt-x86_64-gcc mingw-w64-x86_64-gcc git make unzip`
- `mkdir C:\\xmrig-source`
- `cd C:\\xmrig-source`
- `curl --output xmrig-deps-master.zip https://github.com/xmrig/xmrig-deps/archive/refs/heads/master.zip`
- `unzip xmrig-deps-master.zip`
- `git clone https://github.com/xmrig/xmrig.git`

### Modifying
> You need external code editor like, sublime or notepad++
- Go to `C:\xmrig-source\xmrig`
- Inside `src` folder, look for `donate` header file, and edit it with your favorite code editor.
- Look for variable `kDefaultDonateLevel` and `kMinimumDonateLevel`. Change both value to `0`
- Save it!

### Compiling
Now, the time has finally come.. ✨
- Still opening MSYS2
- `cd C:\\xmrig-source\\xmrig` (Just to make sure)
- `mkdir builds && cd builds`
- `"C:\Program Files\CMake\bin\cmake.exe" .. -G "Unix Makefiles" -DXMRIG_DEPS=C:/xmrig-source/gcc/x64`
- Now you have compiled xmrig inside `C:\xmrig-source\xmrig\builds`

Finally, edit the `config.json` and change `donate-level` value to `0`

### Issues
There are a bunch of MSYS2 shortcuts, like MINGW64, UCRT64, and CLANG64.

If you encounter some errors when compiling, you might try `MSYS2 MINGW64` instead.

## Other platform

Visit [manual build](https://xmrig.com/docs/miner/build) for more info
> Optionally, make a donation to [developer](https://github.com/xmrig/xmrig#donations)
