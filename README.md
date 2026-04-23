# Joycon-Robotics for XLeRobot on Windows

## 安装 BetterJoy 驱动

进入 `hidapi_for_windows/BetterJoy_v7.1/Drivers`
运行 `ViGEmBusSetup_x64.msi`（64位系统），如果是32位系统请运行 `ViGEmBusSetup_x86.msi`

## 代码下载与环境配置

```bash
git clone https://github.com/box2ai-robotics/joycon-robotics.git
conda activate lerobot

cd joycon-robotics
set PYTHONUTF8=1
pip install -e .

# 安装hidapi与numpy
pip install hidapi numpy matplotlib
# 卸载hid，不能与hidapi共存，否则会报错 ImportError: Unable to load any of the following libraries:hidapi.dll
pip uninstall hid
```
