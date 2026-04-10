# 贝佐斯致股东信知识库

> 把杰夫·贝佐斯 1997-2020 年的 24 封亚马逊股东信，变成一座可点击、可漫游的知识城堡。

**在线访问**：https://bezos.feima.ai/

## 这是什么

把贝佐斯 24 年的股东信全部翻译成中文，提取出反复出现的核心概念、亚马逊的产品/业务、关键人物，构建成一个互相交叉链接的知识图谱网站。

灵感来源于 [巴菲特致股东信知识库](https://buffett-letters-eir.pages.dev/)（by 邦比快跑），并参考其视觉设计。

## 项目内容

- **24 封股东信** — 1997-2020 完整中文翻译
- **16 个核心概念** — 客户至上、长期主义、Day 1、飞轮效应、自由现金流、逆向工作法、高标准、一类决策与二类决策、发明与失败、低价策略、自助服务平台、数据驱动决策、漫游、气候承诺、创造大于消耗、差异化即生存
- **15 项亚马逊产品/业务档案** — 亚马逊、AWS、Prime、Kindle、FBA、Marketplace、KDP、Alexa、Amazon Go、Whole Foods、Amazon Studios、Zappos、Fire TV、Amazon Logistics、Mechanical Turk
- **4 位关键人物** — 贝佐斯、安迪·贾西、杰夫·威尔克、本杰明·格雷厄姆
- **789+ 条交叉链接** — 概念-公司-人物-信件之间互相引用

## 目录结构

```
├── vault/              # Obsidian 知识库源文件（Markdown + YAML frontmatter）
│   ├── letters/        # 24 封股东信译文
│   ├── concepts/       # 16 个概念卡片
│   ├── companies/      # 15 项产品/业务档案
│   ├── people/         # 4 位人物档案
│   ├── index-pages/    # 索引页
│   └── 欢迎.md
├── site/               # 生成的静态 HTML 网站
├── build_site.py       # 静态网站生成器（Markdown → HTML）
├── DESIGN.md           # 设计系统参考（来自 awesome-design-md）
└── README.md
```

## 重新构建

需要 Python 3 和两个依赖：

```bash
pip install markdown pyyaml
python3 build_site.py
```

构建产物会输出到 `site/` 目录，直接用任何静态文件服务器（Caddy / nginx / Cloudflare Pages 等）托管即可。

## 网站特性

- **左侧深海军蓝导航栏** — 按"索引/股东信/概念/产品/人物"分组
- **右侧反向链接面板** — 每个页面自动显示所有引用它的其他页面，可折叠展开（基于 Obsidian `[[wikilinks]]` 计算）
- **首页** — Hero 区 + 数据统计 + 快速导航卡片 + 概念/产品 TOP 15 标签云 + 关键人物
- **优雅的中文衬线字体** — Noto Serif SC 用于标题，DM Sans 用于正文
- **响应式** — 支持移动端

## 致谢

- 设计灵感与视觉参考：[巴菲特致股东信知识库](https://buffett-letters-eir.pages.dev/) by [邦比快跑](https://mp.weixin.qq.com/s/UD2k4ZgkjC30lwXmdsZj5Q)
- 设计系统：[awesome-design-md](https://github.com/VoltAgent/awesome-design-md)
- 使用 [Claude Code](https://claude.com/claude-code) 协作完成翻译、概念提取、知识图谱构建和网站开发
