# AE Master

> An After Effects advisor skill grounded in official Adobe documentation.

**AE Master** is built for motion designers who need clear, production-ready guidance—not another pile of disconnected tutorials. It turns Adobe user guides, expression references, release notes, and system requirements into practical workflows for real shots, templates, and deliveries.

## Capabilities

- **Officially grounded answers**: Validates menus, features, format support, version differences, beta status, and known issues against Adobe Help and Release Notes.
- **Practical AE workflows**: Covers keyframes, text and shape animation, compositing, rotoscoping, tracking, 3D, color management, rendering, export, and performance.
- **Expression support**: Provides ready-to-paste JavaScript expressions, with the target property, adjustable controls, coordinate or dimension notes, and compatibility context.
- **Troubleshooting and delivery**: Separates viewer behavior, project color space, footage interpretation, output settings, and platform playback—then troubleshoots from low-risk to high-risk fixes.

## Typical Questions

- “What is the most reliable way to build this After Effects shot?”
- “Which property should this expression go on, and why is it throwing an error?”
- “How can I make an Essential Graphics / MOGRT template editable without making it fragile?”
- “Why do Roto, tracking, 3D, color, or render results differ from what I expected?”
- “Is this feature supported in my current version, and is it still in beta?”

## Usage

After installing this skill, invoke $ae-master in your task.

You can also simply describe your AE problem. Include your AE version, operating system, full error message, relevant layers or effects, and delivery specs when possible; this makes it easier to provide a reproducible solution.

## Guiding Principles

1. **Conclusion first, then the steps**: Recommend the most reliable production path first, followed by the key settings and verification method.
2. **Keep official facts separate from creative advice**: Adobe-confirmed product behavior is never presented as a personal aesthetic judgment.
3. **Verify version-sensitive information**: New features, compatibility, format support, beta status, and known issues are checked against current official pages.
4. **Make expressions usable**: Defaults to the JavaScript expression engine and keeps expressions distinct from the scripting API.

## Repository Structure

- SKILL.md
- agents/openai.yaml
- references/official-source-map.md
- references/expression-workflow.md

## Official Sources

- [After Effects User Guide](https://helpx.adobe.com/after-effects/user-guide.html)
- [After Effects Release Notes](https://helpx.adobe.com/after-effects/desktop/what-s-new/release-notes-after-effects.html)
- [Expression language reference](https://helpx.adobe.com/after-effects/using/expression-language-reference.html)

---

## 中文说明

> 基于 Adobe 官方文档的 After Effects 专属顾问 Skill。

**AE 大师** 面向日常使用 After Effects 的动效师：把 Adobe 官方用户指南、表达式参考、版本更新与系统要求转化为可执行的中文操作建议。它不是把文档链接堆给你，而是优先解决当前镜头、模板或交付中的具体问题。

### 能力

- **官方事实核验**：对菜单、功能、格式支持、版本差异、Beta 与已知问题，优先核验 Adobe Help 与 Release Notes。
- **AE 实操工作流**：覆盖关键帧、文字与形状动画、合成、抠像、跟踪、3D、色彩管理、渲染导出与性能优化。
- **表达式协作**：提供可直接粘贴的 JavaScript expression，并说明放置属性、可调参数、坐标/维度与兼容性。
- **专业排错与交付**：把查看器、项目色彩空间、素材解释、输出设置与平台播放区分开来，按低风险到高风险的顺序排查。

### 适合解决的问题

- “这个 AE 动效镜头最稳的做法是什么？”
- “这段表达式应该贴在哪里，为什么报错？”
- “基本图形 / MOGRT 模板怎样做得可编辑又不易崩？”
- “Roto、跟踪、3D、色彩或渲染结果为什么和预期不同？”
- “这个功能在当前版本是否支持，是否仍属于 Beta？”

### 使用方式

安装本仓库中的 Skill 后，可在任务中引用 ae-master。

也可以直接描述你的 AE 问题。建议同时提供 AE 版本、操作系统、报错全文、涉及图层/效果及目标交付规格；这样可以更快给出可复现的方案。

### 回答原则

1. **先结论，再步骤**：先推荐稳定的制作路径，再说明关键设置与验证方法。
2. **官方事实与创作建议分开**：Adobe 已确认的产品行为不会和个人审美判断混为一谈。
3. **版本敏感内容实时核验**：新功能、兼容性、格式支持、Beta 与已知问题优先查看最新官方页面。
4. **表达式可落地**：默认以 JavaScript expression engine 为准，不混淆表达式与脚本 API。

### 仓库结构

- SKILL.md
- agents/openai.yaml
- references/official-source-map.md
- references/expression-workflow.md

### 官方资料基础

- [After Effects User Guide](https://helpx.adobe.com/after-effects/user-guide.html)
- [After Effects Release Notes](https://helpx.adobe.com/after-effects/desktop/what-s-new/release-notes-after-effects.html)
- [Expression language reference](https://helpx.adobe.com/after-effects/using/expression-language-reference.html)

---

让 AE 大师成为你随时可调用的官方资料核验者、表达式搭档与动效制作顾问。
