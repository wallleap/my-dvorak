# 我的 Dvorak 键盘方案

仅 Dvorak，非 Dvorak Programmer

- 左 QWERTY
- 右 **Dvorak**

![](https://cdn.wallleap.cn/img/pic/illustration/20260718160350482.jpg?imageSlim)

## macOS 平台

1. 下载 [Karabiner-Elements](https://karabiner-elements.pqrs.org/)

2. 复制 `karabiner/karabiner.json` 到 `~/.config/karabiner` 目录下

3. 确保这个已启用

   ![](https://cdn.wallleap.cn/img/pic/illustration/20260718145208602.png?imageSlim)

> 怎么获取 `key_code`：运行 Karabiner-EventViewer，打开 **Monitoring events** 后按下按键，完成后点击 Copy to pasteboard

在某些 app 禁用：

在应用程序目录找到 `xxx.app`，右击-显示包内容，进入 `Contents` 目录，使用文本编辑器打开 `info.plist`，找到包名复制

![](https://cdn.wallleap.cn/img/pic/illustration/20260719100137148.png?imageSlim)

Karabiner-Elements - Complex Modifications 使用文本编辑器打开

![](https://cdn.wallleap.cn/img/pic/illustration/20260719094420229.png?imageSlim)

参照 `"^com\\.netease\\.uuremote$"` 修改一个，之后全局替换

```json
"bundle_identifiers": [
  "^com\\.netease\\.uuremote$",
  "^com\\.oray\\.sunlogin\\.macclient$"
],
```



## Windows 平台

1. 下载 [PowerToys](https://learn.microsoft.com/zh-cn/windows/powertoys/)，安装完右击托盘图标，选择关闭

2. 复制 `PowerToys` 目录下三个 `json` 文件到 `%LocalAppData%\Microsoft\PowerToys\Keyboard Manager` 目录

3. 重新运行 PowerToys，确认映射正确

   ![](https://cdn.wallleap.cn/img/pic/illustration/20260718182141500.png?imageSlim)

4. 如果没有成功映射，可以在 PowerToys 选择恢复这个备份文件 `PowerToys/Backup/settings_134288397215974515.ptb` 