# SDK打包配置

## 编译指令设置
- 可以通过该设置配置SDK包含的编译指令，及不包含的编译指令，可以单独设置模拟器版及真机版。在xcode 12之后默认模拟器包含`arm64`，与真机SDK合并会冲突，需要通过这个方法去掉.

```swift

EXCLUDED_ARCHS[sdk=iphoneos*] = x86_64 // 设置真机不包含的指令
EXCLUDED_ARCHS[sdk=iphonesimulator*] = arm64 // 设置模拟器不包含的指令
ARCHS[sdk=iphoneos*] = arm64 armv7 // 设置真机包含的指令
ARCHS[sdk=iphonesimulator*] = x86_64 i386 // 设置模拟器包含的指令
VALID_ARCHS[sdk=iphoneos*] = arm64 armv7 
VALID_ARCHS[sdk=iphonesimulator*] = x86_64 i386

```
- 查看SDK包含的编译指令，使用 `lipo -info 路径`![](/images/Snip20201106_11.png)