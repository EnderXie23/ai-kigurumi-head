# ai-kigurumi-head-reference

一个用于将动漫/游戏角色参考图转换为 **Kigurumi 头壳多视图参考图** 的 AI 图像生成工作流。

本项目不是 STL 自动建模工具，也不是 LoRA 训练项目。它的目标是提供一套可复用的 Prompt 工作流，帮助用户稳定生成可用于头壳定制沟通的参考图。

## 项目目标

输入：

- 角色 2D 官方图
- 游戏内 3D 截图
- 去遮挡角色头部图
- 优秀 Kigurumi 头壳案例图

输出：

- 去遮挡角色头部四视图
- Kigurumi 头壳四视图设计图
- 商品照风格四面或八面头壳参考图

## 核心思路

不要一步直接从角色图生成最终头壳图。

推荐流程：

1. **角色参考图 → 去遮挡角色头部四视图**
2. **角色头部四视图 → Kigurumi 头壳四视图设计图**
3. **Kigurumi 头壳设计图 → 商品照风格四面/八面图**

核心原则：

- 先稳定结构
- 再头壳化
- 最后商品照化
- 参考图必须明确分工
- 每次修正只解决一个主要问题

## 文件说明

```text
ai-kigurumi-head-reference/
├─ README.md
├─ SKILL.md
├─ LICENSE
├─ .gitignore
└─ prompts/
   ├─ step1-head-reference.md
   ├─ step2-kigurumi-design.md
   ├─ step3-product-view.md
   └─ troubleshooting.md
```

## 快速开始

1. 准备角色参考图。
2. 按照 `prompts/step1-head-reference.md` 生成去遮挡角色头部四视图。
3. 按照 `prompts/step2-kigurumi-design.md` 转换为 Kigurumi 头壳四视图设计图。
4. 按照 `prompts/step3-product-view.md` 生成商品照风格四面或八面视图。
5. 如果结果不理想，参考 `prompts/troubleshooting.md` 修改 Prompt。

## 素材准备建议

建议将素材分为以下几类：

```text
目标角色_头壳参考/
├─ 01_角色3D结构参考/
├─ 02_角色2D气质表情参考/
├─ 03_kigurumi优秀案例/
├─ 04_实际上传组合/
├─ 05_生成结果/
└─ 06_失败记录/
```

## 注意事项

- 不建议上传未授权的角色原图、游戏截图、店家商品图或他人私有生成图到公开仓库。
- 本仓库主要保存工作流和 Prompt，不保存完整聊天记录。
- 如果使用他人的图片作为参考，请遵守对应素材的版权与使用规则。
- 本项目输出结果仅作为设计沟通参考，不保证可直接用于生产或建模。

## License & Additional Terms

This project uses CC BY-NC 4.0 with additional community-use restrictions.

本项目采用 CC BY-NC 4.0 协议，并附带额外社区使用条款。

See:
- LICENSE
- ADDITIONAL_TERMS.md