# 素材标签与使用说明

交付共21张独立RGBA PNG：13种角色、8种道具。中文标签在本文件、JSON和预览图中，标签没有写进透明素材。原始三张洋红底图片保留在sources目录。

## 对齐

角色画布512×640，脚底锚点(256,608)。所有姿势以相同尺寸显示，切图不重算object-fit。锚点映射公式：left=目标脚底x−256×scale；top=目标脚底y−608×scale。transform-origin:50% 95%。

道具画布512×512，底部锚点(256,480)。饭碗系列和饼干系列分别统一宽度，切换满饭/剩饭或完整/缺口饼干时使用相同外层位置和缩放。原生成图的碗形与角度有细微差别，采用硬切，不做连续变形。

## 文件标签

| ID | 中文标签 | 路径 | 用途 |
|---|---|---|---|
| idle | 期待 | assets/characters/whale_idle.png | 开场、等待 |
| confused | 困惑 | assets/characters/whale_confused.png | 红绿灯、装犹豫 |
| excited | 秒懂兴奋 | assets/characters/whale_excited.png | 白米饭、Token饼干、抢答 |
| stunned | 失败呆住 | assets/characters/whale_stunned.png | 失败、定格、可灰度化 |
| pretend | 尴尬假笑 | assets/characters/whale_pretend.png | 装人类、汗滴 |
| happy | 抱饭满足 | assets/characters/whale_happy.png | 通关、结尾、已含饭碗与Token饼干 |
| panic | 慌张 | assets/characters/whale_panic.png | 失败解冻、99%紧张 |
| hungry | 馋到流口水 | assets/characters/whale_hungry.png | 等开饭 |
| smug | 得意叉腰 | assets/characters/whale_smug.png | 秒选成功、提交前 |
| pout | 委屈鼓脸 | assets/characters/whale_pout.png | 套娃确认 |
| determined | 握拳下决心 | assets/characters/whale_determined.png | 决定装人类特写 |
| pray | 闭眼祈祷 | assets/characters/whale_pray.png | 99%等待 |
| victory | 开心比耶 | assets/characters/whale_victory.png | 通过瞬间 |
| rice_full | 满满大白米饭 | assets/props/rice_full.png | 验证码目标、满饭 |
| bowl_empty | 空饭碗 | assets/props/bowl_empty.png | 验证码干扰 |
| cookie_token | 完整Token饼干 | assets/props/cookie_token.png | 验证码目标、饼干特写 |
| cookie_token_bitten | 缺口Token饼干 | assets/props/cookie_token_bitten.png | 通关咔嚓特写 |
| cookie_plain | 普通无字饼干 | assets/props/cookie_plain.png | 验证码干扰 |
| toast | 吐司面包 | assets/props/toast.png | 验证码干扰、装点错 |
| noodles | 一碗面条 | assets/props/noodles.png | 验证码干扰 |
| rice_leftover | 少量剩饭 | assets/props/rice_leftover.png | 通关饭碗特写 |

## 特别注意

- happy图中的饭碗和饼干已经与人物合在一起，不能单独移动；独立食物图用于验证码和额外特写。
- stunned保持原彩色；失败时用CSS grayscale(1)整体转灰。panic与pretend图内已有汗滴，不要再重复加。
- 普通饼干cookie_plain没有Token字，正好作为干扰项；Token图中的文字不要重复绘制。
- previews中的背景格与标签仅用于预览。视频必须使用assets中的独立PNG。
- 原始人物间存在轻微绘画差异，已统一画布和脚底，建议漫画硬切，不做五官插值。

## 片尾图

assets/endcard/studio_trio.png：工作室片尾插画，保持完整比例。它是独立片尾背景，不属于13种角色或8个道具。显示时点见storyboard.json。
