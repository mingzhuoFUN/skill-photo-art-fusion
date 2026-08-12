# 实景共绘 · Photo Art Fusion

通过虚实结合的方式，在保留你的照片主体的情况下，对剩余的非主体元素进行艺术创作的skill

它不是简单套滤镜，而是在保留照片身份、主体关系与空间逻辑的基础上，选择适合的主创区域，加入和你照片本身相符的艺术风格。

## 核心能力

- **虚实结合**：保留决定照片身份的真实内容，在适合的区域建立明确艺术创作点。
- **主体分级保护**：区分身份主体、情境人物和偶然人物，避免“画面里有人就全部锁死”。
- **结构驱动创作**：没有明显主体时，根据线条、轮廓、分割、包围、重复和空间关系建立创作焦点。
- **主创与承接区域**：主创区完整表达艺术语言，其他候选区域以较低强度呼应和衬托。
- **摄影修复与再创作**：主动处理阴影、曝光、色偏、杂乱等问题，并可将问题区域转化为创作载体。
- **名作与艺术语言匹配**：根据具体主体、场景、构图、色彩和情绪选择名作、艺术家或流派作为锚点。
- **同源发散**：从原图提取形态、色彩、材质、光线、空间或意象，生成原图没有但来源关系清晰的新元素。
- **密度控制**：避免全图同质化纹理、多个竞争中心和无来源元素堆砌。

## 仓库结构

```text
skill-photo-art-fusion/
├── README.md                         # 中文项目介绍
├── index.html                        # GitHub Pages 首页
└── photo-art-fusion-zh/              # 可安装的完整 Skill 包
    ├── SKILL.md                      # 触发描述与核心工作流
    └── agents/
        └── openai.yaml               # Codex UI 展示与默认提示词
```

`README.md` 和网站文件位于 Skill 包之外，不会在 Skill 触发时占用运行上下文。

## 安装


最简单的使用方式是复制github链接给你的AI 例如codex Claude code 等让其读取并应用这个skill

链接：
https://github.com/mingzhuoFUN/skill-photo-art-fusion

### 方法一：克隆后复制

```powershell
git clone https://github.com/mingzhuoFUN/skill-photo-art-fusion.git
Copy-Item -Recurse -Force .\skill-photo-art-fusion\photo-art-fusion-zh "$env:USERPROFILE\.codex\skills\photo-art-fusion-zh"
```

重新打开 Codex，使其发现新安装的 Skill。

### 方法二：手动安装

下载本仓库，将 `photo-art-fusion-zh` 整个目录复制到：

```text
C:\Users\你的用户名\.codex\skills\photo-art-fusion-zh
```

不要只复制 `SKILL.md`；`agents/openai.yaml` 也属于完整结构的一部分。

## 使用方式

上传一张照片后，直接让AI按照skill 创作即可



## 隐私原则

Skill 将用户上传并要求修改视为当前编辑授权，只向图像生成服务发送必要图片和最终提示词；默认保留原图并另存结果，不覆盖原文件。

## 当前状态

这是一个持续通过真实照片测试和迭代的实验性 Skill，重点评估创作可见性、主体保持、区域层级、艺术融合、审美修复与运行效率。

