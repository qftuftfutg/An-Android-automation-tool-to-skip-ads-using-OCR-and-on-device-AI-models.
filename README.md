# 清屏（QingPing）

清屏是一款 Android 无障碍辅助工具，目标是降低开屏广告和误触外跳的干扰，并记录各目标应用的拦截情况。

## 项目资料

- [项目问题记录总览](docs/project-issues/README.md)
- [清屏问题历史与遗留项](docs/project-issues/问题记录.md)

## 源码包

当前拟发布源码包：`qingping-1.7.0-source-with-support.zip`（324,294 bytes）。

**注意：源码包尚未作为 GitHub Release 附件或仓库文件发布。** 本次 GitHub 连接已验证可以创建、读取和删除文本文件，但当前可用的 GitHub 上传接口不支持直接传输本地 ZIP 二进制文件，因此不会用错误的文本/base64 文件冒充 ZIP。源码包内容可在后续通过 GitHub 网页的 Add file → Upload files 上传到 `releases/`，或创建 Release 后添加附件。

## 版本与验证声明

- 该 ZIP 内部目录名为 `qingping-1.7.0/`，包含 56 个条目。
- ZIP 完整性检查通过（未发现损坏条目）。
- 版本标签统一为 1.7.0，不代表所有功能都已完成 Android Gradle 构建或真机回归。
- 未在本次上传操作中执行 Android 编译，也未进行设备回归测试。
- 项目历史问题记录截至 2026-10-23，具体遗留项见问题记录文档。

## 安全原则

AI 不能直接授权点击；正文/标题中的“跳过”不能触发广告跳过；观察模式只记录不点击；截图按短生命周期隔离处理，不应上传或进入共享存储。
