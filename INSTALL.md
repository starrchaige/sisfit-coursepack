# INSTALL

本文档说明如何在其他电脑上安装 `sisfit-coursepack`。

## 压缩包内容

解压后你应该看到：

```text
sisfit-coursepack/
```

目录中至少应包含：

- `SKILL.md`
- `README.md`
- `README_EN.md`
- `INSTALL.md`
- `CONTRIBUTING.md`
- `examples.json`
- `boundary_checklist.md`
- `xiaohongshu_post.md`
- `LICENSE`

## 通用安装步骤

1. 解压 zip
2. 找到目标工具的 `skills` 目录
3. 将整个 `sisfit-coursepack/` 目录复制进去
4. 重启工具，或新开一个会话，让它重新扫描技能目录

注意：

- 不要只复制 `SKILL.md`，要复制整个 `sisfit-coursepack/` 目录
- 如果目标电脑里已经有同名目录，先备份旧版本，再决定覆盖
- 如果你的工具使用 profile 隔离，优先放到对应 profile 的 `skills` 目录

## 平台路径速查

下面是常见默认路径示例。

### macOS / Linux

- Trae: `~/.trae/skills/`
- Claude Code: `~/.claude/skills/`
- Codex: `~/.codex/skills/`
- Hermes: `~/.hermes/skills/`
- OpenClaw: `~/.openclaw/skills/`

### Windows

- Trae: `%USERPROFILE%\\.trae\\skills\\`
- Claude Code: `%USERPROFILE%\\.claude\\skills\\`
- Codex: `%USERPROFILE%\\.codex\\skills\\`
- Hermes: `%USERPROFILE%\\.hermes\\skills\\`
- OpenClaw: `%USERPROFILE%\\.openclaw\\skills\\`

如果是 profile 隔离模式，优先使用对应 profile 下的 `skills` 目录。

## macOS / Linux 一键安装命令

下面的命令假设你当前就在 zip 所在目录，并且 zip 文件名为：

```text
sisfit-coursepack_v0.2.0.zip
```

命令逻辑是：

1. 临时解压 zip
2. 创建目标 `skills` 目录
3. 覆盖旧版 `sisfit-coursepack`
4. 复制新版目录
5. 清理临时目录

### Trae

```bash
ZIP="sisfit-coursepack_v0.2.0.zip"; TARGET="$HOME/.trae/skills"; TMPDIR="$(mktemp -d)" && unzip -q "$ZIP" -d "$TMPDIR" && mkdir -p "$TARGET" && rm -rf "$TARGET/sisfit-coursepack" && cp -R "$TMPDIR/sisfit-coursepack" "$TARGET/" && rm -rf "$TMPDIR"
```

### Claude Code

```bash
ZIP="sisfit-coursepack_v0.2.0.zip"; TARGET="$HOME/.claude/skills"; TMPDIR="$(mktemp -d)" && unzip -q "$ZIP" -d "$TMPDIR" && mkdir -p "$TARGET" && rm -rf "$TARGET/sisfit-coursepack" && cp -R "$TMPDIR/sisfit-coursepack" "$TARGET/" && rm -rf "$TMPDIR"
```

### Codex

```bash
ZIP="sisfit-coursepack_v0.2.0.zip"; TARGET="$HOME/.codex/skills"; TMPDIR="$(mktemp -d)" && unzip -q "$ZIP" -d "$TMPDIR" && mkdir -p "$TARGET" && rm -rf "$TARGET/sisfit-coursepack" && cp -R "$TMPDIR/sisfit-coursepack" "$TARGET/" && rm -rf "$TMPDIR"
```

### Hermes

```bash
ZIP="sisfit-coursepack_v0.2.0.zip"; TARGET="$HOME/.hermes/skills"; TMPDIR="$(mktemp -d)" && unzip -q "$ZIP" -d "$TMPDIR" && mkdir -p "$TARGET" && rm -rf "$TARGET/sisfit-coursepack" && cp -R "$TMPDIR/sisfit-coursepack" "$TARGET/" && rm -rf "$TMPDIR"
```

如果你使用 profile 目录，把 `TARGET="$HOME/.hermes/skills"` 改成：

```bash
TARGET="$HOME/.hermes/profiles/<profile>/skills"
```

### OpenClaw

```bash
ZIP="sisfit-coursepack_v0.2.0.zip"; TARGET="$HOME/.openclaw/skills"; TMPDIR="$(mktemp -d)" && unzip -q "$ZIP" -d "$TMPDIR" && mkdir -p "$TARGET" && rm -rf "$TARGET/sisfit-coursepack" && cp -R "$TMPDIR/sisfit-coursepack" "$TARGET/" && rm -rf "$TMPDIR"
```

## 1. Trae

默认安装路径：

```text
~/.trae/skills/
```

示例：

```bash
mkdir -p ~/.trae/skills
cp -R sisfit-coursepack ~/.trae/skills/
```

Windows 路径示例：

```text
%USERPROFILE%\.trae\skills\
```

安装后目标目录应为：

```text
~/.trae/skills/sisfit-coursepack/
```

## 2. Claude Code

常见安装路径：

```text
~/.claude/skills/
```

示例：

```bash
mkdir -p ~/.claude/skills
cp -R sisfit-coursepack ~/.claude/skills/
```

Windows 路径示例：

```text
%USERPROFILE%\.claude\skills\
```

如果你在使用项目级或 profile 级 skills 目录，放到对应目录即可。

## 3. Codex

常见安装路径：

```text
~/.codex/skills/
```

示例：

```bash
mkdir -p ~/.codex/skills
cp -R sisfit-coursepack ~/.codex/skills/
```

Windows 路径示例：

```text
%USERPROFILE%\.codex\skills\
```

如果你的 Codex 环境把技能目录映射到其他位置，以你现有安装为准。

## 4. Hermes

常见安装路径：

```text
~/.hermes/skills/
```

如果是 profile 隔离环境，也可能是：

```text
~/.hermes/profiles/<profile>/skills/
```

示例：

```bash
mkdir -p ~/.hermes/skills
cp -R sisfit-coursepack ~/.hermes/skills/
```

Windows 路径示例：

```text
%USERPROFILE%\.hermes\skills\
```

如果你使用的是 profile home，优先复制到对应 profile 的 `skills` 目录。

## 5. OpenClaw

常见安装路径：

```text
~/.openclaw/skills/
```

示例：

```bash
mkdir -p ~/.openclaw/skills
cp -R sisfit-coursepack ~/.openclaw/skills/
```

Windows 路径示例：

```text
%USERPROFILE%\.openclaw\skills\
```

如果你的 OpenClaw 环境有单独的导入目录或 profile 目录，以实际配置为准。

## 6. 其他兼容工具

如果某个工具也采用“目录即 skill、`SKILL.md` 为入口”的约定，通常可以按下面方式安装：

```text
<tool-home>/skills/sisfit-coursepack/
```

关键是保持：

- 顶层目录名为 `sisfit-coursepack`
- `SKILL.md` 位于该目录根部
- 其余配套文档文件一并保留

## 快速校验

安装后至少检查两件事：

1. 目录存在，例如：

```bash
ls ~/.trae/skills/sisfit-coursepack
```

2. `SKILL.md` 头部可读，例如：

```bash
sed -n '1,12p' ~/.trae/skills/sisfit-coursepack/SKILL.md
```

你应能看到类似内容：

```text
name: "sisfit-coursepack"
version: 0.2.0
status: public_skill_v0_2
```

## 升级旧版本

如果目标电脑已经安装过旧版：

1. 先备份旧目录
2. 删除或移走旧的 `sisfit-coursepack/`
3. 再复制新版目录
4. 重启工具或新开会话

示例：

```bash
mv ~/.trae/skills/sisfit-coursepack ~/.trae/skills/sisfit-coursepack.backup
cp -R sisfit-coursepack ~/.trae/skills/
```

## 故障排查

如果安装后看不到这个 skill，优先检查：

- 是否复制了整个目录，而不是只复制单个文件
- 目录名是否仍然是 `sisfit-coursepack`
- `SKILL.md` 是否在目录根部
- 是否放到了正确的 `skills` 目录
- 工具是否需要重启或重新打开会话
