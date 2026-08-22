# Compact Prompt Examples

Use these examples to calibrate density, not as fixed templates. Preserve the user's language and requested format.

## Git forensics

**Input**

> 帮我对比 HiComposerBench 的 master、baseline/ace-rtl 和本地工作区，判断哪些保留或丢弃；先只读，不要修改。

**Output**

> 只读审计 HiComposerBench 的 `master`、`baseline/ace-rtl` 与工作区。用 `git merge-base` 定位分叉点，分别统计两侧 commit/path 集合及 overlap；区分 HEAD、tracked、untracked 与 CRLF 噪声，并验证本地/远端 refs，不臆造缺失分支。按路径给出 Keep/Discard/Commit-on-master，附 hash、ISO 时间和证据。不得 merge、reset 或改工作区。完成标准：每项差异已归类，未知项明确标注。

**Why these terms stay**

`merge-base`, refs, tracked/untracked, CRLF, and set overlap replace longer explanations with exact Git concepts.

## Event-driven product behavior

**Input**

> 帮我写一个用于开发拖延症网页应用的 prompt，要有提醒和任务拆解。

**Output**

> 开发一个任务启动网页应用：用户可创建任务并将其拆成可编辑、排序、完成的下一步；当用户设定的提醒时间到达时，系统应显示任务与下一步，并提供开始、稍后提醒和重排。通知权限不可用时回退到页内提醒，不虚构时长或频率。沿用现有技术栈；关键架构信息缺失时先问一个问题。完成标准：创建→拆解→提醒→完成流程可运行，并有对应测试与启动说明。

**Why EARS applies**

The reminder has a trigger and observable response. Other requirements stay in compact natural language.

## Explicit detailed mode

**Input**

> 把“审查项目登录安全”优化成详细 prompt，要求每个结论可追溯。

**Output**

> 只读审查当前项目的登录安全，不修改文件、配置、依赖或外部状态。
>
> 1. 定位全部登录入口和 trust boundary，追踪凭据从客户端、API、认证逻辑、用户存储到 session/token 的 data flow。
> 2. 基于实际代码与配置检查认证绕过、用户枚举、暴力破解防护、密码处理、session fixation、Cookie/JWT 属性、CSRF、CORS、注入、开放重定向、OAuth/OIDC（如适用）、secret 泄露和敏感日志。
> 3. 仅把有文件、行号和可利用路径证据的问题列为 confirmed finding；依赖部署配置或无法验证的控制标为 unverified，不从缺失证据推断漏洞。
> 4. 每项发现包含 severity、confidence、CWE/OWASP 映射、证据、攻击前提、影响、最小修复和验证测试。
>
> 完成标准：每条可达登录路径已检查或列为 blind spot；输出按 confirmed、unverified、未发现证据分组，所有结论可追溯且不泄露 secret。

This output exceeds the default because the user explicitly requested detail and traceability.

## Avoid fabricated precision

**Input**

> 优化：系统要快速返回搜索结果。

**Output**

> 定义并验证搜索响应性能：先确认目标延迟、百分位、负载和测试环境；信息未提供时标为待定，不自行填写阈值。完成标准：需求包含可测量的延迟指标、并发条件、测量方法及超限行为。

Do not turn “fast” into an invented value such as “200 ms at p95.” A number supplied as a proposal must be labeled as an assumption.
