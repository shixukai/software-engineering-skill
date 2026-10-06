<p align="center">
  <img src="assets/hero.svg" alt="Software Engineering：面向 AI 编程代理的按任务指导" width="100%" />
</p>

<p align="center">
  <strong>让工程判断有依据，让验证范围说清楚。</strong><br />
  面向 AI 编程代理的实验性中文软件工程 Skill。
</p>

<p align="center">
  <a href="#试用安装预览版">试用预览版</a> ·
  <a href="#项目状态">项目状态</a> ·
  <a href="#工作流程示意">观看示意短片</a> ·
  <a href="#内容范围">内容范围</a> ·
  <a href="README.md">English</a>
</p>

> **安装预览版 · `0.1.0-preview.1`。** 提供可在本地安装的实验性 Skill 包。最终宿主加载和模型行为检查仍未完成，请从可丢弃的练习目录开始。

## 项目思路

从当前工程问题出发，检查相关需求、代码或观察结果，选择适用的方法，说明主要取舍，以及实际验证了什么。

实验性 Skill 按任务组织内容，让代理读取相关流程和方法，而非每次加载整个参考集合。目标是给出具体判断、对应证据与尚未解决的限制。

- **说清前提**：区分已确认事实、约束与未知
- **按任务选方法**：让处理深度与当前问题相称
- **让结论可复查**：保留依据、验证范围与剩余风险

## 工作流程示意

这段原创短片为 27 秒，用来说明预期交互方式。它不是实际安装运行、性能测试或真实项目结果的录像。

https://github.com/user-attachments/assets/f8a918e0-594f-4232-ab0f-bd87f8b0b2c7

## 内容范围

预览运行包包含十条任务流程，涉及：

- 需求澄清与验收
- 架构、领域与集成设计
- 功能实现
- 代码与变更审查
- 测试策略与验证
- 缺陷诊断
- 重构与遗留改动
- 集成、构建与交付
- 运行可靠性与运维
- 工程计划与协作

这些是指导内容的范围，不表示每项工程能力均已验证。Skill 不会增加代理修改、发布或操作系统的权限。

## 试用安装预览版

**版本：`0.1.0-preview.1`（预发布）。** 本包提供 [Skill 入口](skills/software-engineering/SKILL.md)及其引用文件，供本地试用。静态包检查已通过；这个公开包在宿主中的实际加载和模型行为尚未验证。

下载该版本的源码压缩包，或检出对应标签，然后在仓库根目录打开终端。下列命令需要已安装 Codex CLI，适用于 macOS/Linux 的 Bash 或 Zsh：

```bash
preview_dir="$(mktemp -d "${TMPDIR:-/tmp}/se-skill-preview.XXXXXX")" &&
mkdir -p "$preview_dir/.agents/skills" &&
cp -R skills/software-engineering "$preview_dir/.agents/skills/" &&
printf 'Preview directory: %s\n' "$preview_dir" &&
(cd "$preview_dir" && codex)
```

保留这个终端和打印出的路径。这里只把 Skill 复制到独立练习目录，不安装到主目录，也不修改全局配置。目录隔离不等于安全沙箱：宿主已有的设置、其他 Skill、连接和审批规则仍然适用。

进入 Codex 后使用 `/skills`，或显式输入 `$software-engineering`。先从不含敏感信息的虚构分析题开始：

```text
$software-engineering
一个虚构的报告任务可能在用户点击取消后完成。
请列出需要确认的行为要求，以及可观察的验收条件。
本次只分析，不修改文件或调用外部服务。
```

如果出现同名 Skill，选择打印出的练习目录内的条目。若未出现，重启 Codex，并核对[官方 Skill 文档](https://learn.chatgpt.com/docs/build-skills)。其他宿主尚未验证。请保留完整 Skill 文件夹；只复制 `SKILL.md` 会丢失引用内容。

### 移除预览

先退出 Codex，再在同一个终端中，把这份副本移出 Skill 发现路径：

```bash
if [ -n "${preview_dir:-}" ] &&
   [ -f "$preview_dir/.agents/skills/software-engineering/SKILL.md" ] &&
   [ ! -e "$preview_dir/software-engineering.disabled" ]; then
  mv "$preview_dir/.agents/skills/software-engineering" \
     "$preview_dir/software-engineering.disabled"
fi
```

重启宿主后再检查该本地条目是否消失。移出的副本仍可恢复；保存需要保留的练习内容后，可以手动删除打印出的临时目录。不需要移除任何全局 Skill 或配置。

## 项目状态

这次预发布在完整验收前提供本地安装试用。它不是稳定版；公开发布不表示剩余检查已经通过。

目前已完成独立分发边界整理、来源标注审查，以及候选的文件、链接和路由静态检查。最终运行行为与宿主发现检查尚未完成，真实工程效果也未评估。

本项目不宣称已证明质量提高、速度加快或成本降低。当前边界见 [STATUS.md](STATUS.md)。

## 许可与反馈

本仓库的原创 Skill 文本、介绍文字和演示素材采用 [MIT 许可证](LICENSE)。该授权不改变第三方作品的权利，详见 [NOTICE.md](NOTICE.md)。

欢迎在 Issues 提出问题或针对项目方向给出具体反馈。请使用原创虚构例子，不要提交私有源码、生产日志、个人信息或受版权限制的原文。
