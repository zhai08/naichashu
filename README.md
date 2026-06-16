NaichaMouse macOS Fork

这是一个基于 NaichaShu 的 macOS 兼容版本。

原项目：
https://github.com/Xzyery/naichashu

原作者：
Xzyery

本 Fork 的主要目标是让项目能够在 macOS 上正常运行，同时移除部分 Windows 专用功能和不必要的敏感权限需求。

⸻

功能

本版本保留了原项目的大部分功能：

* 桌宠动画与状态切换
* 拖动、置顶显示
* 随机动作与气泡台词
* 成长等级、经验、金币系统
* 专注计时
* 喝水提醒
* 久坐提醒
* 扭蛋机
* 配饰系统
* AI 聊天功能

⸻

macOS 兼容修改

本 Fork 对原项目进行了以下调整：

* macOS 下不再加载 Windows user32 API
* macOS 下默认关闭全局键盘监听与打字跟随功能
* macOS 打包运行时，本地数据保存到标准 Application Support 目录
* 避免因权限问题导致的崩溃

⸻

安全说明

本版本不会主动申请或使用：

* 输入监控（Input Monitoring）
* 辅助功能权限（Accessibility）
* 摄像头
* 麦克风
* 定位
* 通讯录
* 管理员权限

AI 聊天功能只有在用户自行配置 API 后才会联网。

如果未配置 API，程序不会主动访问外部 AI 服务。

⸻

系统要求

建议使用：

* macOS
* Python 3.10–3.12

已知 Python 3.13 + PyQt5 在部分 macOS 环境下可能出现 Qt 插件兼容问题。

⸻

安装与运行

简单版使用方法（macOS）

1. 下载并解压 NaichaMouse-macOS.zip （右侧release里）
2. 找到 NaichaMouse.app
3. 右键点击 NaichaMouse.app
4. 选择 打开（Open）
5. 如果系统提示无法验证开发者，请再次点击 打开

如果提示“已损坏，无法打开”

将奶茶鼠app移动到download（下载）文件夹

打开终端（Terminal），输入下面命令后回车：

xattr -dr com.apple.quarantine ~/Downloads/NaichaMouse.app

然后再次右键点击 NaichaMouse.app → 打开

为什么会这样？

由于本项目是个人维护的开源版本，没有 Apple 官方签名，因此 macOS 可能会拦截首次运行。这并不代表程序真的损坏，只是系统的安全检查机制。


代码版：
1. 下载项目

下载本仓库源码并解压。

进入项目目录：

cd naichashu

2. 创建虚拟环境

python3 -m venv .venv

3. 激活虚拟环境

source .venv/bin/activate

激活成功后，终端前面会出现：

(.venv)

4. 安装依赖

pip install -r requirements.txt

5. 启动程序

python main.py

⸻

常见问题

ModuleNotFoundError: No module named ‘PyQt5’

原因：

PyQt5 尚未安装到当前 Python 环境。

解决方法：

pip install -r requirements.txt

或：

pip install PyQt5

然后重新运行：

python main.py

⸻

为什么不能直接双击 main.py？

因为 Python 程序依赖额外库（例如 PyQt5）。

直接双击文件或使用系统自带 Python 运行时，可能找不到这些依赖，从而导致启动失败。

建议按照上面的步骤创建虚拟环境并安装依赖后运行。

⸻

本地数据

源码运行时，用户数据会保存在项目目录中，例如：

naicha_mouse_profile.json
naicha_mouse_ai_config.json

这些文件用于保存：

* 等级
* 金币
* 配饰状态
* AI 配置

不建议上传到 GitHub 或分享给他人。

⸻

项目结构

main.py
requirements.txt
IMG_5791/
accessories/
naicha_mouse_state_map.json
naicha_mouse_dialogues.json
naicha_mouse_gacha_pool.json
naicha_mouse_accessories.json

请不要只复制 main.py。

程序运行需要上述图片资源文件夹和 JSON 配置文件。

⸻

免责声明

本仓库为个人维护的 macOS 兼容 Fork。

原项目版权及主要功能设计归原作者 Xzyery 所有。

本 Fork 仅包含兼容性、安全性和运行方式相关修改。
