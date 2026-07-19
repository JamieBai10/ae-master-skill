# AE 表达式工作准则

以 Adobe 官方 [Expression language reference](https://helpx.adobe.com/after-effects/using/expression-language-reference.html) 与 [Understanding the expression language](https://helpx.adobe.com/after-effects/using/expression-language.html) 为准。

## 回答步骤

1. 确认目标属性及维度：标量（Opacity/Rotation）、二维（Position）或三维；确认用户想驱动的结果而不只是一段代码。
2. 先优先给不依赖图层名称的方案；若必须引用图层或效果，说明需将名称改成代码中的名称，或用吸管/表达式拾取器生成引用。
3. 写出最小表达式；注明粘贴位置、是否要先打关键帧，以及时间单位为秒。
4. 验证：移动当前时间指示器、改变输入属性，并检查表达式错误提示。若项目为旧版，检查 `File > Project Settings > Expressions` 的 engine。

## 必须避免的混淆

- 表达式基于 JavaScript，并使用 AE 的内置对象；它只决定所附属性在每一帧的值。
- 脚本是命令序列，可创建/修改项目；不要把脚本 API（例如 `app.project` 的写操作）贴给只需要表达式的用户。
- 当前 JavaScript engine 与 Legacy ExtendScript 的语法/行为不同。旧项目可默认 Legacy；需要兼容时先核验，不要假设 `let`、`const`、现代数组/字符串方法均可用。
- JavaScript 区分大小写。图层、效果、属性的名称引用也会受到重命名和本地化影响。

## 常见模式的检查点

| 目标 | 先核验的官方元素 | 特别检查 |
| --- | --- | --- |
| 循环关键帧 | `loopIn` / `loopOut` 方法 | 循环类型、关键帧区间及是否需包含最后一帧。 |
| 跟随/延迟 | `valueAtTime()`、`thisComp.layer()` | 时间偏移为秒；位置维度要匹配。 |
| 数值映射 | `linear()`、`ease()`、`easeIn()`、`easeOut()` | 输入/输出范围、夹紧行为和数组维度。 |
| 随机抖动 | `wiggle()`、`seedRandom()` | 幅度单位、频率和是否需要可重复随机结果。 |
| 文本/框适配 | `sourceRectAtTime()`、Text 属性 | 段落文本的边界与 `includeExtents` 行为；字体/描边会影响测量。 |
| 父子与坐标空间 | `toComp()`、`fromComp()`、`toWorld()` 等 | 分清层空间、合成空间、世界空间与二维/三维层。 |

## 输出格式

用下面的紧凑结构，除非用户只要代码：

1. **用途**：一句话解释结果。
2. **放置位置**：例如“选中 Position，按住 Option/Alt 点击秒表”。
3. **表达式**：代码块。
4. **调整项**：只解释用户真正会改的变量。
5. **兼容性**：仅在版本/engine 会影响结果时写出。
