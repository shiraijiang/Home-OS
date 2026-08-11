# 06 Backlog

这里只放已经明确推迟或尚未确认的内容。Backlog 不等于承诺开发。

## 已明确推迟

- 家务 / 家政角
- 大桌
- 穿搭 / 衣架功能化
- 图鉴 / 书堆功能化
- 季节切换相关扩展
- 未来「隐居地」功能
- 房间画风切换功能

## 已预留但当前不启用

### 隐居地入口

物理入口固定为扫地机器人充电口 / 充电座。当前版本只作为正常充电设施存在，不可点、无提示。未来功能启用时再定义进入方式、场景和返回逻辑。

### 可切换画风

当前只完成 Default 方向。`assets/reference/style-reference-alt-01.PNG` 仅作为未来备选画风方向参考。

未来新增画风时：

- 原则上保持家具语义、主要布局和功能坐标一致。
- 每套画风独立维护 style reference、palette 和必要 sprite 规则。
- 不要求第一版实现换肤系统。

## 尚未确认

### 冰箱顶固定装饰

需要确认具体物件、数量、位置和轮廓。确认后转入 `04-art.md` 的 Base 规格并追加决定日志。

### 正式调色板

`assets/palette.json` 已建立，但当前只记录「尚未锁定」状态。Base 母版稳定后再测试并写入正式颜色，不提前拍脑袋定 HEX 和色数。

### 像素处理脚本

决定流程仍为：中值滤波 → 降采样 → 调色板量化。

`tools/pixelize.py` 尚未创建，因为项目还未进入代码执行阶段。等 Base 与正式 palette 确认后再实现，避免先写一个和最终素材不匹配的脚本。

## 已完成，不再作为 Backlog

- `assets/reference/scene-master-default.PNG` 已入库。
- `assets/reference/pixel-style-reference.PNG` 已入库。
- `assets/reference/style-reference-alt-01.PNG` 已入库。
