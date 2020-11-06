# SDK打包配置

## 编译指令设置
可以通过该设置配置SDK包含的编译指令，及不包含的编译指令，可以单独设置模拟器版及真机版。

``` swift
EXCLUDED_ARCHS[sdk=iphoneos*] = x86_64 // 设置
EXCLUDED_ARCHS[sdk=iphonesimulator*] = arm64
ARCHS[sdk=iphoneos*] = arm64 armv7
ARCHS[sdk=iphonesimulator*] = x86_64 i386
VALID_ARCHS[sdk=iphoneos*] = arm64 armv7
VALID_ARCHS[sdk=iphonesimulator*] = x86_64 i386
```