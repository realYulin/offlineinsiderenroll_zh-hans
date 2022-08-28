To download the original English script, [please click here](https://github.com/abbodi1406/offlineinsiderenroll).
# OfflineInsiderEnroll

![OfflineInsiderEnroll 的英文截屏](https://i.imgur.com/hzusXzd.png)

## 描述

OfflineInsiderEnroll 是一个命令脚本，允许用户注册到
Windows 预览体验计划而不登录到 Microsoft 账户。

该脚本支持 Windows 11 或 Windows 10 1809 和更新版本。

## 用法

此脚本需要管理权限才能运行。您只需右键单击它>“以管理员身份运行”即可执行它。

### 安装和配置更改

After starting, the script offers selection of __*Windows Insider Program*__ channels.
要进行选择，请按下与您选择的选项对应的数字。

If the machine was not enrolled to the Insider Program, you will get prompted to
restart your machine to enable *`Microsoft Flight Signing`* which is required by
*`Windows Insider Program`*.

**Notice:** Windows Insider Program requires telemetry to be set to *`Full`*.
After enrolling your machine to the *Windows Insider Program* please make sure
that your diagnostic data collection settings are set to *`Full`*. Some `Insider
Preview` builds may not get offered in *`Windows Update`* if you do not have
correct telemetry settings.

You can verify or modify your telemetry settings as follows:

__Windows 11__: *`设置`* > *`Privacy and Security`* > *`Diagnostics & feedback`*

__Windows 10__: *`设置`* > *`Privacy`* > *`Diagnostics & Feedback`*

### Restoring Windows Insider Program to default options

To restore *`Windows Insider Program`* to default settings simply choose `Stop
receiving Insider Preview builds` in `OfflineInsiderEnroll Script`. You will get prompted
to reboot, because this option will disable *`Microsoft Flight Signing`*.

## 此脚本如何运行？

This script takes advantage of undocumented `TestFlags` registry value.
If this value is set to `0x20`, all access to online *Windows Insider* services
gets disabled. Because of this, we can set our own *Windows Insider Preview*
configuration without being overriden by the contact to the service. Since
`Windows Update` does not check if machine is actually enrolled to the program,
you will get offered *Insider Preview* builds by just setting correct values in
the registry.

## 许可

此项目使用 MIT License 许可。查看 "LICENSE" 文件以获取详细信息。
