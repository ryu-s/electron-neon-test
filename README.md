# electron-neon-test-20201111

windowsでビルドする場合  
```
rustup default stable-x86_64-pc-windows-msvc
```
をやっておかないとエラーが出るかも。  

windowsで
```
electron-build-env neon build --release
electron .
```
とやると
```
  process didn't exit successfully: `C:\Users\shinmura\Source\Repos\electron-neon-test\native\target\release\build\neon-sys-15901a502fe9a320\build-script-build` (exit code: 1)
```
というエラーが出て失敗する。
代わりに
```
neon build --release
electron .
```
だとうまくいく。

