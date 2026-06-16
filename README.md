This is a macOS-compatible fork of NaichaShu.
Original project: https://github.com/Xzyery/naichashu
Original author: Xzyery

# NaichaMouse macOS Safe Source Edition

奶茶鼠桌宠是一个基于 PyQt5 的桌面陪伴小程序。本分支在保留原有桌宠、动画、成长、扭蛋、配饰和 AI 聊天功能的基础上，加入了 macOS 兼容处理。

## 主要变化

- macOS 下不再加载 Windows `user32` API。
- macOS 下默认关闭全局打字检测、打字跟随和打字气泡计数。
- macOS 打包运行时，本地数据写入 `~/Library/Application Support/NaichaMouse/`，避免写入 `.app` 内部或桌面目录。
- Windows 下仍保留原来的全局打字跟随逻辑。

## 功能保留

- 桌宠窗口、拖动、置顶显示
- GIF/PNG 状态动画
- 启动动画、退出动画
- 右键菜单
- 随机动作和气泡台词
- 成长等级、经验、金币
- 专注计时、喝水提醒、久坐提醒
- 扭蛋机奖励
- 配饰显示、位置和缩放保存
- 气泡样式切换
- AI 聊天配置与对话

## macOS 安全说明

macOS 稳妥版不会申请或使用：

- 输入监控
- 辅助功能权限
- 摄像头
- 麦克风
- 定位
- 通讯录
- 管理员权限

AI 聊天只有在用户主动配置 API 后才会联网。API Key 会保存在本地配置文件中，不建议提交到仓库或发送给他人。

## 运行方式

建议使用 Python 3.10 到 3.12。若使用 Conda 的 Python 3.13，PyQt5 在 macOS 上可能出现 Qt `cocoa` 插件加载问题。

```bash
cd naichashu-main
python3 -m venv .venv
.venv/bin/python -m pip install -r requirements.txt
.venv/bin/python main.py
```

退出方式：右键奶茶鼠，选择 `退出`。

## 本地数据

源码方式运行时，本地数据默认保存在项目目录：

- `naicha_mouse_profile.json`
- `naicha_mouse_ai_config.json`

macOS `.app` 打包方式运行时，本地数据保存在：

```text
~/Library/Application Support/NaichaMouse/
```

这些文件用于保存等级、金币、配饰状态和 AI 配置，不应提交到 Git。

## 项目文件

```text
main.py
requirements.txt
IMG_5791/
accessories/
naicha_mouse_state_map.json
naicha_mouse_dialogues.json
naicha_mouse_gacha_pool.json
naicha_mouse_accessories.json
```

不要只复制 `main.py`。程序运行需要旁边的素材文件夹和 JSON 配置。
