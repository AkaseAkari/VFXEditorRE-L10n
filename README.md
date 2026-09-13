# VFXEditorRE 汉化字典

VFXEditorRE（基于 [0ceal0t/Dalamud-VFXEditor](https://github.com/0ceal0t/Dalamud-VFXEditor) 1.9.4.4 的中英双语版）的运行时翻译字典。

## 文件说明

| 文件 | 条目数 | 用途 |
| --- | --- | --- |
| `l10n_static.json` | 1636 | 静态 UI 文本字典（英文原文 → 中文译文） |
| `l10n_interp.json` | 113 | 插值文本模板字典（`"Emitter {{0}} ({{1}}"` → `"发射器 {{0}} ({{1}}"` 形式） |
| `manual_translations.json` | - | 人工校对/补充的翻译条目（构建字典的源数据之一） |
| `fixes.json` | - | 对参考译文（AtmoOmen/VFXEditor-CN）的修正条目 |

## 使用方式

字典以 C# 常量形式编译进插件（`VFXEditor/L10n.cs`），由插件的「设置 → 语言」下拉切换加载：

- **中文模式**：显示文本查 `l10n_static` / `l10n_interp` 字典，未命中的保持英文
- **英文模式**：全部显示源码原文

## 翻译原则

- AVFX 等格式的二进制 tag（`LpSt`、`SdNm` 等四字符码）一律不翻译
- 括号内的骨骼代码名保留原文，如 `面部 (j_kao)`
- 术语对齐 [AtmoOmen/VFXEditor-CN](https://github.com/AtmoOmen/VFXEditor-CN) 风格
- Tile = 平铺（游戏开发术语）
- 跨编辑器有歧义的单词保留英文原文（如 Normal / Screen / Add / Repeat）

翻译成果基于 AtmoOmen/VFXEditor-CN，部分条目为人工校对与新增。
