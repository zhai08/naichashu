# 奶茶鼠桌宠

奶茶鼠桌宠是一个基于 PyQt5 的 Windows 桌面陪伴小程序。它会常驻桌面，随机切换奶茶鼠 GIF/PNG 表情，支持拖动、边缘移动、打字陪写气泡、成长等级、金币扭蛋机、可拖动配饰和大模型 API 对话。

## 免编程下载运行

普通用户不需要安装 Python，也不需要打包。

在 GitHub 下载项目 ZIP 后，解压并双击运行：

```text
release\奶茶鼠桌宠.exe
```

首次运行后，程序会在 exe 同目录生成本地存档和 AI 配置：

- `naicha_mouse_profile.json`
- `naicha_mouse_ai_config.json`

这两个文件用于保存等级、金币、抽奖、配饰位置和 API 设置。

## 素材预览

<p>
  <img src="IMG_5791/%E9%9D%99%E6%80%81%E5%8D%96%E8%90%8C.png" width="120" alt="静态卖萌">
  <img src="IMG_5791/%E5%8D%96%E8%90%8C.GIF" width="120" alt="卖萌">
  <img src="IMG_5791/%E5%A4%A7%E5%93%AD.GIF" width="120" alt="大哭">
  <img src="IMG_5791/%E7%82%B9%E5%A4%B4.GIF" width="120" alt="点头">
  <img src="IMG_5791/%E9%80%81%E4%BD%A0%E8%8A%B1%E8%8A%B1.GIF" width="120" alt="送你花花">
  <img src="IMG_5791/%E5%AD%A6%E4%B9%A0%E4%B8%AD.GIF" width="120" alt="学习中">
</p>

<p>
  <img src="IMG_5791/%E5%90%AF%E5%8A%A8%E7%9A%84%E6%97%B6%E5%80%99%E5%B1%95%E7%A4%BA%E8%B5%B7%E4%B8%8D%E6%9D%A5.GIF" width="120" alt="启动起床">
  <img src="IMG_5791/%E6%88%91%E6%9D%A5%E4%BA%86.GIF" width="120" alt="我来了">
  <img src="IMG_5791/%E6%94%BE%E7%83%9F%E8%8A%B1.GIF" width="120" alt="放烟花">
  <img src="IMG_5791/%E8%B7%B3%E4%B8%80%E8%B7%B3.GIF" width="120" alt="跳一跳">
  <img src="IMG_5791/%E6%84%89%E5%BF%AB%E9%A3%9E%E5%A4%A9.GIF" width="120" alt="愉快飞天">
  <img src="IMG_5791/%E9%80%80%E5%87%BA%E6%97%B6%E5%B1%95%E7%A4%BA%E5%86%8D%E8%A7%81.GIF" width="120" alt="退出再见">
</p>

配饰示例：

<p>
  <img src="accessories/crown_small.png" width="90" alt="小皇冠">
  <img src="accessories/crown_full_sugar.png" width="90" alt="满糖皇冠">
  <img src="accessories/glasses_study.png" width="90" alt="学习眼镜">
  <img src="accessories/flower_clip.png" width="90" alt="小花发夹">
  <img src="accessories/milk_tea_hat.png" width="90" alt="奶茶帽">
  <img src="accessories/lucky_star_halo.png" width="90" alt="欧气星环">
</p>

## 快速开始

1. 安装 Python 3.10 或更高版本。
2. 在项目目录安装依赖：

```bat
pip install -r requirements.txt
```

3. 双击运行：

```bat
run_naicha_mouse.bat
```

也可以在命令行运行：

```bat
python main.py
```

## 主要功能

- 启动动画：先播放 `启动的时候展示起不来.GIF`，再播放 `我来了.GIF`。
- 退出动画：右键退出后播放 `退出时展示再见.GIF`，约 3.5 秒后关闭。
- 常规随机：日常、休息、吃饭、学习、工作和低概率事件表情会按权重切换。
- 打字陪写：检测键盘节奏，显示安全拟态气泡，不显示真实输入内容。
- 移动模式：支持停止移动、底部散步、边缘巡游和召唤回来。
- 大小档位：30%、40%、50%、60%、70%、80%、90%、100%。
- 成长系统：记录等级、互动值、金币、陪伴时间和今日专注次数。
- 扭蛋机：消耗金币抽取配饰、称号、演出、语言奖励和奶茶碎片。
- 配饰系统：抽到配饰后可佩戴、隐藏、缩放，右键长按配饰可拖动调整位置。
- 气泡样式：抽到气泡边框后，可在右键菜单切换奶盖气泡等样式。
- 演出收藏：抽到演出奖励后，可在右键菜单中回放收藏演出。
- AI 聊天：可配置 OpenAI-compatible、Claude Messages 或 Gemini generateContent 接口，与奶茶鼠对话。

## 右键菜单

- `摸摸奶茶鼠`
- `喂点东西`
- `送你花花`
- `开始专注` / `结束专注`
- `休息一下`
- `久坐伸展`
- `鼓励我一下`
- `庆祝一下`
- `状态面板`
- `气泡样式`
- `演出收藏`
- `AI 聊天`
- `奶茶鼠扭蛋机`
- `配饰`
- `称号`
- `关闭/开启打字跟随`
- `关闭/开启打字气泡`
- `换个常驻动作`
- `召唤回来`
- `移动模式`
- `大小`
- `透明度`
- `退出`

## 成长和金币规则

互动值用于升级，金币用于扭蛋。获得互动值时，会同步获得等量金币。

| 行为 | 奖励 |
|---|---:|
| 每日首次启动 | +10 互动值，+10 金币 |
| 陪伴 10 分钟 | +5 互动值，+5 金币 |
| 摸摸 | +2 互动值，+2 金币 |
| 喂食 | +5 互动值，+5 金币 |
| 送花 | +5 互动值，+5 金币 |
| 庆祝 | +3 互动值，+3 金币 |
| 完成一次专注 | +25 互动值，+25 金币 |

规则说明：

- 等级上限为 52。
- 互动操作每日上限为 200 互动值。
- 陪伴时长获得的互动值和金币无每日上限。
- 升级所需互动值公式：

```text
required_exp = int(55 + level * level * 0.25 + level * 18)
```

## 奶茶鼠扭蛋机

| 抽取方式 | 消耗 |
|---|---:|
| 每日首抽 | 20 金币 |
| 单抽 | 30 金币 |
| 十连 | 270 金币 |

奖池概率：

| 档位 | 概率 | 内容 |
|---|---:|---|
| 普通 | 68% | 小互动值、金币返还、奶茶碎片、即时台词、普通口头禅 |
| 稀有 | 24% | 临时配饰、稀有口头禅、气泡边框、稀有演出 |
| 超稀有 | 7% | 永久配饰、特殊口头禅包、称号、特殊演出收藏 |
| 隐藏 | 1% | 隐藏配饰、隐藏称号、隐藏语言、大奖礼包 |

十连至少包含 1 个稀有及以上奖励。60 抽未出超稀有及以上时，下一个稀有及以上结果会升级为超稀有。

隐藏档里的 `满糖大奖礼包` 会一次性获得：

- 互动值 +520
- 金币 +520
- 奶茶碎片 +52
- 隐藏配饰：满糖皇冠、欧气星环
- 隐藏称号：今日欧气鼠
- 气泡样式：永久奶盖气泡边框
- 演出收藏：愉快飞天庆祝
- 隐藏口头禅：满糖鼠鼠语、欧气播报、神秘咒语

## AI 聊天配置

右键选择 `AI 聊天` -> `配置 API`，填写：

- 接口格式：OpenAI-compatible、Anthropic Claude Messages 或 Google Gemini generateContent。
- Base URL：按服务商控制台提供的地址填写。
- 模型名：按服务商控制台支持的模型名填写。
- API Key：只保存在本地 `naicha_mouse_ai_config.json`，不会写入项目仓库。

可选 API 推荐：

- [Right Code AI Agent 中转平台](https://www.right.codes/register?aff=05fac8f2)
- [PackyAPI AI API 服务](https://www.packyapi.com/register?aff=xec9)

如果使用第三方中转平台，建议优先选择 OpenAI-compatible 格式，并在平台控制台复制对应的 Base URL、API Key 和模型名。

## 配饰说明

气泡边框抽到后可在右键菜单 `聊天和成长` -> `气泡样式` 中切换。奶盖气泡会带浅奶盖渐变、焦糖描边和右上角小装饰，状态面板也会同步使用当前气泡样式。

配饰透明 PNG 放在 `accessories/`，配饰位置和默认尺寸写在 `naicha_mouse_accessories.json`。

已包含的配饰素材包括：

- 小皇冠、满糖皇冠
- 学习眼镜、耳机、工作牌
- 睡帽、云朵睡帽、奶茶帽
- 星星发夹、小花发夹、粉色蝴蝶结
- 奶茶杯挂件、小背包、围巾
- 欧气星环、守护披风、彩虹贴纸

右键菜单进入 `配饰` 可切换显示、缩放、重置位置或佩戴已有配饰。右键长按当前配饰可以拖动位置。

## 文件结构

| 路径 | 说明 |
|---|---|
| `main.py` | 桌宠主程序 |
| `run_naicha_mouse.bat` | Windows 双击启动脚本 |
| `build_exe.bat` | Windows 一键打包脚本 |
| `requirements.txt` | Python 依赖 |
| `release/` | 可直接双击运行的 exe |
| `IMG_5791/` | 奶茶鼠 GIF/PNG 表情素材 |
| `accessories/` | 透明 PNG 配饰素材 |
| `app_icon.ico` | exe 图标，来自 `IMG_5791/静态卖萌.png` |
| `naicha_mouse_state_map.json` | 状态、素材、随机池和触发配置 |
| `naicha_mouse_dialogues.json` | 气泡文案池 |
| `naicha_mouse_gacha_pool.json` | 扭蛋机奖池、概率和奖励配置 |
| `naicha_mouse_accessories.json` | 配饰默认位置、尺寸和素材文件 |

运行后会自动生成本地数据文件：

| 路径 | 说明 |
|---|---|
| `naicha_mouse_profile.json` | 等级、互动值、金币、陪伴时间和抽奖数据 |
| `naicha_mouse_ai_config.json` | AI 聊天 API 配置 |

这两个文件属于个人本地数据，已经写入 `.gitignore`。

## 自定义

修改状态素材：

```json
{
  "id": "idle_static_cute",
  "file": "静态卖萌.png"
}
```

常规随机由 `naicha_mouse_state_map.json` 里的 `randomGroups` 控制总权重，由每个状态的 `random_group` 和 `random_weight` 控制分组和组内权重。

修改气泡文案：编辑 `naicha_mouse_dialogues.json`。

修改奖池：编辑 `naicha_mouse_gacha_pool.json`。

修改配饰位置和默认尺寸：编辑 `naicha_mouse_accessories.json`。

## Star 趋势

[![Star History Chart](https://api.star-history.com/svg?repos=Xzyery/naichashu&type=Date)](https://star-history.com/#Xzyery/naichashu&Date)
