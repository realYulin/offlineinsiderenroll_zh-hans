To download the original English script, [please click here](https://github.com/abbodi1406/offlineinsiderenroll).
# OfflineInsiderEnroll

![OfflineInsiderEnroll 的英文截屏](https://i.imgur.com/hzusXzd.png)

## 描述

OfflineInsiderEnroll 是一个命令脚本，允许用户注册到
Windows 预览体验计划而不登录到 Microsoft 帐户。
它也支持将 **不符合** Windows 11 系统要求的计算机注册到预览体验计划中。

该脚本支持 Windows 11 或 Windows 10 1809 和更新版本。

## 乱码修复

由于 GitHub 上托管的文件采用 UTF-8 编码，所以直接运行会乱码。
因此下载文件后先使用记事本打开，
点击 *文件* > *另存为*，将*编码*更改为**ANSI**即可修复。

## 用法

此脚本需要管理员权限才能运行。在脚本运行时会自动尝试提升权限，
如果弹出 **用户帐户控制** 的弹窗，请点击 **是**。

### 安装和配置更改

启动后，该脚本会提供 __*Windows 预览体验计划*__ 频道的选择。
要进行选择，请按下与您选择的选项对应的数字。

如果计算机未注册到预览体验计划，系统将提示您
重新启动计算机以启用 *`Microsoft Flight Signing`*，
这是 *`Windows 预览体验计划`* 所要求的。

**注意：** Windows 预览体验计划要求将遥测设置为 *`完整`*。
将计算机注册到 *Windows 预览体验计划* 后，请确保将诊断数据收集设置设置为 `完整`。
如果你没有正确的遥测设置，则某些“预览体验成员预览版”版本可能不会在 *`Windows 更新`* 中提供。

可以验证或修改遥测设置，如下所示：

__Windows 11__: *`设置`* > *`隐私和安全性`* > *`诊断和反馈`*

__Windows 10__: *`设置`* > *`隐私`* > *`诊断和反馈`*

### 将 Windows 预览体验计划恢复为默认选项

要将 *`Windows预览计划`* 恢复为默认设置，只需在“OfflineInsiderEnroll 脚本”中选择“停止接收预览版”。系统将提示您重新启动，因为此选项将禁用 *`Microsoft Flight Signing`*。

## 此脚本如何运行？

此脚本利用未记录的`TestFlags`注册表值。
如果此值设置为`0x20`，则将禁用对联机 *Windows 预览体验计划* 服务的所有访问。因此，我们可以设置自己的 *Windows 预览体验计划* 配置，而不会被服务的联系人覆盖。由于`Windows 更新`不会检查计算机是否实际注册到该程序，因此只需在注册表中设置正确的值，即可获得 *预览体验计划* 版本。

## 许可

此项目使用 MIT License 许可。查看 "LICENSE" 文件以获取详细信息。
