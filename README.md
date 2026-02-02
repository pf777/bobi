# 极速链接 (FastLink)

启动即用 **WebView** 全屏打开默认链接，把**任意普通移动网页地址**封装成 App 使用（不需要 PWA）。

## 功能

- 打开 App 即自动加载 `default_url`，无需点按钮
- 网页在应用内显示，模拟成 App
- 支持在 `res/values/strings.xml` 中修改 `default_url`

## 打包成 APK

详见 **[打包说明.md](打包说明.md)**。

- **Android Studio**：Build → Build Bundle(s) / APK(s) → Build APK(s)，APK 在 `app/build/outputs/apk/debug/`
- **命令行**：先让 Android Studio 打开一次项目生成 gradlew，再执行 `.\gradlew assembleDebug`

## 修改默认链接

编辑 `app/src/main/res/values/strings.xml`：

```xml
<string name="default_url">https://你的链接.com</string>
```

## 技术栈

- Kotlin + View Binding + WebView
- Min SDK 24，Target SDK 34
