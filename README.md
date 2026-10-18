# dsh-boot-suite-templates

> **DeepSeek Harness 开机动画的模板商店数据源**。不建服务器——客户端直接拉这个仓库的 `index.json`。

## 现在有

| 模板 | 作者 | 视觉基于 | 说明 |
|---|---|---|---|
| `deep-sonar` 深海声呐 | DeepSeek | 沈宏宏 | 深蓝底 + 浅蓝强调，五幕下潜叙事，自带六句英文播报（重档机械音色） |
| `archive-ink` 档案墨黑 | 沈宏宏（改色 LeeRolling） | — | 同「档案暖白」版式，强调色换成墨黑 + 深蓝，更冷、更像扫描件 |

> **作者字段的规矩**：基于别人作品改编的模板，`author` 写原作，`adaptedBy` 写改版者。
> 不要把他人的作品署成自己的。

## 目录约定

    index.json                 商店列表（唯一"数据库"）
    templates/<id>/
      template.json            模板本体（必需）
      preview.gif              动图预览（必需）
      preview.png              静帧（建议）
      LICENCE.txt              素材来源与授权（建议）

## 投稿

1. 在 `templates/` 下建一个文件夹，名字 = 模板 id（小写字母数字连字符）
2. 放进去 `template.json` + `preview.gif`（+ 可选静帧）
3. 在 `index.json` 的 `templates` 数组里加一行
4. 提 PR

格式规范见主仓库的 `docs/模板格式.md`。

## 硬约束

- 模板**只能是数据**，不允许任何代码
- 缺图缺音必须能跑（回落默认，绝不黑屏）
- `preview.gif ≤ 5 MB`，`assets/` 合计 ≤ 10 MB

## 客户端怎么读

    https://raw.githubusercontent.com/LeeRolling/dsh-boot-suite-templates/main/index.json

插件会把每个模板的 `template.json` 从这里安装到 `~/.dsh/startup-templates/<id>/`。