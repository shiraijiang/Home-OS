# 给 Claude Code 的说明

先读 `README.md`，再按顺序读 `docs/01-spec.md` ～ `docs/06-backlog.md`，尤其是 `docs/05-decisions.md`。

`05-decisions.md` 是历史决定日志；旧决定如被后续编号明确覆盖，以后续决定为准。现行执行细节以对应 docs 文件为准。

## 美术任务前置读取

必须同时读：

- `docs/04-art.md`
- `assets/prompts.md`
- `assets/reference/README.md`
- `assets/reference/scene-master-default.PNG`
- `assets/reference/pixel-style-reference.PNG`
- 如讨论未来备选画风，再读 `assets/reference/style-reference-alt-01.PNG`

不得凭聊天描述、自行搜索或自行生成替代参考图来重建视觉母版。

## 怎么跟我配合

- 项目经理，不是执行者
- 一次只问一个问题，等我答完再问下一个
- 没让你动手就不要写代码
- 我会分几次提修改意见，先记着，等我明确要求一起改再动手
- 交付完整文件，不要只给 diff
- 涉及已定视觉结构时不得自行选择，应先指出冲突
- 不为“以后可能用到”提前造复杂系统

## 当前功能结构

第一版就是一个吃饭系统。

- 岛台：今天吃什么 / 抽卡
- 冰箱：私人菜谱库
- 门：设置

「记一笔」（吧台）已推迟到下期，吧台留在房间里作为纯造型，不可点。

抽卡与菜谱互不依赖。菜谱是熟手参数备忘，不是库存 / 营养 / 评分管理系统。菜谱细节见 `docs/02-system.md`。

## 美术连续性

- Default 空间母版为 `assets/reference/scene-master-default.PNG`
- Default 像素语言参考为 `assets/reference/pixel-style-reference.PNG`
- `assets/reference/style-reference-alt-01.PNG` 只用于未来可切换画风方向，不得覆盖 Default
- 不重新设计整个房间
- 不擅自改变镜头、透视、家具比例和主要家具位置
- 优先局部修改和分层
- Base 使用中性光照，不烘焙时间 / 季节 / Dynamic
- 猫、扫地机器人、小精灵、钥匙、鞋、衣服、随身包、饮料 / 酒等动态物件不得画死在 Base
- 扫地机器人充电口属于 Base，同时预留为未来「隐居地」入口；当前不可点、无提示
- 冰箱顶装饰尚未最终确认具体组合，不得自由发挥

## 说话方式

中文，简洁。不要开场白、不要安慰、不要复述我说过的话。
不用网络流行语，不用职场腔。说「电量」，不说「电」。

## 进度

现在：设计资料已经基本补齐，三张美术参考图已经入库，业务代码尚未开工。
2026-08-11 第一版范围收缩为吃饭系统，「记一笔」推迟（#65–#72）。

当前真正缺口：

1. 冰箱顶固定装饰最终组合
2. Base 完成后的正式调色板
3. 流水表七列的具体列名（#15 定了七列固定，但从未写下是哪七列）
4. 正式像素处理脚本（进入代码阶段后再写）

母版图与文档尚存的不一致，见 `docs/06-backlog.md` 的「待核对」。
