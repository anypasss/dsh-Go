# DSH Go 悬浮授权 v2（完整源码分支）

这个分支是 DSH Go 1.3.0 的完整源码，并已合入悬浮授权 v2：

- 交还卡可「收起」进悬浮球，点悬浮球重新展开
- 卡片标题、正文、≡ 都可以拖动
- 继续 / 停止 / 倒计时 / 10 分钟超时逻辑保持不变

## 在另一台手机使用

```sh
git clone https://github.com/anypasss/dsh-Go.git
cd dsh-Go
git checkout v1.3.0-handoff-v2
```

按 DSH Go 官方构建文档准备 Flutter 3.47.7、Android SDK 36、NDK 28.2.13676358、Java 17 和 runtime 资源，然后：

```sh
bash tooling/build-apk.sh --side --no-companion -f arm64
```

安装 `app/build/app/outputs/flutter-apk/app-arm64-release.apk`（显示为「DSH Go 测试」，可与原版并存）。

## 关键修改

- `app/android/app/src/main/kotlin/io/github/ccch1mneyyy/dsh_app/phone/PhonePromptUi.kt`
- `app/android/app/src/main/kotlin/io/github/ccch1mneyyy/dsh_app/phone/a11y/ControlOverlay.kt`
- `app/android/app/src/main/kotlin/io/github/ccch1mneyyy/dsh_app/phone/a11y/OverlayModel.kt`
