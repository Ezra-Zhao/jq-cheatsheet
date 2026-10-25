# jq 命令速查表 · jq Cheatsheet

[![Stars](https://img.shields.io/github/stars/Ezra-Zhao/jq-cheatsheet?style=social)](https://github.com/Ezra-Zhao/jq-cheatsheet/stargazers) [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE) ![Languages](https://img.shields.io/badge/languages-3-blue)

Support & more: [GitHub Sponsors](https://github.com/sponsors/Ezra-Zhao) · [Gumroad — templates & workbooks I use](https://ezraflow28.gumroad.com) · [Ko-fi](https://ko-fi.com/ezra777zhao)


> 🌍 [Español](README.es.md) · [Português](README.pt.md)

一份**一页纸**的 jq 速查表：30 条全部真实跑通过的 filter（jq 1.7 实测），每个条目只讲三件事——**它是干什么的、一条能直接复制粘贴的命令、适用场景标签**。不编造函数，不拼凑语法。

## 面向谁

后端开发者、运维/SRE，以及每天跟 JSON 打交道的你。如果你每次解析 API 返回都要现查 jq 语法，这张表能让你把最常用的 filter 一次记牢。

## 怎么用

1. 直接看 **[CHEATSHEET.md](CHEATSHEET.md)** ——速查表正文，英文 filter 全球开发者都无压力。
2. 先装好 jq：macOS 用 `brew install jq`，Debian/Ubuntu 用 `sudo apt install jq`。
3. 把文末的示例 `config.json` 存下来，每条 filter 亲手跑一遍，一小时就顺手了。

## 30 秒上手

```bash
echo '{"name":"api-server","port":8080}' | jq '.name'    # -> "api-server"
echo '{"name":"api-server","port":8080}' | jq -r '.name'  # -> api-server（去引号，可直接喂给 shell）
```

## 收录了什么

| 分类 | 内容 |
|---|---|
| 📥 基础 | 美化输出、取字段、`-r` 裸输出、`-c` 紧凑输出（4 条） |
| 🧭 嵌套与数组 | 深层路径、数组下标、`.[]` 展开、`length` 计数（4 条） |
| 🔎 过滤 | `select` 数值/字符串/组合条件（3 条） |
| 🔄 变换 | `map` 取字段、重塑结构、加计算字段（3 条） |
| 🔗 管道与构造 | `|` 串联、`{a, b}` 简写、拼装汇总对象（3 条） |
| 🔤 字符串与数字 | `tostring`/`tonumber`、`split`/`join`、正则 `test()`（3 条） |
| 📊 聚合 | 排序、去重、分组计数、求和、取最大最小（5 条） |
| 🗝️ 键操作 | `keys`/`has`/`del`（1 条） |
| 🛠️ 实战 | `curl \| jq` 一条龙、日志统计、`--arg` 传变量、`--slurp` 合并（4 条） |

所有 filter 均用 jq 1.7 对真实数据逐条跑通，示例输入输出写在注释里。

## 为什么是这 30 条

- **高频优先**：每一类都是日常真实会敲的命令，没有"看起来厉害但用不上"的冷门函数。
- **实战收尾**：最后 4 条是生产环境真实场景（调 API、看日志、shell 传参），学完即用。

## 欢迎 PR

发现 filter 写错了、缺了常用场景、翻译不到位——欢迎提 Pull Request。新增条目请保持统一格式（功能 / 命令 / 标签），**提交前请用真实 jq 跑一遍验证**。

## 📚 更多速查表

同一作者的其他速查表，同样有中/西/葡三语版本：

- [FFmpeg 命令速查表](https://github.com/Ezra-Zhao/ffmpeg-cheatsheet) — 28 条音视频处理命令
- [Git 实战速查表](https://github.com/Ezra-Zhao/git-cheatsheet) — 30 条日常+救命命令
- [Docker 命令速查表](https://github.com/Ezra-Zhao/docker-cheatsheet) — 28 条容器命令
- [curl 命令速查表](https://github.com/Ezra-Zhao/curl-cheatsheet) — 29 条 API 调试命令
- [正则表达式速查表](https://github.com/Ezra-Zhao/regex-cheatsheet) — 30 条实战正则模式
- [终端神器速查表](https://github.com/Ezra-Zhao/terminal-superpowers-cheatsheet) — 14 个终端效率工具
- [Adobe 免费替代速查表](https://github.com/Ezra-Zhao/adobe-free-alternatives-cheatsheet) — 16 个 Adobe 免费替代品
- [退订省钱速查表](https://github.com/Ezra-Zhao/desubscribe-cheatsheet) — 10 组退订替代，年省约 $1,260
- [kubectl 命令速查表](https://github.com/Ezra-Zhao/kubectl-cheatsheet) — Kubernetes 常用命令速查
- [SQL 查询速查表](https://github.com/Ezra-Zhao/sql-cheatsheet) — 常用 SQL 查询与函数速查
- [SSH 命令速查表](https://github.com/Ezra-Zhao/ssh-cheatsheet) — 28 条 SSH 连接、密钥与隧道命令
- [Vim 命令速查表](https://github.com/Ezra-Zhao/vim-cheatsheet) — 30 条编辑、搜索替换与宏命令
- [tmux 命令速查表](https://github.com/Ezra-Zhao/tmux-cheatsheet) — 30 条会话、窗口与窗格命令
- [systemd 命令速查表](https://github.com/Ezra-Zhao/systemd-cheatsheet) — 30 条服务管理与日志命令

## License

MIT © 2026 Guangyi Zhao，详见 [LICENSE](LICENSE)。
