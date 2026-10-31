# 清屏（QingPing）

清屏是一款 Android 无障碍辅助工具，目标是降低开屏广告和误触外跳的干扰，并记录各目标应用的拦截情况。

## 项目资料

- [项目问题记录总览](docs/project-issues/README.md)
- [清屏问题历史与遗留项](docs/project-issues/问题记录.md)
- [本次源码剥离说明](docs/SOURCE_DISTRIBUTION_NOTICE.md)（随源码包提供）

## 当前公开源码分发范围

当前整理版本为 **1.7.0-clean-source**。它基于原 1.7.0 源码，已移除早期原型中的第三方广告规则 JSON 导入器、导入 UI、兼容字段解析、包名哈希匹配和对应规则执行入口。

清屏自己的内置广告识别、安全控件校验、观察模式、OCR/AI 诊断、日志与统计仍保留。历史文档可能提及早期兼容原型，这是开发历史记录，不代表当前源码仍提供该功能。

详细剥离清单、保留范围和验证边界见源码包内的 `SOURCE_DISTRIBUTION_NOTICE.md`。

## 支持作者
如果这个项目对你有帮助，可以自愿通过 [爱发电支持作者](https://afdian.com/a/123xiaole)。赞助不影响项目功能、安全判断或研究结论。

## 安全原则

AI 不能直接授权点击；正文/标题中的“跳过”不能触发广告跳过；观察模式只记录不点击；自动识别链路取得的屏幕截图按短生命周期内存对象处理，不应写入共享存储或上传。人工标注工具导入的图片会按功能需要持久保存在应用私有目录；用户主动导出的数据集 ZIP 可能被保存到应用外部，不能笼统宣称“所有截图从不落盘”。

## 风险边界

剥离第三方规则兼容层是工程来源管理和降低耦合的措施，不是法律免责保证。代码、规则数据、商标、宣传和实际运营行为可能涉及不同法律问题；公开发布或商业化前应由熟悉中国知识产权与竞争法的律师审查。

QingPing
QingPing is an Android accessibility assistant tool. Its goal is to reduce the interference from splash-screen ads and accidental taps that trigger external jumps, and to record the interception status of each target application.

Project Documents

* Overview of Project Issue Records
* QingPing Issue History and Remaining Items
* This Source Code Stripping Statement (provided with the source code package)

Current Public Source Code Distribution Scope
The currently organized version is 1.7.0-clean-source. It is based on the original 1.7.0 source code, with the third-party ad rule JSON importer, import UI, compatible field parsing, package name hash matching and the corresponding rule execution entry in the early prototype removed.

QingPing's own built-in ad recognition, security control verification, observation mode, OCR/AI diagnosis, logs and statistics are still retained. Historical documents may mention the early compatible prototype, which is a development historical record and does not mean that the current source code still provides this function.

For the detailed stripping list, retention scope and verification boundaries, please refer to SOURCE_DISTRIBUTION_NOTICE.md in the source code package.

Support the Author
If this project is useful to you, you may voluntarily [support the author via Afdian](https://afdian.com/a/123xiaole). Sponsorship does not affect project features, safety decisions, or research conclusions.

Security Principles
AI cannot directly authorize clicks; the word "Skip" in body text/title cannot trigger ad skipping; observation mode records without clicking. Screenshots captured by the automatic-recognition path are handled as short-lived in-memory objects and are not intended to be written to shared storage or uploaded. Images imported by the manual annotation tool are persisted in app-private storage as required by that feature; user-exported dataset ZIP files may be saved outside the app sandbox. These data flows must not be conflated.

Risk Boundaries
Stripping the third-party rule compatibility layer is a measure for engineering source management and coupling reduction, not a legal disclaimer. Codes, rule data, trademarks, promotion and actual operation behaviors may involve different legal issues; before public release or commercialization, a lawyer familiar with China's intellectual property and competition laws shall conduct a review.
