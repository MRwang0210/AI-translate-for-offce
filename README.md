# AI翻译器（办公）

一个 Windows 桌面截图翻译工具。程序常驻系统托盘，可通过全局快捷键截图框选、OCR 识别、调用 OpenAI-compatible API 翻译，并用弹窗展示结果，同时保存本地历史记录。

## 功能

- 截图框选翻译：选中屏幕区域后自动识别文字并翻译。
- OCR + 视觉模型兜底：默认先使用 Windows OCR，识别失败后调用外部视觉模型。
- OpenAI-compatible API：支持自定义 `base_url`、`model`、`api_key`。
- 翻译方向：支持自动识别、英译中、中译英。
- 系统托盘：支持截图翻译、历史记录、设置和退出。
- 本地历史记录：翻译结果保存到 SQLite，便于回看。
- 开机自启：可配置静默启动到托盘。

## 环境要求

- Windows 10/11
- Python 3.10+
- 可用的 OpenAI-compatible API 服务

## 安装运行

```powershell
git clone https://github.com/你的用户名/你的仓库名.git
cd Translator
python -m pip install -r requirements.txt
Copy-Item config.example.json config.json
python main.py
