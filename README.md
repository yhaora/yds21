# yds21

> LLM-assisted UAV spraying & fault-reallocation system

## 📌 项目简介

本项目利用大语言模型（DeepSeek）辅助农业无人机作业决策，优化农药喷洒路径，并在无人机发生故障时通过改进的任务分配算法实时重分配任务，确保作业顺利完成。

## ✨ 主要特性

- 🧠 基于 DeepSeek 大模型进行智能决策辅助
- 🚁 支持多无人机协同喷洒路径规划
- 🔄 故障实时检测与动态任务重分配
- 📊 改进的任务分配算法

## 📂 项目结构

```
├── smart_agriculture_gui.py   # GUI 主程序
├── run_experiments.py         # 实验复现脚本
├── requirements.txt           # Python 依赖列表
├── src/                       # 核心算法源码
├── data/                      # 测试数据集
├── results/                   # 实验结果输出
└── README.md
```

## 🛠️ 运行环境配置

### 操作系统
- Ubuntu 20.04

### Python 版本
- Python 3.8.10

### ROS 版本
- ROS Noetic

### Gazebo 版本
- Gazebo 11.15.1

---

### 部署步骤

#### 1. 克隆仓库

```bash
git clone https://github.com/你的用户名/仓库名.git
cd 仓库名
```

#### 2. 安装 ROS Noetic

```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo apt update
sudo apt install ros-noetic-desktop-full
```

#### 3. 安装 Python 依赖

```bash
pip install -r requirements.txt
```

#### 4. 进入 ROS 工作空间并编译

```bash
cd ~/catkins
catkin_make
```

#### 5. 激活环境变量

```bash
source ~/catkins/devel/setup.bash
```

#### 6. 配置 DeepSeek API 密钥

```bash
export DEEPSEEK_API_KEY="你的密钥"
```

> 💡 提示：可将上述 `source` 和 `export` 命令添加到 `~/.bashrc` 中，避免每次新终端都要手动执行。

---

## 🚀 运行步骤

### 启动 GUI 界面

```bash
python3 smart_agriculture_gui.py
```

### 运行实验（复现测试结果）

```bash
python3 run_experiments.py
```

## 📄 许可证

本项目采用 MIT 许可证，详见 [LICENSE](LICENSE) 文件。
