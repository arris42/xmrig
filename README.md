# XMRig

Unofficial XMRig miner windows release without hash power donation *(0% dev fee)*. You need to manually disable donation fee from source code. ✨

## Release builds
👉 Just [grab it](https://github.com/arris42/xmrig/releases)

## Building from source
If you afraid of my builds contains StuPiD malware, or you are a *Hobbyist* compiler.. Well, follow this steps :

### Prerequisites
- [CMake](https://cmake.org/download/) Make sure to enable `add CMake to the system PATH`
- [MSYS](https://github.com/msys2/msys2-installer/releases/)
- Disable antivirus to prevent any compiling errors (you can enable it again after successful builds)
> Or.. add xmrig folder to antivirus exclusion instead. If you know what to do

### Installing
Open MSYS2 and execute following commands :
- `pacman -Syu` (might need to restart afterwards)
- `pacman -S mingw-w64-ucrt-x86_64-gcc mingw-w64-x86_64-gcc git make unzip`
- `mkdir C:\\xmrig-source`
- `cd C:\\xmrig-source`
- `curl --output xmrig-deps-master.zip "https://codeload.github.com/xmrig/xmrig-deps/zip/refs/heads/master"`
- `unzip xmrig-deps-master.zip`
- `git clone https://github.com/xmrig/xmrig.git`

### Modifying
> You need external code editor e.g Sublime, even notepad as well
- Go to `C:\xmrig-source\xmrig`
- Inside `src` folder, look for `donate.h` header file, and edit it with your favorite code editor.
- Look for variable `kDefaultDonateLevel` and `kMinimumDonateLevel`. Change both value to `0`
- Save it!

### Compiling
Now, the time has finally come.. ✨

Still opening MSYS2? Let's continue :
- `cd C:\\xmrig-source\\xmrig` (Just to make sure)
- `mkdir builds && cd builds`
- `"C:\Program Files\CMake\bin\cmake.exe" .. -G "Unix Makefiles" -DXMRIG_DEPS=C:/xmrig-source/xmrig-deps-master/gcc/x64`
- `make -j$(nproc)`

> Relax, it takes some time to compile ☕

Now you have compiled xmrig inside `C:\xmrig-source\xmrig\builds`. Make sure it's not detected by antivirus!

### Issues
There are bunch of MSYS2 shortcuts after installing, for like MINGW64, UCRT64, and CLANG64. If you encounter some errors while compiling, you can try `MINGW64` instead.

## Other platform

Visit [manual build](https://xmrig.com/docs/miner/build) for more info
> Optionally, make a donation to [developer](https://github.com/xmrig/xmrig#donations)
